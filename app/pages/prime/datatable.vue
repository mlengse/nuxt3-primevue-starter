<script setup lang='ts'>
import { FilterMatchMode } from '@primevue/core/api'

const { tableData, filters, dataTableRef, exportCSV } = usePrimeDataTable()

filters.value = {
  global: { value: null, matchMode: FilterMatchMode.CONTAINS },
  name: { value: null, matchMode: FilterMatchMode.CONTAINS },
  code: { value: null, matchMode: FilterMatchMode.CONTAINS },
  inventoryStatus: { value: null, matchMode: FilterMatchMode.STARTS_WITH },
}

const dataStore = useDataStore()

onMounted(async () => {
  await dataStore.initData()
  tableData.value = dataStore.products
})
</script>

<template lang="pug">
.card
  h2 DataTable Example
  DataTable(ref="dataTableRef", v-model:filters="filters", :value="tableData", data-key="name", :global-filter-fields="['name', 'code', 'inventoryStatus']", striped-rows, :paginator="true", :rows="8", paginator-template="CurrentPageReport FirstPageLink PrevPageLink PageLinks NextPageLink LastPageLink RowsPerPageDropdown", :rows-per-page-options="[8, 15, 50]", current-page-report-template="Showing {first} to {last} of {totalRecords}")
    template(#header)
      .datatable-header
        .flex.justify-between
          span.text-xl Products
          IconField(icon-position="left")
            InputIcon.pi.pi-search
            InputText(v-model="filters.global.value", placeholder="Global Search")
    template(#empty) No Data Found.
    Column(field="name", header="Name", :sortable="true")
    Column(field="code", header="Code", :sortable="true")
    Column(field="price", header="Price", :sortable="true")
    Column(field="inventoryStatus", header="Status", :sortable="true")
    template(#footer)
      .flex.justify-between
        span.text-2xl {{ tableData ? tableData.length : 0 }}
          | Products
        Button(icon="pi pi-external-link", label="Export", @click="exportCSV")
    template(#paginatorRight)

</template>

<style scoped></style>
