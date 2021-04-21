<template>
  <div>
    <p v-for="(piece, index) in pieces" :key="index">{{ piece.content }}</p>
  </div>
</template>

<script>
export default {
  props: {
    pieces: {
      type: Array,
      default: undefined,
    },
  },
};
</script>

<style></style>
