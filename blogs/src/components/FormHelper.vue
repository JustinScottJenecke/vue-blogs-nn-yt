<template>
    <div id="form-helper">

        <h1>Please fill out our form...</h1>
        <form action="" id="form-helper-form">
            <div id="form-header">
                <slot name="form-header"/> <!--slot-->
            </div>
            <div id="form-fields"> 
                <slot name="form-fields"/> <!--slot-->
            </div>
            <div id='form-controls'>
                <slot name="form-controls"/> <!--slot-->
            </div>
            <div id="useful-links">
                <ul>
                    <li>
                        <a href="#">link 1</a>
                    </li>
                    <li>
                        <a href="#">link 2</a>
                    </li>
                    <li>
                        <a href="#">link 3</a>
                    </li>
                    <li>
                        <a href="#">link 4</a>
                    </li>
                </ul>
            </div>
        </form>

    </div>
</template>


<script>
    
    export default ({
        name : 'form-helper',

        data() {
            return {
                sampleText : 'This is the Form Helper component'
            }
        }
    })

</script>


<style scoped>

    #form-helper-form {
        display: flex;
        flex-direction: column;
        padding: 1rem;
    }

    #form-fields ul {
        display: flex;
        flex-direction: column;
        padding: 1rem;
    }

</style>