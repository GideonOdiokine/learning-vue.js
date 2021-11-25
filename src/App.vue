<template>
  <h2 v-for="(name, index) in names" :key="name">{{ index + 1 }} {{ name }}</h2>
  <h2 v-for="name in fullnames" key="name.first">
    {{ name.first }} {{ name.last }}
  </h2>

  <div v-for="actor in actors" >
    {{actor.name}}
    <h6 v-for="movie in actor.movies" >{{movie}}</h6>
  </div>
 <h4 v-for="(value, key,index) in myInfo">
  {{index + 1}} {{key}}  {{value}}
 </h4>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      names: ["Gideon", "Odiokine", "Nancy"],
      fullnames: [
        { first: "Gideon", last: "Odiokine" },
        { first: "Nancy", last: "Asiuloka" },
        { first: "Favour", last: "Odiokine" },
      ],
      actors: [
        { name: "Gideon Odiokine", movies: ["Princess", "Diana"] },
        { name: "John Odiokine", movies: ["Lovery", "Army of Death"] },
      ],
      myInfo:{
        name:'Gideon',
        channel:"Gidicode",
        course:"Vue.js 3"
      }
    };
  },
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
