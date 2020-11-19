<template>
  <div>
    <div class="header">
      <span @click="open = !open">{{ open ? "&#x25B2; Collapse" : "&#x25BC; Expand" }}</span>
    </div>
    <slot v-if="open">
      <div> Default Content </div>
    </slot>
  </div>
</template>

<script>
export default {
  name: 'CollapsibleSection',
  data() {
    return {
      open: true,
    };
  },
};
</script>

<style scoped>
  .header {
    background-color: #bbb;
    padding: 3px;
    cursor: pointer;
  }
</style>
