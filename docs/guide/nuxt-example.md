## 🚀 How to use in Nuxt
Create Plugin with the following example code
```
import Vue from 'vue';
import vueFabricWrapper from 'vue-fabric-wrapper';

Vue.component("FabricCanvas", vueFabricWrapper.FabricCanvas)
Vue.component("FabricCircle", vueFabricWrapper.FabricCircle)
```

Add this to nuxt.config and use mode client
```
module.exports = {
	plugins: [
			{ src: "@/plugins/fabric.js", mode: "client" }
		]
}
```

Finally use client-only to render only on the client side
```
<template>
  <client-only>
    <fabric-canvas>
      <fabric-circle :id="2"></fabric-circle>
    </fabric-canvas>
  </client-only>
</template>

<script>
export default {

};
</script>

<style>
</style>
```