<template>
<h1>{{title}}</h1>
<p>Have a look at our Promotion</p>
<div v-if="showModal">
   <modal theme="promotion" @click="toggleModal">
   <template v-slot:links>
       <a href="#">Register</a>
       <a href="#">Find our more </a>
   </template>
      <h1>T A R A</h1>
      <p>come and get up to 50% off</p>
      </modal>
</div>
<button @click="toggleModal">Open Modal</button>
</template>
<script>
import modal from './components/Modal-comp'
export default {
  name : 'App',
  components : {
   modal
  },

  data() {
   return{
    title:'T A R A',
    header:'Sign up to win a prize',
    text: 'come and get up to 50% off ',
    showModal:false
   }
  },
  methods: {
    toggleModal() {
    this.showModal = !this.showModal ;
    }
  },
}
</script>
<style>



</style>
