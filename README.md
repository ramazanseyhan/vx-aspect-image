# vx-aspect-image

> Using images with aspect ratio intact.

[![NPM](https://img.shields.io/npm/v/vx-aspect-image.svg)](https://www.npmjs.com/package/vx-aspect-image) [![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)

## Install

```bash
npm install --save vx-aspect-image
```

## Usage

```javascript
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
```

## License

MIT © [](https://github.com/)
