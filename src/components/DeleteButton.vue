<template>
    <div>
        <button @click="toastNotify">Delete</button>
    </div>
</template>

<script>
    export default {
        name: "DeleteButton",
        toastNotify: "Successfully deleted!",
        methods: {
            toastNotify() {
                // first arg = name of emit (custom name)
                // optionally list of arguments, this list gets passed along to handler that receives emit
                // additional args need to match args rec'd on other side thats the function(arg,arg,arg..etc)
                this.$root.$emit(`toastNotify`, `Successfully deleted`);
            }
        },
    }
</script>

<style scoped>

</style>