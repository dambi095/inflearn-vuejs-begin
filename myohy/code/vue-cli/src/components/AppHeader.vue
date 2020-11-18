<template>
    <header>
        <h1>Header</h1>
        <span>{{ propsdata }}</span>
        <button v-on:click="sendEvent">send</button>
    </header>
</template>

<script>
export default {
    props: [ 'propsdata' ],
    methods: {
        sendEvent: function () {
            this.$emit('renew'); // 위로 이벤트 전달
        }
    }

}
</script>

<style>

</style>