<template>
  <div>
    <b-media right-align vertical-align="center" v-for="article in articleList" :key="article.articleId"  class="article-box">
      <img :src="article.thumbnail" class="article-thumbnail"/>
      <h6 class="mt-0 mb-1 title">{{article.title}}</h6>
      <p class="abstract">
        {{article.summary}}
      </p>
    </b-media>
  </div>

</template>

<script>
  export default {
    name: "Articles",
    data() {
      return {
        articleList: [
          {
            "articleId": 1,
            "title": "微信公众号爬虫",
            "summary": "微信公众号爬虫，目前主要有两种方式： 搜狗搜索有专门的公众号搜索功能，不过只能获取公众号最近10条群发信息，如下图：image.png 登录 微...",
            "thumbnail": "https://upload-images.jianshu.io/upload_images/2377712-a59a8ad8b7b76cc0.png?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
            "nickname": "Namikun",
            "comments": 0,
            "likes": 15
          },
          {
            "articleId": 2,
            "title": "淘宝上有哪些价格不贵，好吃到哭的面值得购买？",
            "summary": "大家好哇！我是最近在日本的小丸子，由于特别爱吃拉面，在日本的每一天我都要吃一碗拉面，再配上一瓶波子汽水，特别滴爽！ 实际上，我经常在家里囤日式拉...",
            "thumbnail": "https://upload-images.jianshu.io/upload_images/1359662-2872d0b5d7f6b9f3.png?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
            "nickname": "小丸子的杂物集",
            "comments": 10,
            "likes": 200
          },
          {
            "articleId": 3,
            "title": "APP推荐类篇一：手机舍不得卸载的8款APP，集生活工作学习于一体",
            "summary": "从有智能手机开始，我们就开始往手机中下载安装各种APP，资讯类、生活类、社交类、拍照的，下载完成后总会因为手机内存不够卸载的，也会因为比较鸡肋删...",
            "thumbnail": "https://upload-images.jianshu.io/upload_images/13934390-ca36abb653ae23dd?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
            "nickname": "迅捷CAD",
            "comments": 1,
            "likes": 26
          },
          {
            "articleId": 4,
            "title": "前世缘今生劫",
            "summary": "（没办法，琳琅让我更文，不更不行啊！刚刚琳琅说我卡文卡的很好，我打算让帝君也剜心。这周更文以后隔两周再更文，不要催。累死了，写个文容易吗我） 第...",
            "thumbnail": "https://upload-images.jianshu.io/upload_images/6856154-4fd5253dde530e81.jpeg?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
            "nickname": "笙笙不息白笙",
            "comments": 14,
            "likes": 12
          },
          {
            "articleId": 5,
            "title": "极简生活",
            "summary": "昨晚整理整理东西，一直到两点多。很多时候打算是十点之前睡觉的。但很多时候自己又打乱了这种规矩。 生活规律总是定了又改，改了又定。 遵守的不是很好...",
            "thumbnail": "https://upload-images.jianshu.io/upload_images/5482569-3d4eb8c7a2cb99c4.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
            "nickname": "会写",
            "comments": 1,
            "likes": 152
          },
          {
            "articleId": 6,
            "title": "［简书交友］我有一个梦想",
            "summary": "自我介绍 嘿！这里是一个02年的水瓶座妹子。 思想跳脱，热情开朗。 偶尔会小丧，但总体的画风一定是积极向上的。 勉强加上文艺的特性吧，虽然有点搞...",
            "thumbnail": "https://upload-images.jianshu.io/upload_images/14273117-b64391760d5c8ee2.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
            "nickname": "YS春虫虫",
            "comments": 47,
            "likes": 15
          }
        ]
      }
    }
  }
</script>

<style scoped>
  .article-box{
    padding-top: 10px;
    border-top: 1px #ccc solid;
    margin-bottom: 15px;
    line-height: 10px;
  }
  .abstract {
    margin: 0 0 8px;
    font-size: 13px;
    line-height: 24px;
    color: #999;
  }

  .title {
    font-weight: bold;
    color: #333;
  }
  .article-thumbnail{
    width: 80px;
    height: 80px;
    border-radius: 10px;
    float:right;
  }
</style>
