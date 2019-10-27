<template>
  <div id="badge">
    <div class="user" />
    <div class="message" />
  </div>
</template>

<script>
export default {
  name: 'Badge',
  components: {},
  props: {},
  data () {
    return {
    }
  },
  mounted () {},
  methods: {}
}
</script>

<style lang="scss" scoped>
#badge {
  .user{
    width: 100px;
    height: 100px;
    margin-left: 50px;
    border-radius: 50%;
    background-color: lightgreen;

  }
}
</style>
