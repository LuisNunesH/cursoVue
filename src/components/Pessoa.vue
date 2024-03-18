<template>
    <div>
        Essa é a descrição da pessoa {{ nome }}
        <Info />
        <Form />
    </div>
</template>
<script>
    import Info from './Info.vue';
    import Form from './Form.vue';
    export default {
        name: 'Pessoa',
        components: {
            Info
        },
        data(){
            return {
                nome: 'Matheus'
            }
        },
    }
</script>