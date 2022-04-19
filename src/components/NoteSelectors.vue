<script>
import NoteSelector from "./NoteSelector.vue";

export default {
  data: function () {
    return {
      notes: [
        { id: 1, body: "First Note", timestamp: Date.now() },
        { id: 2, body: "Second Note", timestamp: Date.now() },
        { id: 3, body: "Third Note", timestamp: Date.now() },
      ],
    };
  },
  components: {
    NoteSelector,
  },
};
</script>

<template>
  <div class="note-selectors">
    <NoteSelector v-for="note in notes" v-bind:note="note" v-bind:key="note.id" />
  </div>
</template>
