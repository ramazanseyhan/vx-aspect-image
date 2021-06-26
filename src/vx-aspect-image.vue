<template>
  <div class="container">
    <div class="padding-area" :style="aspectRadioPadding" />
    <img class="image" :src="src" :alt="alt" />
  </div>
</template>

<script>
const EDGES = {
  WIDTH: 0,
  HEIGHT: 1,
};
export default {
  data() {
    return {
      ratio: [],
    };
  },
  props: ["src", "alt", "aspectRatio"],
  created() {
    this.ratio = this.aspectRatio.split("/");
  },
  computed: {
    aspectRadioPadding() {
      return {
        "padding-top": `${
          (100 / this.ratio[EDGES.WIDTH]) * this.ratio[EDGES.HEIGHT]
        }%`,
      };
    },
  },
};
</script>

<style scoped>
.container {
  display: block;
  width: 100%;
  position: relative;
  overflow: hidden;
  height: fit-content;
}

.padding-area {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: -999;
}
.image {
  display: block;
  height: 100%;
  width: 100%;
  object-position: center;
  object-fit: contain;
}
</style>