<template>
    <div id="form-two">

        <h1>Form Two:</h1>
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
                <textarea name="message" placeholder="message" id="" cols="30" rows="3"></textarea>
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
        name : "from-two",

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
