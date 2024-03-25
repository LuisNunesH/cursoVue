<template>
    <div>
        <img :src="avatar" alt="Avatar">
        <Reutilizacao />
    </div>
</template>
<script>
    import Reutilizacao from './Reutilizacao.vue';

    export default {
        name: 'Picture',
        components: {
            Reutilizacao
        },
        data() {
            return {
                avatar: '/img/avatar.png',
                descricao: 'Matheus Battisti'
            }
        }
    }
</script>