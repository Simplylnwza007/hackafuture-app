<template>
  <div class="wallet-page">
    <link href="https://fonts.googleapis.com/css?family=Athiti&display=swap" rel="stylesheet">
    <div class="back-index" @click="$router.push({ path: '/' })" />
    <div class="title">
      Wallet
    </div>
    <div v-if="message != ''" id="badge">
      <div class="user" />
      <div class="message">
        {{ message }}
      </div>
    </div>
    <div v-if="showVisual" id="badge">
      <div class="user" />
      <div class="visual">
        <div class="circle" style="top: 40px;left:100px;background-color:grey;" />
        <span style="top: 50px;left: 270px">บัญชีรับบริจาค<br>1,500,000 บาท</span>
        <div class="circle" style="top: 240px;left:0px;background-color:orange;" />
        <span style="top: 240px;left: 170px">คุณ<br>1,000,000 บาท</span>
        <div class="circle" style="top: 240px;left:390px;background-color:blue;" />
        <span style="top: 240px;left: 560px">นายประยูร<br>500,000 บาท</span>
        <div class="circle" style="top: 440px;left:0px;background-color:red;" />
        <span style="top: 440px;left: 170px">นายประเสริฐ<br>5,000 บาท</span>
      </div>
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
          <div @click="$router.push({ path: 'balance' })">
            ดูยอดเงิน
          </div>
          <div @click="$router.push({ path: 'virtualization' })">
            Group <br> Virtualization
          </div>
        </div>
        <div class="row-menu">
          <div @click="$router.push({ name: 'transfer' })">
            โอนเงิน
          </div>
          <div @click="$router.push({ path: 'history' })">ประวัติการโอนเงิน</div>
        </div>
      </div>
    </div>
    <div class="click" @click="openMenu = !openMenu" />
  </div>
</template>

<script>
export default {
  name: 'Wallet',
  data () {
    return {
      openMenu: false,
      message: '',
      showVisual: true
    }
  },
  mounted () {
    const page = localStorage.getItem('page')
    switch (page) {
      case 'balance':
        this.setMessage('ยอดเงินคงเหลือ 995,000 บาท')
        break
      case 'transfer':
        this.setMessage('โอนเงินให้ A => B จำนวน 5,000 บาท')
        break
      case 'history':
        this.setMessage('วันที่ 27/10/2019 โอนเงินให้ A => B จำนวน 5,000 บาท')
        break
      default:
        this.setMessage('ยอดเงินคงเหลือ 1,000,000 บาท')
        break
    }
  },
  methods: {
    setMessage(m) {
      this.message = m
    }
  }
}
</script>

<style lang="scss" scoped>
.wallet-page {
  font-family: 'Athiti', sans-serif;
  position: relative;
  #badge{
    position: absolute;
    top: 300px;
    left: 0;
    z-index: 99;
    display: flex;
    .user{
      width: 100px;
      height: 100px;
      margin-left: 50px;
      border-radius: 50%;
      background-color: lightgreen;
    }
    .message{
      font-size: 50px;
      padding: 20px 40px;
      width: 800px;
      height: fit-content;
      margin-left: 50px;
      border-radius: 50px;
      background-color: white;
    }
    .visual{
      font-size: 30px;
      padding: 20px 40px;
      width: 800px;
      height: 800px;
      margin-left: 50px;
      border-radius: 50px;
      background-color: white;
      position: relative;
      .circle{
        position: absolute;
        width: 100px;
        height: 100px;
        margin-left: 50px;
        border-radius: 50%;
        background-color: lightgreen;
      }
      span{
        position: absolute;
      }
    }
  }
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
