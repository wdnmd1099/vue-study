<template>
  <div class="p1">
  
    C1组件的 用户名：<input  :value="value"   @input="oninput" />
    C1组件的 密码：  <input  :value="value1"  @input='oninput1'/> 
          
  </div>

</template>
  

<script>
export default {
        props: ["value","value1"],
       data(){
        return {
        user:{
            mingZi: '占位',
            miMa: '占位',
          }
        }
       },
     methods:{
      oninput(e){
        this.user.mingZi = e.target.value
          this.$emit('input',this.user)
      },
      oninput1(e){
        this.user.miMa = e.target.value
          this.$emit('input',this.user)
      },
     }
  };
</script>
  
  
<style>
.p1{
  padding: 10px;
}
  
</style>