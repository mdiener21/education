<template>
    <div>
        <h1>hi im home</h1>
            <udemy-sections></udemy-sections>
            <appHeader></appHeader>
            <hr>
            <div class="row">
              <app-servers></app-servers>
              <app-server-details></app-server-details>
            </div>
            <hr>
            <app-footer></app-footer>
            <supermap></supermap>
        
    </div>
</template>
<script>
import UdemySection from "./UdemySections.vue";
import Header from "./Shared/Header.vue";
import Footer from "./Shared/Footer.vue";
import Servers from "./Server/Servers.vue";
import ServerDetails from "./Server/ServerDetails.vue";
import MyMap from "./MyMap.vue"


export default {
  components: {
    appHeader: Header,
    udemySections: UdemySection,
    "app-servers": Servers,
    "app-server-details": ServerDetails,
    "app-footer": Footer,
    "supermap" : MyMap

  },
  methods: {
    goBack() {
      window.history.length > 1 ? this.$router.go(-1) : this.$router.push("/");
    }
  }
}
</script>
