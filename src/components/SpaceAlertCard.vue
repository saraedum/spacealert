<script lang="ts">
import SpaceAlertAction from "./SpaceAlertAction.vue";

export default {
  components: {SpaceAlertAction},
  props: ["x", "y", "z", "subtitle","code"]
}
</script>

<template>
  <div class="card">
    <div class="code">{{ code }}</div>
    <space-alert-action when="X" v-if="x">{{ x }}</space-alert-action>
    <space-alert-action when="Y" v-if="y">{{ y }}</space-alert-action>
    <space-alert-action when="Z" v-if="z">{{ z }}</space-alert-action>
    <div v-if="subtitle != '-'">
      <hr/>
      <span class="subtitle">
        {{ subtitle }}
      </span>
    </div>
  </div>
</template>
<style scoped>
.code {
  position: absolute;
  left: -2cm;
  font-size: x-small;
}
.card {
  position: relative;
  break-inside: avoid;
  border: 1px dashed gray;
  width: 61mm;
  padding: 2mm;
  margin-left: 35mm;
  margin-right: 35mm;
  margin-bottom: 1mm;
  line-height: 1.14em;
}
.subtitle {
  font-size: smaller;
  display: inline;
}
</style>
