<template>
    <div class="note-container">
    <NoteSelectors />
    <NoteEditor />
  </div>
</template>

<script>
import NoteSelectors from "@/components/NoteSelectors.vue"
import NoteEditor from "@/components/NoteEditor.vue"
  export default {
    components: {
    NoteSelectors,
    NoteEditor
},
    data() {
      return {
        
      }
    }
  }
</script>

<style lang="scss">
  
</style>