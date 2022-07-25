<script>
import Vue from 'vue';
// Uncomment import and local "components" registration if library is not registered globally.
// import { VComponentsSample } from '@/entry.esm';

export default Vue.extend({
  name: 'ServeDev',
  // components: {
  //  VComponentsSample,
  // }
});
</script>

<template>
  <div id="app">
    <v-components-sample />
  </div>
</template>
