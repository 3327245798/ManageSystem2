<template>
  <div class="errPage-container">
    <el-button icon="el-icon-arrow-left" class="pan-back-btn" @click="back">
      返回
    </el-button>
    <div class="img_401">
     <img class="pan-gif" src="@/assets/401_images/401.gif" alt="401"/>
     </div>
    
  </div>
</template>

<script>
//import errGif from '@/assets/401_images/401.gif'

export default {
  name: 'Page401',
  data() {
    return {
      //errGif
    }
  },
  methods: {
    back() {
      if (this.$route.query.noGoBack) {
        this.$router.push({ path: '/dashboard' })
      } else {
        this.$router.go(-1)
      }
    }
  }
}
</script>

<style lang="scss" scoped>
  .errPage-container {
    height: 60px;
    width: 800px;
    max-width: 100%;
    margin: 100px auto;
    border: 1px red solid;
    .pan-back-btn {
      background: #008489;
      color: #fff;
      border: none!important;
    }
    .img_401{
      background: #373a3a;
      height:50px;
      width: 100%;
    }
    .pan-gif {
      margin: 0 auto;
      display: block;
    }
    .pan-img {
      display: block;
      margin: 0 auto;
      width: 100%;
    }
    .text-jumbo {
      font-size: 60px;
      font-weight: 700;
      color: #484848;
    }
    .list-unstyled {
      font-size: 14px;
      li {
        padding-bottom: 5px;
      }
      a {
        color: #008489;
        text-decoration: none;
        &:hover {
          text-decoration: underline;
        }
      }
    }
  }
</style>
