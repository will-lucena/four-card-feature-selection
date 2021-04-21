<template>
  <div class="header-box">
    <p
      v-for="(piece, index) in pieces"
      :key="index"
      class="text"
      :class="{ 'text--bold': piece.isBold, 'text--small': piece.isSmall }"
    >
      {{ piece.content }}
    </p>
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

<style lang="scss" scoped>
@import "@/assets/scss/styles.scss";
@import "@/assets/scss/base.scss";

.header-box {
  margin: 2rem 0;
}

.text {
  font-family: $font-family;
  font-weight: 200;
  font-size: 1.5rem;
  color: $grey;
  text-align: center;
  margin: 0.5rem 0;
}

.text--bold {
  font-weight: 600;
  color: $blue-darker;
}

.text--small {
  font-size: 1rem;
  font-weight: 400;
}
</style>
