<template>
  <div class="app">
      用户信息：{{user}}  
     
      <!-- C1是C1.vue里的输入框，但是要改App.vue的数据，这里有两个输入框，按这种方式
      是不能用v-model的，因为$event不能区分哪个是用户名哪个是密码，会造成
      数据污染，只能通过这种非语法糖的方式拿到event的具体属性 -->
      <C1  :value="user.userName"  
      :value1="user.userMia" 
      @input="user.userName = $event.mingZi, user.userMia = $event.miMa" />


   APP组件的： <input type="text" :value="user.userName" @input="user.userName=$event.target.value"/>
   APP组件的： <input type="text" v-model="user.userMia" />
  </div>
</template>



<script>
 import C1 from "./C1.vue"
export default {
  data() {
    return {
      user:{
        userName:"1",
        userMia:'2'
      }
    };
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