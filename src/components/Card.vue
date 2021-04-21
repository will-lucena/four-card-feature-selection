<template>
  <div
    class="card"
    :class="{
      'card--cyan': cyan,
      'card--red': red,
      'card--orange': orange,
      'card--blue': blue,
    }"
  >
    <div>
      <h1 class="title">{{ title }}</h1>
      <p class="description">{{ description }}</p>
    </div>
    <img :src="image" alt="icon" class="image" width="50px" height="50px" />
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
    color: {
      type: String,
      default: undefined,
    },
  },
  data() {
    return {
      cyan: false,
      blue: false,
      orange: false,
      red: false,
      colors: {
        cyan: () => (this.cyan = true),
        blue: () => (this.blue = true),
        orange: () => (this.orange = true),
        red: () => (this.red = true),
      },
    };
  },
  computed: {
    image() {
      if (this.imageName != undefined && this.imageName.length > 0) {
        return require(`@/assets/images/${this.imageName}`);
      }
      return require("@/assets/images/image-default.png");
    },
  },
  mounted() {
    this.colors[this.color]();
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/styles.scss";
@import "@/assets/scss/base.scss";

.card {
  background-color: $grey-ligher;
  margin: 1rem;
  min-width: 200px;
  max-width: 400px;
  border-radius: 8px;
  border-top: 4px solid;
  border-top-color: $grey-ligher;
  justify-content: space-between;
}

.card--cyan {
  border-top-color: $cyan;
}

.card--red {
  border-top-color: $red;
}

.card--orange {
  border-top-color: $orange;
}

.card--blue {
  border-top-color: $blue;
}

.title {
  font-family: $font-family;
  color: $blue-darker;
  font-weight: 600;
  font-size: 1.5rem;
}

.description {
  font-family: $font-family;
  color: $grey;
  font-weight: 400;
  font-size: 1rem;
}

.image {
  align-self: flex-end;
  object-fit: contain;
}
</style>
