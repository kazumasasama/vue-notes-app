<template>
  <div class="note-selectors">
    <NoteSelector
      v-for="note in notes"
      :key="note.id"
      :note="note"
      :selectedNoteId="selectedNoteId"
      v-on:selectNote="selectNote"
    />
  </div>
</template>

<script>
import NoteSelector from "@/components/NoteSelector.vue"
  export default {
    components: {
      NoteSelector,
    },
    data() {
      return {
        notes: [
        { id: 1, body: "This is a first test", timestamp: Date.now() },
        { id: 2, body: "This is a second test", timestamp: Date.now() },
        { id: 3, body: "This is a third test", timestamp: Date.now() },
        { id: 4, body: "This is a fourth test", timestamp: Date.now() }
      ],
      selectedNoteId: 1,
      }
    },
    methods: {
      selectNote(note) {
        this.selectedNoteId = note.id
      },
    },
  }
</script>

<style lang="scss">
  
</style>