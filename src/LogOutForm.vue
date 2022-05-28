<template>
    <div>
        <h2>Witaj {{email}}</h2>
        <a @click="logOut()">Wyloguj</a>
    </div>
</template>

<script>
export default {
    props: ['email'],
    methods: {
        logOut(){
            this.$emit('logout')
        }
    }
}
</script>