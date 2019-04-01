<template>
  <div
    draggable
    @dragstart.self="onDrag"
    @dragover.prevent
    @dragenter.prevent
  >
    <slot/>
  </div>
</template>

<script>
export default {
  props: {
    transferData: {
      type: Object,
      required: true
    }
  },
  methods: {
    onDrag (e) {
      e.dataTransfer.effectAllowed = 'move'
      e.dataTransfer.dropEffect = 'move'

      e.dataTransfer.setData('payload', JSON.stringify(this.transferData))
    }
  }
}
</script>

<style lang="css" scoped>
</style>
