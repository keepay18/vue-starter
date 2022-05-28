<template>
  <div>

    <h1>Witaj w systemie do zapisów na zajęcia</h1>
    <div v-if="!loggedIn">
      <label>Zaloguj sie mailem</label>
      <input type="text" v-model="email">
      <button @click="logMeIn()">Zaloguj sie</button>                                                                                                                                           
    </div>
    <div v-else>
      <h2>Witaj {{email}}</h2>
      <a @click="logOut()">Wyloguj</a>
    </div>
    
    
    
    


  </div>
</template>

<script>
import "milligram"
export default {
  data(){
    return{
      email: '',
      loggedIn: false,
    }; 
    
  },
  methods: {
  logMeIn() {
    this.loggedIn = true;
  },
  logOut() {
    this.loggedIn = false;
    this.email='';
  }
}
}
</script>

<style>
  .too-long-info{
    color: red;
  }

</style>
