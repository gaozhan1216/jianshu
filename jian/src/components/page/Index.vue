<template>
  <b-row>
    <b-col cols="8" class="box">
      <v-carousel></v-carousel>
      <v-hot-collection></v-hot-collection>
      <v-article></v-article>
    </b-col>
    <b-col>
      <b-nav vertical>
        <b-nav-item>
          <b-img src="../../static/img/1.png" class="nav-img"/>
        </b-nav-item>
        <b-nav-item>
          <b-img src="../../static/img/2.png" class="nav-img"/>
        </b-nav-item>
        <b-nav-item>
          <b-img src="../../static/img/3.png" class="nav-img"/>
        </b-nav-item>
        <b-nav-item>
          <b-img src="../../static/img/4.png" class="nav-img"/>
        </b-nav-item>
        <b-nav-item>
          <b-img src="../../static/img/5.png" class="nav-img"/>
        </b-nav-item>
        <b-nav-item>
          <div class="download">
            <b-img src="../../static/img/code.png" class="qrcode"/>
            <div class="info">
              <div class="title">
                下载简书手机APP
              </div>
              <div class="description">
                随时随地发现和创作内容
              </div>
            </div>

          </div>
        </b-nav-item>
      </b-nav>
      <v-hot-user></v-hot-user>
    </b-col>
  </b-row>
</template>

<script>
  import vCarousel from '../common/Carousel';
  import vHotCollection from '../common/HotCollections';
  import vArticle from '../common/Articles';
  import vHotUser from '../common/HotUsers';

  export default {
    name: "Index",
    components: {
      vCarousel, vHotCollection, vArticle, vHotUser
    }
  }
</script>

<style scoped>
  .box {
    margin-top: 15px;
  }

  .nav-img {
    width: 90%;
    min-height: 48px;
  }

  .download {
    margin-bottom: 30px;
    padding: 10px 22px;
    width: 90%;
    border: 1px solid #f0f0f0;
    border-radius: 6px;
    background-color: #fff;
  }

  .qrcode {
    width: 60px;
    height: 60px;
    opacity: .85;
  }

  .info .title {
    margin-top: 4px;
    font-size: 13px;
    color: #999;
  }

  .info {
    position: relative;
    float: right;
    margin-top: 10px;
    margin-right: -20px;
  }

  .description {
    margin-top: 4px;
    font-size: 13px;
    color: #999;
  }
</style>
