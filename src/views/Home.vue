<template>
  <div class="home">
    <TheNavigation />
    <!-- <h2>Home Page</h2>
    <router-link :to="{name: 'CitySearch'}">Go to City Search</router-link> -->
    <TheHomePage />
    
    <TheFooter />
  </div>
</template>

<script>
// @ is an alias to /src
import TheNavigation from "@/components/TheNavigation";
import TheFooter from "@/components/TheFooter";
import TheHomePage from "@/components/TheHomePage.vue";


export default {
  name: "Home",
  components: {
    TheNavigation,
    TheFooter,
    TheHomePage
  }
};
</script>
