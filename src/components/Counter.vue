<template>
<div>
    <h1>{{titulo}}</h1>
    <p>{{ contador }}</p>
    <button @click=incrementar>+</button>
    <button @click="decrementar">-</button>
    <p> {{contadorAlCuadrado}} </p>
</div>
</template>

<script>
export default {

props: ['title'],
    data () {
        return {

            contador: 10
        }
    },
    methods: {
        incrementar () {
            this.contador++
        },
        decrementar () {
            this.contador--
        },
        getSquare() {
            return this.contador  * this.contador
        }

    },
    computed: {
        contadorAlCuadrado () {
            return this.contador * this.contador
        },
        titulo() {
            return this.title? this.title : 'Sin titulo'
        }

    }
    
    
}
</script>

<style>

</style>