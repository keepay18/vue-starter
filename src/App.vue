<template>
  <div>

    <h1>Witaj w systemie do zapisów na zajęcia</h1>
    <div v-if="!email">
      
      <login-form @login="enter($event)" button-label="Wejdź"></login-form>
                                                                                                                                            
    </div>
    <div v-else>
      <log-out-form :email="email" @logout="logOut()"></log-out-form>
    </div>
    

    
    


  </div>
</template>

<script>
import "milligram"
import LoginForm from "./LoginForm";
import LogOutForm from "./LogOutForm";

export default {
  components: {LoginForm, LogOutForm},
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
