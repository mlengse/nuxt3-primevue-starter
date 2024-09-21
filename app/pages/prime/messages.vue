<script setup lang="ts">
const { showSuccessMessage, showInfoMessage, showWarnMessage, showErrorMessage } = useMessages()
const { confirmAction, confirmDelete } = useConfirmation()

const lastDeletedId = ref(0)

function doSomeAction() {
  // do something
}

function doSomeDeleteAction(idToDelete: number) {
  // do something
  lastDeletedId.value = idToDelete
}
</script>

<template lang="pug">
div.card
  h2 PrimeVue Toast Demo
  div.flex.flex-row.gap-4
    div
      Button(label="Success", @click="showSuccessMessage('Success Message', 'Message Content')").p-button-success
    div
      Button(label="Info", @click="showInfoMessage('Info Message', 'Message Content')").p-button-info
    div
      Button(label="Warn", @click="showWarnMessage('Warn Message', 'Message Content')").p-button-warning
    div
      Button(label="Error", @click="showErrorMessage('Error Message', 'Message Content')").p-button-danger
  h2 Confirmation
  div.flex.flex-row.gap-4
    Button(label="Trigger action with confirmation", @click="confirmAction(doSomeAction)").p-button-info
    Button(label="Trigger delete action with confirmation", @click="confirmDelete(1, doSomeDeleteAction)").p-button-danger
  h2 Messages
  div.flex.flex-row.gap-4.flex-wrap
    Message(severity="success") Success Message Content
    Message(severity="info") Info Message Content
    Message(severity="warn") Warning Message Content
    Message(severity="error") Error Message Content

</template>

<style scoped></style>
