<template>
    <div class="p1">
        <button @click="add">可以运算+100</button>
        <button @click="change">可以直接给结果</button>
    </div>
</template>
    


<script>
    
export default {
        props: ["xxx","add","change"],
    };
    
    
</script>
    
    
<style>
  .p1{
    padding: 10px;
  }
    
</style>