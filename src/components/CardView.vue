<template>
  <div class="card" style="width: 18rem;">
  <div class="card-header">
    {{ user.name }}
  </div>
  <ul class="list-group list-group-flush">
    <li class="list-group-item">{{  user.username }}</li>
    <li class="list-group-item">{{ user.email }}</li>
    <li class="list-group-item">{{ user.website }}</li>
  </ul>
</div>
</template>

<script>
// import { ref } from 'vue';

export default {
  props :{
    user: Object
  }

}
</script>

<style>

</style>