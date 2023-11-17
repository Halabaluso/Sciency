<template>
  <div>
    <HeaderComponent/>
    <HeroComponent id = "home" />
    <FirstDiv id = "soldout" />
    <SecondDiv id = "tickets" />
    <ThreeDiv id = "speakers" />
    <FourDiv id = "organization"/>
    <FiveDiv/>
    <Footer/>
  </div>
</template>

<script setup>
import HeaderComponent from "../components/HeaderComponent.vue"
import FirstDiv from "../components/FirstDiv.vue"
import SecondDiv from "../components/SecondDiv.vue"
import ThreeDiv from "../components/ThreeDiv.vue"
import FourDiv from "../components/FourDiv.vue"
import FiveDiv from "../components/FiveDiv.vue"
import Footer from "../components/Footer.vue"
import HeroComponent from "../components/HeroComponent.vue"
</script>

<style>

</style>