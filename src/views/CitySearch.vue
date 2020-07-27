<template>
  <div class="city-search">
    <TheNavigation />
    <GoBack />
    <TheCitySearchBanner />
    <TheCitySearch />
    <TheFooter />
  </div>
</template>

<script>
// @ is an alias to /src
import TheNavigation from "@/components/TheNavigation"
import TheFooter from "@/components/TheFooter"
import GoBack from "@/components/GoBack"
import TheCitySearch from "@/components/TheCitySearch"
import TheCitySearchBanner from "@/components/TheCitySearchBanner"

export default {
  name: "Home",
  components: {
    TheNavigation,
    TheFooter,
    GoBack,
    TheCitySearch,
    TheCitySearchBanner
  }
};
</script>