<template>

</template>

<script>
export default {
  name: "App",
  data() {
    return {
     baseMultiply:5,
     baseValue:10
    };
  },
  methods:{
    add(a, b, c){
      return a + b + c
    },
    multiply(num){
      return num * this.baseMultiply;
    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.underline {
  text-decoration: underline;
}
.btn {
  font-size: 20px;
}
.promoted {
  color: rgb(165, 25, 25);
}
.ital {
  font-style: italic;
}
</style>
