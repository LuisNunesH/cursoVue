<template>
    <div>
        <p>{{ email }}</p>
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else>Estou em busca de novas oportunidades</p>
        <p>Utilizo as seguintes tecnologias para backend:</p>
        <ul>
            <li v-for="(technology, index) in backendTechnologies" :key="index">{{ technology }}</li>
        </ul>
        <p>Utilizo as seguintes tecnologias para frontend</p>
        <ul>
            <li v-for="technology in frontendTechnologies" :key="technology.id">{{ technology.language }}</li>
        </ul>
        <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
        <p>Para acessar meu portfólio <a v-bind:href="meu_link">basta clicar aqui</a> </p>
        <Picture />
        <div>
            <button @click="showEmail">{{ textoBotao }}</button>
        </div>
    </div>
</template>
<script>
    import Picture from './Picture.vue'

    export default {
        name:'Info',
        components: {
            Picture
        },
        props: {
            email: String,
            esta_trabalhando: Boolean
        },
        data(){
            return {
                mostrar_email: false,
                meu_link: 'https://google.com',
                textoBotao: 'Mostrar e-mail',
                backendTechnologies: ['JavaScript', 'Node.js', 'Express', 'MongoDB'],
                frontendTechnologies: [
                    {id: 1, language: 'HTML'},
                    {id: 2, language: 'CSS'},
                    {id: 3, language: 'JavaScript'}
                ]
            }
        },
        methods: {
            showEmail(){
                this.mostrar_email = !this.mostrar_email
                if(!this.mostrar_email){
                    this.textoBotao = 'Mostrar e-mail'
                } else {
                    this.textoBotao = 'Esconder e-mail'
                }
            }
        }
    }
</script>