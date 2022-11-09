<template>
  <div class="box has-text-weight-bold has-text-centered">
    <slot></slot>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'BoxBase'
})
</script>

<style scoped>
.box {
  background: #FBCF72;
}
</style>