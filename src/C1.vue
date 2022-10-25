<template>
    <div class="p1">
        <button @click="$emit('update:xxx',xxx+100)">可以运算+100</button>
        <button @click="$emit('update:xxx',`这是字符串`)">可以直接给结果，字符串</button>
        <button @click="$emit('update:xxx',10000)">可以直接给结果，数字</button>
        <button @click="$emit('update:xxx',xxx=10086)">会报警告，不能直接赋值</button>
        <!-- 也可以像下面这样写 -->
        <!-- <button @click="x1">button2</button> -->  
    </div>
</template>
    


<script>
    
export default {
        props: ["xxx"],
        methods: {
          x1(){
            this.$emit('update:xxx',299)
            console.log('值已改变')
          }
        },
    };
    
    
</script>
    
    
<style>
  .p1{
    padding: 10px;
  }
    
</style>