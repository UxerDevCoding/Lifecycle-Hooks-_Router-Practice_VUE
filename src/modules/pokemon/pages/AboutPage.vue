<template>
    <h1>About Page</h1>
    <hr>
    <h2>{{ name }}</h2>
    <button @click="onChangeName">
        Cambiar nombre
    </button>
</template>


<script>
export default {

    data() {
        return {
            name: 'Omar'
        }
    },
    methods: {
        onChangeName() {
            this.name = 'María'
        }
    },
    beforeCreate() {
        console.log('beforeCreate')
    },
    created() {
        this.name = 'Juan Carlos'
        console.log('created')
    },
    beforeMount() {
        console.log('beforeMount') // Peticiones HTTP
    },
    mounted() {
        console.log('mounted')
    },
    beforeUpdate() {
        console.log('beforeUpdate')
    },
    updated() {
        console.log('updated')
    },
    activated() {
        console.log('activated')
    },
    deactivated() {
        console.log('deactivated')
    },
    beforeUnmount() {
        console.log('beforeUnmount')
    },
    unmounted() {
        console.log('unmounted')
    },
    errorCaptured() {
        console.log('errorCaptured')
    },
    renderTracked() {
        console.log('renderTracked')
    },
    renderTriggered() {
        console.log('renderTriggered')
    },

}

</script>