<template>
  <div class="container-fluid">
    <header-component/>
  <router-view></router-view>
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';

export default {
  name: 'App',
  components: {
    HeaderComponent
  }
}
</script>

<style>

</style>
