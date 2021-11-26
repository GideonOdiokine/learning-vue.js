<template>
  <div>
    <pre>
    {{ JSON.stringify(formValues, null, 2) }}
  </pre
    >
  </div>
  <form>
    <div>
      <label for="name">Name</label>
      <input type="text" id="name" v-model="formValues.name" />
    </div>
    <div>
      <label for="profile">Profile Summary</label>
      <textarea id="profile" v-model="formValues.profileSimmary" />
    </div>
    <div>
      <label for="countries">Choose a country:</label>

      <select name="cars" v-model="formValues.country" id="countries">
        <option value="">Select a Country</option>
        <option value="USA">USA</option>
        <option value="Ghana">Ghana</option>
        <option value="UK">UK</option>
      </select>
    </div>

    <div>
      <label for="jobLocation">Job Location</label>

      <select name="jobLocation" multiple v-model="formValues.jobLocation" id="jobLocation">
        <option value="Dubai">Dubai</option>
        <option value="Nigeria">Nigeria</option>
        <option value="India">India</option>
      </select>
    </div>
    <div>
      <input type="checkbox" v-model="formValues.remoteWork"  id="remoteWork" />
      <label for="remoteWork">Open to remote work ?</label>
    </div>
  </form>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      formValues: {
        name: "",
        profileSimmary: "",
        country:"",
        jobLocation:[],
        remoteWork:false
      },
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}
label {
  font-weight: bold;
  display: flex;
  margin-bottom: 5px;
}
input + label {
  font-weight: bold;
  display: inline-flex;
  margin-right: 20px;
}

input[type="text"],
textarea,
select {
  display: block;
  width: 400px;
  padding: 6px 12px;
  font-size: 14px;
  line-height: 1.4287143;
  color: #555;
  background-color: #fff;
  background-image: none;
}
</style>

// //
<h2>{{name}}</h2>
//
<div>
//   <button @click="changeName, increment(1, $event)">Change name </button>
// </div>

//
<h2> {{count}} </h2>

//
<div>
//   <button @click="increment(1, $event)">Increase</button>
//   <button @click="decrement(1)">reduce</button>
//    <button @click="increment(5)">Increase</button>
//   <button @click="decrement(5)">reduce</button>
// </div>

// methods:{ changeName(){ this.name ="Gidysmart" }, increment(num, event){
this.count +=num console.log(event) }, decrement(num){ this.count -=num } }

