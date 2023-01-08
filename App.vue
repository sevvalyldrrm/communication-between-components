<template>
  <div class="container">
    <app-header></app-header>
    <hr>
    <div class="row">
      <server></server>
      <server-details></server-details>
    </div>
    <hr>
    <div class="row">
      <flooter></flooter>
    </div>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Server from './components/Server.vue'
import Flooter from './components/Flooter.vue'
import ServerDetails from './components/ServerDetails.vue'

export default {
  components: {
    'server': Server,
    'flooter': Flooter,
    'server-details': ServerDetails,
    'app-header': Header,
  }
}
</script>