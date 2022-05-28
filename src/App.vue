<template>
  <div>

    <h1>Witaj w systemie do zapisów na zajęcia</h1>
    <div v-if="!email">
      <login-form @login="logMeIn($event)"></login-form>                                                                                                                                           
    </div>
    <div v-else>
      <h2>Witaj {{email}}</h2>
      <a @click="logOut()">Wyloguj</a>
    </div>
    

    
    


  </div>
</template>

<script>
import "milligram"
import LoginForm from "./LoginForm";
export default {
  components: {LoginForm},
  data(){
    return{
      email: '',
      
    }; 
    
  },
  methods: {
  logMeIn(username) {
    this.email=username
  },
  logOut() {
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
