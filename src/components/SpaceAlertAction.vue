<template>
  <div>
    <span class="when" :class="when" /><span class="action"><slot /></span>
  </div>
</template>
<script>
export default {
  props: ["when"]
}
</script>
<style scoped>
div {
  display: flex;
  border: 1px;
  margin: 0px;
  padding: 0px;
}

.when {
  align-self: start;
}

.action {
  align-self: center;
  font-size: smaller;
}

.when::before {
  font-weight: 900;
  margin-right: 1mm;
  text-shadow: 1px 1px grey;
}

.X::before {
  content: "X";
  color: yellow;
}
.Y::before {
  content: "Y";
  color: orange;
}
.Z::before {
  content: "Z";
  color: red;
}
</style>
