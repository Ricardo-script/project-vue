<template>
    <img :src="avatar" :alt="descricao" width="80">
</template>

<script>
export default {
    name: 'Picture',
    data(){
        return{
            avatar: '/img/user.png',
            descricao: 'user image'
        }
    }
}
</script>