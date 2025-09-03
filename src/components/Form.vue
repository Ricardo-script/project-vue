<template>
    <form action="" @submit="enviarFormulario($event)">
        <InputText />
        <InputText />
        <input type="text" v-model="name">
        <Submit />
    </form>
</template>

<script>
    import InputText from './form/InputText.vue';
    import Submit from './form/Submit.vue';
    export default {
        name: 'Form',
        data(){
            return{
                name: 'Ricardo',
                email: 'teste@gmail.com'
            }
        },
        components: {
            InputText,
            Submit
        },
        methods:{
            enviarFormulario(e){
                e.preventDefault();
                const name = this.name;
                const email = this.email
                console.log({ name, email });
            }
        }
    }
</script>