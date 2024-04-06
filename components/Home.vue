<div>
<template>
     <AppHeader /> 
<h1>This is the main page.</h1>
  <AppFooter /> 
</template>


<script>
  import {AppHeader} from './AppHeader.vue'
  import {AppFooter} from './AppFooter.vue'
  export default {
   name:'Home',
   components:{ AppHeader, AppFooter}
 
},
mounted(){
    let user = localStorage.getItem('user-info');
    if (!user) { 
        this.$router.push({name: 'SignUp'})
    }
  }
    </script>
</div>