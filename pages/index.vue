<template>
  <div class="containerA">
    <img src="/index.png" alt="" @click="$router.push({ name: 'wallet' })" />
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss">
.containerA {
  width: 1080px;
  height: 2340px;
  img {
    position: fixed;
    top: 0;
    left: 0;
  }
}
</style>
