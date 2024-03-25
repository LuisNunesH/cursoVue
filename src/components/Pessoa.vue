<template>
    <div>
        Essa é a descrição da pessoa {{ nome }}
        <Info :email="email" :esta_trabalhando="false"/>
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
                nome: 'Matheus',
                email: 'luis.nunes@sptech.school'
            }
        },
    }
</script>