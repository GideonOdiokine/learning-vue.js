<template>
 <h3> {{title}} </h3>
<p>Welcome ..............</p>
<div v-if="showModal" >
  <Modal   theme="sale" @close="toggleModal">
    <template v-slot:links >
      <a href="#">Sign up</a>
      <a href="#">More Info</a>
    </template>
    <h4>Gideon Odiokine Book</h4>
    <p>I'm rich and when will work towards my riches</p>
  </Modal>
</div>

<button @click="toggleModal" >open modal</button>


</template>

<script>
import Modal from './components/Modal.vue'
export default {
  name: "App",
  components:{
    Modal
  },
  data() {
    return {
      title:"My First Vue App",
      header:"Join for a giveaway",
      text:"Grab your copy now",
      showModal:false
    };
  },
  methods:{

    toggleModal(){
      this.showModal = !this.showModal;
    }
    // handleClick(){ 
    //   console.log(this.$refs.name)
    //   this.$refs.name.focus()
    // }
  }
};
</script>

<style>
#app{
  font-family: sans-serif;
  text-align: center;
  margin-top: 60px;
}
 h3{
   border-bottom: 1px solid #ddd;
   padding-bottom:10px;
   display: inline-block;
 }
</style>