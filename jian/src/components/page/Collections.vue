<template>
  <div>
    <div class="banner">
      <img src="/static/img/hot.png"/>
    </div>
    <b-row>
      <b-col cols="4" v-for="collection in collectionList" :key="collection.collectionId">
        <div class="collection-wrap">
          <router-link :to="'/c/'+collection.collectionId">
            <img :src="collection.collectionUrl" class="avatar-collection"/>
          </router-link>
          <h5 class="name">{{collection.collectionName}}</h5>

          <span>{{collection.summary}}</span>

          <p>
            <br/>
            <b-button variant="success">关注</b-button>
          </p>
          <p>
            <span>{{collection.articleCount}}篇文章</span>
            <span>{{collection.fansCount}}个关注</span>
          </p>
        </div>
      </b-col>
    </b-row>
  </div>

</template>

<script>
  export default {
    name: "Collections",
    data() {
      return {
        collectionList: []
      }
    },
    created() {
      var that = this
      this.$http
        .get('http://localhost:8080/collection/list')
        .then(function (response) {
          alert(JSON.stringify(response.data.data));
          that.collectionList = response.data.data;
        })
    }
  }
</script>

<style scoped>
  .banner {
    margin-top: 15px;
    width: 100%;
    min-height: 60px;
    background-color: hsla(0, 0%, 71%, .2);
    border-radius: 6px;
  }

  .banner img {
    height: 90px;
    width: 100%;
  }

  .collection-wrap {
    height: 280px;
    margin-top: 80px;
    padding: 0 20px;
    border: 1px solid #e6e6e6;
    border-radius: 4px;
    background-color: hsla(0, 0%, 71%, .1);
    text-align: center;
  }

  .avatar-collection {
    width: 80px;
    height: 80px;
    margin: -40px 0 10px;
    display: inline-block;
    border: 1px solid #ddd;
    background-color: #fff;
    border-radius: 10px;
  }

  .name {
    font-weight: bold;
  }
</style>
