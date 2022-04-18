<template>
  <main id="app">

    <div>
      <button v-on:click="loadFormOne">Form One</button>
      <button v-on:click="loadFormTwo">Form Two</button>
    </div>

    <!-- Keeps data alive in inactive component (state) -->
    <keep-alive>
      <component v-bind:is="activeComponent"></component>
    <keep-alive/>

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
          + 'quas, sunt nisi quam totam.',

        activeComponent : 'form-one'
      }
    },

    // methods
    methods : {
      
      loadFormOne() {
        this.activeComponent = 'form-one'
      },
      loadFormTwo() {
        this.activeComponent = 'form-two'
      }
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
