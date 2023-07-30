<script setup lang="ts">
import SpaceAlertCard from "./components/SpaceAlertCard.vue"
import Papa from "papaparse";
import Threats from "./assets/threats.csv?raw";

const threats = Papa.parse(Threats);
</script>

<template>
  <main>
    <space-alert-card v-for="threat in threats.data" :x="threat[7]" :y="threat[8]" :z="threat[9]" :subtitle="threat[10]" :code="threat[0]"/>
  </main>
</template>

<style scoped>
@page {
  margin-left: 0mm;
  margin-right: 0mm;
}
body {
  width: 210mm;
}
</style>
