<template>
    <div class="recommend-collection">
      <a class="collection" v-for="topic in topicList" :key="topic.id">
        <router-link :to="'/c/'+topic.id">
          <img :src="topic.topicUrl" class="small-img">
          <div class="name more">{{topic.topicName}}</div>
        </router-link>
      </a>
      <router-link to="/collections">
        <span class="more">更多热门专题></span>
      </router-link>
    </div>
</template>

<script>
    export default {
        name: "Topic",
      data() {
        return {
          topicList: [
            {
              "id": 1,
              "topicUrl": "//upload.jianshu.io/collections/images/14/6249340_194140034135_2.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
              "topicName":"@IT·互联网"
            },
            {
              "id": 2,
              "topicUrl": "//upload.jianshu.io/collections/images/283250/%E6%BC%AB%E7%94%BB%E4%B8%93%E9%A2%98.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
              "topicName":"手绘"
            },
            {
              "id": 3,
              "topicUrl": "//upload.jianshu.io/collections/images/13/%E5%95%8A.png?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
              "topicName":"旅行·在路上"
            },
            {
              "id": 4,
              "topicUrl": "//upload.jianshu.io/collections/images/95/1.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
              "topicName":"故事"
            },
            {
              "id": 5,
              "topicUrl": "//upload.jianshu.io/collections/images/83/1.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
              "topicName":"摄影"
            },
            {
              "id": 6,
              "topicUrl": "//upload.jianshu.io/collections/images/21/20120316041115481.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
              "topicName":"简书电影"
            },
            {
              "id": 7,
              "topicUrl": "//upload.jianshu.io/collections/images/4/sy_20091020135145113016.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
              "topicName":"读书"
            },
          ]
        }
      }
    }
</script>

<style scoped>
div{
  display: inline-block;
  padding: 0 11px 0 6px;
  margin-top: 10px;
  font-size: 14px;
  color: black;
}
  .collection{
    margin-left: 40px;
    margin-top: 10px;

  }
  .collection img{
    width: 30px;
    height: 30px;
  }
</style>
