<template>
  <div>
    <h1>{{ title }}</h1>
    <p>{{ description }}</p>
    <img :src="image" alt="icon" />
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: undefined,
    },
    description: {
      type: String,
      default: undefined,
    },
    imageName: {
      type: String,
      default: undefined,
    },
  },
  computed: {
    image() {
      if (this.imageName != undefined && this.imageName.length > 0) {
        return require(`@/assets/images/${this.imageName}`);
      }
      return require("@/assets/images/image-default.png");
    },
  },
};
</script>

<style lang="scss" scoped></style>
