<template>
  <div class="container mt-5">
      <div class="row g-3">
        <div class="col-md-3" v-for="user in users" :key="user.id">
          <card-view :user="user"/>
        </div>
      </div>
  </div>
</template>

<script>
import axios from 'axios';
import { ref } from 'vue';
import CardView from '@/components/CardView.vue';


export default {
  
  components:{
    CardView
  },



  setup(){
    
    const users = ref([]);

    function getUsers(){
    
      axios.get('https://jsonplaceholder.typicode.com/users')
      .then(function (response) {
      
        users.value = response.data;
      
      })
    .catch(function (error) {
   
        console.log(error);
      })
    }

    getUsers(); 


    return {
      users
    }
  }



}
</script>

<style>

</style>