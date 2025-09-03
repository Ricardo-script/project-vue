<template>
    <h2>Esta é a descrição da pessoa: {{ nome }}</h2>
    <Info />
    <FormComponent />
</template>08:51

<script>
    import Info from './Info.vue';
    import FormComponent from './Form.vue';
    export default {
        name: 'Pessoa',
        data(){
            return{
                nome: 'Ricardo'
            }
        },
        components:{
            Info,
            FormComponent
        }
    }
</script> 