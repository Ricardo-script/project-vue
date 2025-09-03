<template>
    <div>
        <HeaderComponent />
        <h1>Olá mundo</h1>
        <PrimeiroComponente />
        <LyfeCycle />
        <Pessoa />
    </div>
</template>

<script>
    import HeaderComponent from './components/Header.vue';
    import PrimeiroComponente from './components/PrimeiroComponente.vue';
    import LyfeCycle from './components/LifeCycle.vue';
    import Pessoa from './components/Pessoa.vue';
    export default {
        name: 'App',
        components: {
            HeaderComponent,
            PrimeiroComponente,
            LyfeCycle,
            Pessoa,
        },
    }
</script>
