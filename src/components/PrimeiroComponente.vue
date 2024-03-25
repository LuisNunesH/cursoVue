<template>
    <div>
        <h1>Oi</h1>
        <MultiplosEventos />
        <Reutilizacao />
    </div>
</template>

<script>
    import MultiplosEventos from './MultiplosEventos.vue'
    import Reutilizacao from './Reutilizacao.vue'

    export default {
        name: 'PrimeiroComponente',
        components: {
            MultiplosEventos,
            Reutilizacao
        },
        data(){
            return {
                nome: 'Maria'
            }
        }
    }
</script>