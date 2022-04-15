<template>
  <div
    class="note-selector"
    :class="{active: selectedNoteId === note.id}"
    @click="selectNote(note)"
  >
    <p class="note-selector-title">{{ note.body }}</p>
    <p class="note-selector-timestamp">{{ note.timestamp }}</p>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        
      }
    },
    props: [
      "note",
      "selectedNoteId"
    ],
    methods: {
      selectNote(note) {
        this.$emit("selectNote", note);
      },
    },
  }
</script>

<style lang="scss">
  
</style>