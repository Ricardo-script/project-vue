<template>
    <div>
        <h1>Olá Vue!</h1>
        <p>Meu nome é {{ nome }} e tabalho como {{ profissao }}</p>
    </div>
    <MultiplosEventos />
</template>

<script>
    import MultiplosEventos from './MultiplosEventos.vue';
    export default {
        name: ' ',
        components: {
            MultiplosEventos
        },
        data(){
            return{
                nome: 'Ricardo',
                profissao: 'Desenvolvedor'
            }
        }
    }
</script>