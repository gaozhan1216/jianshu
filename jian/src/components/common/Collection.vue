<template>
  <div>
    <h4>专题{{id}}详情</h4>
    <b-row>
      <!--左边-->
      <b-col cols="8">
        <b-media vertical-align="center" class="article-box">
          <div class="top">
            <div>
              <img :src="topic.topicUrl"/>
            </div>
            <div class="top_left">
              <p>{{topic.topicName}}</p>
              <p>收藏了：{{topic.articleCount}},关注了：{{topic.fans}}</p>
            </div>
          </div>
          <v-article></v-article>
        </b-media>
      </b-col>

      <!--右边-->
      <b-col>
        <div>
          <span>{{topic.description}}</span>
        </div>
        <div>
          <a class="collection" v-for="fans in fansList" :key="fans.id">
            <div>
              <img :src="fansList.avatar"/>
            </div>
            <div>
              <p>{{fansList.name}}</p>
            </div>
          </a>
        </div>
      </b-col>
    </b-row>
  </div>

</template>

<script>
  import vArticle from '../common/Article'
  export default {
    components:{
      vArticle
    },
    data() {
      return {
        id: this.$route.params.id,
        topic: {},
        articleList: [],
        fansList:[]
      }
    },
    activated() {
      this.id = this.$route.params.id;
      console.log(this.id);
      if (this.id == 1) {
        var t = {
          "id": 1,
          "topicName": "读书",
          "topicUrl": "https://upload.jianshu.io/collections/images/83/1.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
          "summary": "读书读书读书读书读书读书读书读书",
          "articleCount": 49535,
          "fans": 1601,
          "description":"欢迎关注公众号简宝玉( 公众号ID : jianshu4321 )后台回复“指南”获取玩转简书绝密珍贵资料汇总；有问题，找宝玉。简宝玉同志会专程为你答疑解惑关于简书的一切。Hi，很高兴在@IT·互联网专题遇见你。收录范围：收录IT&互联网行业观察与思考，数码产品极客体验分析等类型文章投稿须知：https://www.jianshu.com/p/4edc76104c27",
          "creator":"简书",
          "articleList":[
            {
              "id":1,
              "title":"测试文章",
              "summary":"测试文章测试文章测试文章测试文章测试文章...",
              "thumbnail":"1.png",
              "authorId":2,
              "nickname":"作者",
              "comments":1234,
              "likes":12
            }
          ],
          "fansList":[
            {
              "authorId":1,
              "avatar":"https://upload.jianshu.io/users/upload_avatars/938707/a9b1aa2c94db?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96/format/webp",
              "name":"12"
            },
            {
              "authorId":2,
              "avatar":"https://upload.jianshu.io/users/upload_avatars/938707/a9b1aa2c94db?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96/format/webp",
              "name":"123"
            }
          ]
        };
        this.topic = t;
      } else {
        this.topic = {};
      }
    },
    computed: function () {
      return this.topic;
    }
  }
</script>

<style scoped>
  .top{
    display: flex;
  }
  .top img{
    width: 65px;
    height: 65px;
    border-radius: 10px;
  }
  .collection img{
    width: 100px;
    height: 100px;
  }
</style>
