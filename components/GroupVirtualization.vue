<template>
  <div id="createGroup">
    <div class="flex-layout">
      <span>Group</span>
      <select class="input" name="group_select" style="margin-left:110px">
        <option value="เงินบริจาคน้ำท่วม">
          เงินบริจาคน้ำท่วม
        </option>
      </select>
    </div>
    <div class="flex-layout" style="margin-top:40px">
      <!-- <span>ไปยัง</span>
      <input class="input" style="margin-left:85px"> -->
    </div>
    <div class="flex-layout" style="margin-top:40px">
      <!-- <span>จำนวน</span>
      <input class="input" type="number"> -->
    </div>
    <div class="btn" @click="$emit('status','virtualization')">
      <span>ดู</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'createGroup',
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
#createGroup {
  font-size: 52px;
  width: 1080px;
  height: 600px;
  background-color: white;
  border-top-left-radius: 20px;
  border-top-right-radius: 20px;
  padding: 60px 40px 40px 40px;
  .flex-layout {
    display: flex;
  }
  .input {
    margin-left: 50px;
    width: 800px;
    border: 1px solid black;
    border-radius: 20px;
    padding-left: 20px;
    option {
      width: 800px;
      font-size: 52px;
    }
  }
  .btn {
    width: 600px;
    border-radius: 50px;
    height: 120px;
    background-color: cornflowerblue;
    margin-top: 40px;
    margin-left: 220px;
    margin-right: auto;
    cursor: pointer;
    position: relative;
    padding: 20px 80px;
    span {
      font-size: 50px;
      color: white;
    }
  }
}
</style>
