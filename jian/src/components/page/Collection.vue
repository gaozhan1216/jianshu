<template>
  <div>
    <b-row class="box">
      <b-col cols="8">
        <b-media vertical-align="center" class="article-box">
          <img :src="collectionDetail.collection.collectionUrl" class="article-thumbnail"/>
          <div class="colleciton-info">
            <h6 class="mt-0 mb-1 title">{{collectionDetail.collection.collectionName}}</h6>
            <p class="abstract">
              <span>收藏了{{collectionDetail.collection.articleCount}}篇文章,{{collectionDetail.collection.fansCount}}关注</span>
            </p>
          </div>
          <div class="button-box">
            <b-button variant="outline-success" class="my-btn">投稿</b-button>
            <b-button variant="success" class="my-btn">
              <font-awesome-icon icon="plus" style="color: #FFFFFF;font-size:10pt"/>
              关注
            </b-button>

          </div>
        </b-media>
        <v-article></v-article>
      </b-col>
      <b-col>
        <div class="right-box">
          <p>专题公告</p>
          <p>投稿须知</p>
          <p>{{collectionDetail.collection.notice}}</p>
        </div>
        <div class="right-box">
          <p>分享到</p>
        </div>
        <div class="right-box">
          <span>关注的人({{collectionDetail.fansList.length}})</span>
          <ul class="list collection-follower">
            <li v-for="fans in collectionDetail.fansList" :key="fans.userId">
              <router-link :to="'/u/'+fans.userId">
                <img :src="fans.avatar" class="fans-avatar"/>
              </router-link>
            </li>
          </ul>
        </div>

      </b-col>
    </b-row>
  </div>

</template>

<script>
  import vArticle from '../common/Articles';

  export default {
    components: {
      vArticle
    },
    data() {
      return {
        id: this.$route.params.id,
        collectionDetail: {
          "collection": {},
          "articleList": [],
          "fansList": []
        }
      }
    },
    activated() {
      this.id = this.$route.params.id;
      console.log(this.id);
      if (this.id == 1) {
        this.collectionDetail.collection = {
          "collectionId": 1,
          "collectionName": "读书",
          "collectionUrl": "https://upload.jianshu.io/collections/images/83/1.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64",
          "notice": "读书专题仅收录与读书有关的书评、读书笔记、阅读方法、读书清单等文章。 \n" +
          "文中不得出现非简书的链接;包括但不限于公众号、二维码、头条号、微博、一点资源等带有广告性质的信息; 配图不能带有水印。 \n" +
          "文章收录字数1000字起( 大神请忽略此限制)，请不要直接摘抄原文的话就来投稿。请注意排版美观、请不要密集投稿。 \n" +
          "投稿请查看投稿须知：https://www.jianshu.com/p/2a4cc9232f37 \n" +
          "进群请添加主编微信: MYH561...",
          "articleCount": 49535,
          "fansCount": 1601,
          "articleList": [
            {
              "articleId": 1,
              "title": "测试文章",
              "summary": "测试文章测试文章测试文章测试文章测试文章...",
              "thumbnail": "1.png",
              "authorId": 2,
              "nickname": "作者",
              "comments": 1234,
              "likes": 12
            }
          ]
        };
        this.collectionDetail.fansList = [
          {
            "userId": 1,
            "nickname": "王诗翔",
            "avatar": "https://upload.jianshu.io/users/upload_avatars/3884693/b425c707-d998-46a6-98b1-9b1e241513c3.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96/format/webp"
          },
          {
            "userId": 2,
            "nickname": "乔汉童",
            "avatar": "https://upload.jianshu.io/users/upload_avatars/5796592/73837104-47e5-4fe9-a5be-054bd50b06f7.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96/format/webp"
          },
          {
            "userId": 3,
            "nickname": "胡七筒",
            "avatar": "https://upload.jianshu.io/users/upload_avatars/8781442/79bf6acc-5dd3-49d1-9e2b-6c58066c1442.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96/format/webp"
          },
          {
            "userId": 4,
            "nickname": "冰千里",
            "avatar": "https://upload.jianshu.io/users/upload_avatars/8972166/bd7164e9-2272-4ecf-91d0-f4903a150d4f.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96/format/webp"
          },
          {
            "userId": 5,
            "nickname": "简书版权",
            "avatar": "https://upload.jianshu.io/users/upload_avatars/1835526/9bc600ce-7672-42b8-b03b-1a779593dd45.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96/format/webp"
          }
        ];

      } else {
        this.collection = {};
      }
    }
  }
</script>

<style scoped>
  .box {
    margin-top: 10px;
    margin-bottom: 10px;
  }

  .abstract {
    margin: 0 0 8px;
    font-size: 13px;
    line-height: 20px;
    color: #999;
  }

  .right-box {
    font-size: 12px;
    color: #333;
    line-height: 20px;
    border-bottom: 0.3px solid #EEE;
    padding-top: 10px;
  }

  .list {
    margin-bottom: 20px;
    padding-bottom: 10px;
    list-style: none;
    border-bottom: 1px solid #f0f0f0;
    clear: both;
  }

  .list li {
    display: inline;
    margin-left: -5px;
  }

  .fans-avatar {
    width: 32px;
    height: 32px;
    border-radius: 32px;
    cursor: pointer;
  }

  .colleciton-info {
    float: right;
    margin-right: 380px;
  }

  .button-box {
    clear: both;
    float: right;
    margin-top: -50px;
  }

  .my-btn {
    width: 100px;
    height: 35px;
    border-radius: 20px;
    text-align: center;
    vertical-align: center;
    font-size: 13px;
  }
</style>
