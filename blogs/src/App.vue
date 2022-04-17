<template>
  <main id="app">

    <form-one/>
    <form-two/>

  </main>
</template>


<script>
  import FormOne from './components/FormOne.vue';
  import FormTwo from './components/FormTwo.vue';

  export default {

    // Component Name
    name: 'App',

    // Sub-Components 
    components : {
      'form-one' : FormOne,
      'form-two' : FormTwo    
    },

    // Data
    data() {
      return {
        title : "This is the Slot Title",

        text : 'Lorem ipsum dolor sit amet consectetur adipisicing elit. \n'
          + 'Rerum, eos dignissimos! Eligendi nostrum id cupiditate veniam dolor, \n '
          + 'mollitia hic libero repudiandae harum aliquid quos doloremque \n'
          + 'quas, sunt nisi quam totam.'
      }
    },

    // methods
    methods : {

    }

  }
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
