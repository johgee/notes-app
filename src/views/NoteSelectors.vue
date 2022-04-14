<template>
  <div class="note-selectors">
    <NoteSelector v-for="note in notes" v-bind:key="note.id" v-bind:note="note" />
  </div>
</template>

<script>
import NoteSelector from "./NoteSelector.vue";

export default {
  components: {
    NoteSelector,
  },
  data: function () {
    return {
      notes: [
        { id: 1, body: "first test", imestamps: Date.now() },
        { id: 2, body: "second test", imestamps: Date.now() },
        { id: 3, body: "third test", imestamps: Date.now() },
        { id: 4, body: "fourth test", imestamps: Date.now() },
      ],
    };
  },
};
</script>
