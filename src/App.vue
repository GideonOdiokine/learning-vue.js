<template>
<h2>{{name}}</h2>
<div>
  <button @click="changeName, increment(1, $event)">Change name </button>
</div>

<h2> {{count}} </h2>

<div>
  <button @click="increment(1, $event)">Increase</button>
  <button @click="decrement(1)">reduce</button>
   <button @click="increment(5)">Increase</button>
  <button @click="decrement(5)">reduce</button>
</div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
     name:'Gideon',
     count:0
    };
  },
  methods:{
    changeName(){
      this.name ="Gidysmart"
    },

   increment(num, event){
     this.count +=num
     console.log(event)
   },
   decrement(num){
     this.count -=num
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
