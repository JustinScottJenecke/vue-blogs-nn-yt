<template>
  <main id="app">

    <!-- FormHelper.vue -->
    <form-helper>
      <div slot="form-header"> 
         <h2>
            Blog Creator
          </h2>
         <p>
            Use the provided form to create new Blogs
         </p>
      </div>

      <div slot="form-fields"> 
        <input type="text" placeholder="name" required>
        <input type="password" placeholder="password" required>
      </div>

      <div slot="form-controls"> 
        <input 
          type="submit"
          v-on:click.prevent="handleSubmit"
          value="Submit"
        >
      </div>
    </form-helper>
    <!-- FormHelper.vue -->

  </main>
</template>


<script>
  import FormHelper from './components/FormHelper.vue';

  export default {

    // Component Name
    name: 'App',

    // Sub-Components 
    components : {
      'form-helper' : FormHelper
    
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
