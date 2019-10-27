<template>
  <div class="wallet-page">
    <div class="back-index" @click="$router.push({ path: '/' })"/>
    <div class="title">
      Wallet
    </div>
    <div v-if="!openMenu" class="show-wallet-1">
      <img src="/wallet-1.png" alt="">
    </div>
    <div v-else class="show-wallet-2">
      <img src="/wallet-2.png" alt="">
    </div>
    <div class="body-wallet">
      <img id="background" src="/line_blue_faded_background_69077_2560x1600.jpg" alt="">
      <div v-if="openMenu" class="menu-list">
        <div class="row-menu">
          <div>ดูยอดเงิน</div>
          <div>ดู Group</div>
        </div>
        <div class="row-menu">
          <div>โอนเงิน</div>
          <div>ประวัติการโอนเงิน</div>
        </div>
      </div>
    </div>
    <div class="click" @click="openMenu = !openMenu"/>
  </div>
</template>

<script>

export default {
  name: 'Wallet',
  data () {
    return {
      openMenu: false
    }
  },
  methods: {
    // openMenu () {
    //   alert(1)
    // }
  }
}
</script>

<style lang="scss" scoped>
.wallet-page {
  position: relative;
  .back-index {
    position: absolute;
    width: 170px;
    height: 200px;
  }
  .title {
    position: absolute;
    color: #fff;
    font-size: 60px;
    background-color: #262f4a;
    top: 120px;
    left: 170px;
    width: 600px;
  }
  .body-wallet {
    position: absolute;
    width: 1080px;
    height: 1963px;
    top: 242px;
    background: #fff;
    overflow: hidden;
    #background {
      height: 100%;
    }
    .menu-list {
      position: absolute;
      bottom: 0;
      // width: 100%;
      // border: 1px solid #262f4a;
      // border-top-left-radius: 10px;
      // border-top-right-radius: 10px;
      width: 1080px;
      height: 600px;
      background-color: white;
      border-top-left-radius: 20px;
      border-top-right-radius: 20px;
      padding: 20px;
      .row-menu {
        width: 100%;
        display: flex;
        div {
          width: 50%;
          text-align: center;
          border: 1px solid #c4c4c4;
          font-size: 60px;
          height: 290px;
          padding-top: 85px;
        }
      }
    }
  }
  .click {
    position: absolute;
    width: 100%;
    height: 140px;
    bottom: 0;
    // background-color: red;
  }
//   margin: 0 auto;
//   min-height: 100vh;
//   display: flex;
//   justify-content: center;
//   align-items: center;
//   text-align: center;
//   .subtitle {
//     font-weight: 300;
//     font-size: 42px;
//     color: #526488;
//     word-spacing: 5px;
//     padding-bottom: 15px;
//   }
// }

// .links {
//   padding-top: 15px;
}
</style>
