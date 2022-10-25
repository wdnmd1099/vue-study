<template>
  <div class="app">
      这是xxx的值：{{xxx}}
      <C1 :xxx.sync="xxx"/>
  </div>
</template>



<script>
import C1 from "./C1.vue"
export default {
  data() {
    return {xxx:100,};
  },
  components: {C1},
};
</script>



<style>
.app {
    border: 3px solid red;
    padding: 30px;
}
</style>