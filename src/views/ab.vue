<template>
  <div>
    <h1>This is an ab</h1>
    <h1>{{sss}}</h1>
  </div>
</template>

<script>
export default {
  name: "Arya",
  data() {
    return {
      name: "Arya",
    };
  },
  computed:{
    sss(){
      return this.$route.params.ex
    }
  },
  // 添加组件内守卫
  // 又添加了一个注释
  // 第三个注释
  beforeRouteEnter: (to, from, next) => {
    next((vm) => {
      alert("hello" + vm.name);
    });
  },
};
</script>

