<template>
<h2>add method {{add(3,8,9)}}</h2>
<h2>add method {{add(12,12,10)}}</h2>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
     
    };
  },
  methods:{
    add(a, b, c){
      return a + b + c
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
