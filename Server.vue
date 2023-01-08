<template>
  <div>
    <div class="col-xs-12 col-sm-6">
      <ul class="list-group">
        <server-list @click.native="sendToServer(server)" v-for="server in servers" :serverData="server"></server-list>
      </ul>
    </div>
  </div>
</template>

<script>
import ServerList from './ServerList.vue';
import {eventBus} from '../main'

export default {
  data: function () {
    return {
      servers: [
        { id: 1, status: "Kritik" },
        { id: 2, status: "Normal" },
        { id: 3, status: "Tehlike" },
        { id: 4, status: "Bilinmiyor" }
      ]
    }
  },
  components : {
    'server-list' : ServerList
  },
  methods: {
    sendToServer(server) {
      eventBus.sendToData(server);
    }
  }

}
</script>

<style scoped>

</style>

