<script>
import Vue from "vue";
import VxAspectImage from "@/vx-aspect-image.vue";

export default Vue.extend({
  name: "ServeDev",
  components: {
    VxAspectImage,
  },
});
</script>

<template>
  <div id="app">
    <vx-aspect-image
      src="https://picsum.photos/900/400"
      aspectRatio="9/4"
      alt="image-alt"
    />
  </div>
</template>


<style>
html,
body,
#app {
  margin: 0;
  padding: 0;
  height: 100%;
}
#app {
  max-width: 100%;
}
</style>