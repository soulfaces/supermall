<template>
  <div class="tab-bar">
    <slot></slot>
  </div>
</template>

<script>
  export default {
    name: "tab-bar"
  }
</script>

<style >
  .tab-bar {
    display: flex;
    background-color: #f0f0f0;
    height: 49px;
    bottom: 0;
    left: 0;
    right: 0;
  }
</style>
