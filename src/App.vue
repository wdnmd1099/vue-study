<template>
  <div class="app">
      这是xxx的值：{{xxx}}
      <C1/>
  </div>
</template>



<script>
import C1 from "./C1.vue"
export default {
  data() {
    return {xxx:100,};
  },
  components: {C1},
  provide(){
    return {
      xxx:this.xxx,
      add:this.add,
      change:this.change,
    }
  },
  methods: {
    add(){
        this.xxx += 100
        console.log(this.xxx)
      },
      change(){
        this.xxx = 2223333
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