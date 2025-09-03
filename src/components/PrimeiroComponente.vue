<template>
    <div>
        <h1>Olá Vue!</h1>
        <p>Meu nome é {{ nome }} e tabalho como {{ profissao }}</p>
    </div>
</template>

<script>
    export default {
        name: ' ',
        data(){
            return{
                nome: 'Ricardo',
                profissao: 'Desenvolvedor'
            }
        }
    }
</script>