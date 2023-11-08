<template>
  <v-main>
    <Navigation />
    <router-view />
    <Footer />
  </v-main>
</template>

<script setup>
import Navigation from "@/components/Navigation.vue";
import Footer from "@/components/Footer.vue";
</script>
