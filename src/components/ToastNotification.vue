<!-- toast notification is popular, its a short popup at top of page then disappears -->

<!-- NULL and Empty Strings also means False in javascript -->

<!-- after git cloning a vuejs you have to run npm install -->

<template>
    <!-- have to style Ref in JS script only -->
    <!-- a number that equals to zero is false, if the msgQueue has a length display it, if NOT don't display -->
    <div v-if="msgQueue.length" class="baseDiv">
        <div v-for="(msg, index) in msgQueue" :key="index">
            <h1>{{msg}}</h1>
            <button @click="clearMessage(index)">Dismiss</button>
        </div>
    </div>
</template>

<script>


    export default {
        name: "ToastNotification",
        data() {
            return {
                msgQueue: []
            }
        },
        methods: {
            handleNotification(message) {
                this.msgQueue.push(message);
            },
            clearMessage(index){
                this.msgQueue.splice(index, 1);
            }
        },
        mounted () {
            this.$root.$on('toastNotify', this.handleNotification);
        },
    }
</script>

<style scoped>
.baseDiv{
    border: 2px dotted orange;
    width: 20vw;
    /* fixed will always show on screen no matter if you've scrolled down eg notifications*/
    position: fixed;
    right: 10px;
    top: 10px;
}
</style>