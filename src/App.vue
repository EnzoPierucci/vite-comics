<script>
import HeaderComp from "./components/headerComp.vue"
import MainComp from "./components/mainComp.vue"
import BlueBar from "./components/blueComp.vue"
import FooterComp from "./components/footerComp.vue"
import CardComp from "./components/cardComp.vue"
import comicsData from "./components/dc-comics.json"

export default {
    components: {
        HeaderComp,
        MainComp,
        BlueBar,
        FooterComp,
        CardComp,
    },
    data() {
    return {
      comics: comicsData,
    };
  },
}
</script>

<template>

<HeaderComp/>
<MainComp/>

<div class="container mx-auto">
    <div class="grid grid-cols-3 gap-4 py-8">
      <CardComp
        v-for="comic in comics"
        :key="comic.id"
        :comic="comic"
      />
    </div>
  </div>
<BlueBar/>
<FooterComp/>
<SocialComp/>

</template>

<style scoped>

</style>
