<template>
    <div id="form-one">

        <h1>Form One:</h1>
        <!-- Form Helper -->
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
        <!-- /Form Helper -->

    </div>
</template>


<script>
    import FormHelper from './FormHelper.vue'

    export default ({
        
        // --- Name ---
        name : "from-one",

        // --- Components ---
        components : {
            'form-helper' : FormHelper
        },

        // --- Data ---
        data() {
            return {

            }
        },
        
        // --- Methods ---
        methods : {

        },

        // --- Props ---
        props : {

        }
    })
</script>


<style scoped>

</style>
