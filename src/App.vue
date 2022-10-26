<template>
  <div class="app">
      这是xxx的值：{{xxx}}
      <C1 :xxx="xxx" :add="add" :change="change"/>
  </div>
</template>



<script>
import C1 from "./C1.vue"
export default {
  data() {
    return {xxx:100,};
  },
  components: {C1},
  methods: {
    change(){
      this.xxx = 22333
      console.log(this.xxx)
    },
    add(){
      this.xxx+=100
      console.log(this.xxx)
    }

  },
};
</script>



<style>
.app {
    border: 3px solid red;
    padding: 30px;
}
</style>