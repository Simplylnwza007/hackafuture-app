<template>
  <div class="containerA">
    <img src="/test.png" alt="" @click="$router.push({ name: 'wallet' })" />
    <CreateGroup id="createGroup"></CreateGroup>
  </div>
</template>

<script>
import CreateGroup from '@/components/CreateGroup'
export default {
  components: {
    CreateGroup
  }
}
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
  #createGroup {
    position: fixed;
    z-index: 3;
    bottom: 142px;
    left: 0;
  }
}
</style>
