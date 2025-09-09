<template>
    <img :src="avatar" :alt="descricao" width="80">
    <MudarImagem @mudarImagem="trocarImagem"/>
</template>

<script>
import MudarImagem from './MudarImagem.vue';
export default {
    name: 'Picture',
    components: {
        MudarImagem
    },
    methods: {
        trocarImagem(){
            this.avatar = '/img/user02.png'
        }
    },
    data(){
        return{
            avatar: '/img/user.png',
            descricao: 'user image'
        }
    }
}
</script>