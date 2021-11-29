<template>
 <h3> {{title}} </h3>

<Modal/>
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
      title:"My First Vue App"
    };
  },
  methods:{
    handleClick(){
      console.log(this.$refs.name)
      this.$refs.name.focus()
    }
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