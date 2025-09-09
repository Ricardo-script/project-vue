<template>
    <p>{{ email }}</p>
    <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
    <p v-else>Estou em busca de novas oportunidades</p>
    <p>Utilizo as seguintes tecnologias para o back-end:</p>
    <ul>
        <li v-for="(technology, index) in backend_technologies" :key="index">
            {{ technology }}
        </li>
    </ul>
    <p>Utilizo as seguintes tecnologias para o front-end:</p>
    <ul>
        <li v-for="technology in frontend_technologies" :key="technology.id">
            {{ technology.language }}
        </li>
    </ul>
    <div>
        <button @click="showEmail">{{ textoBotao }}</button>
    </div>
    <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
    <p>Para acessar meu portifólio <a v-bind:href="meu_link" target="_blank">basta clicar aqui</a></p>
    <PictureComponent />
</template>

<script>
import PictureComponent from '@/components/Picture.vue';
export default {
    name: 'Info', 
    props:{
        email: String
    },
    data(){
        return {
            esta_trabalhando: false,
            mostrar_email: true,
            meu_link: 'https://google.com',
            textoBotao: 'Mostrar e-mail',
            backend_technologies: ['Javascript','PHP', 'Python'],
            frontend_technologies: [
                {id: 1, language: 'HTML'},
                {id: 1, language: 'CSS'},
                {id: 1, language: 'Vue'},
            ],
        }
    },
    components: {
        PictureComponent
    },
    methods:{
        showEmail(){
           this.mostrar_email = !this.mostrar_email;
           if(!this.mostrar_email){
            this.textoBotao = 'Mostrar e-mail'
           }else{
            this.textoBotao = 'Ocultar e-mail'
           }
        }
    }
}
</script>