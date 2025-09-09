<template>
    <h2>Esta é a descrição da pessoa: {{ nome }}</h2>
    <Info :email="email"/>
    <FormComponent />
</template>08:51

<script>
    import Info from './Info.vue';
    import FormComponent from './Form.vue';
    export default {
        name: 'Pessoa',
        data(){
            return{
                nome: 'Ricardo',
                email: 'ricardo@gmail.com.br'
            }
        },
        components:{
            Info,
            FormComponent
        }
    }
</script> 