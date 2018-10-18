<template>
  <div class="recommend-collection">
    <a class="collection" v-for="article in articleList" :key="article.id">
      <router-link :to="'/c/'+article.id">
        <div class="media" style="margin-top: 20px">
          <div class="media-left">
            <div class="title" style="color: black;font-weight: bolder">
              <p>{{article.articleTitle}}</p>
            </div>
            <div class="content" style="color: darkseagreen;font-size: 13px">
              <p>{{article.articleContent}}</p>
            </div>
            <div class="down" >
              <a class="nickname" target="_blank" style="color: darkseagreen;font-size: 13px">{{article.articleWriter}}</a>
              <a target="_blank" style="color: darkseagreen;font-size: 13px">
                <i class="iconfont ic-list-comments"></i> {{article.articleComment}}
              </a>
              <span  style="color: darkseagreen;font-size: 13px"><i class="iconfont ic-list-like"></i> {{article.articleFollow}}</span>
            </div>
          </div>
          <div class="media-right">
            <div>
              <div class="pic">
                <img :src="article.articlePic">
              </div>
            </div>
          </div>
        </div>
      </router-link>
    </a>
  </div>
</template>

<script>
    export default {
        name: "Article",
      data(){
          return{
            articleList:[
              {
                "id":1,
                "articleTitle":"推荐10个可以免费学习的网站",
                "articleContent":"Word联盟 http://www.wordlm.com/ Word联盟是一个专注Word教程的网站，它提供包括：海量Word模板免费下载",
                "articlePic":"https://upload-images.jianshu.io/upload_images/3283382-0005c074c584552a.jpg!thumbnail?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
                "articleComment":12,
                "articleFollow":123,
                "articleWriter":"木子奇"
              },
              {
                "id":2,
                "articleTitle":"树洞-是不是和别人睡过的女孩就不是好女孩了？",
                "articleContent":"我快大学毕业了，和男朋友在一起两年多了，在一起半年之后发生关系，他跟我说这很正常，不要有心理负担，但是我看见一些文章，似乎对待我这样的人并不友好...",
                "articlePic":"https://upload-images.jianshu.io/upload_images/3283382-0005c074c584552a.jpg!thumbnail?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
                "articleComment":12,
                "articleFollow":123,
                "articleWriter":"木子奇"

              },
              {
                "id":3,
                "articleTitle":"用Python发一个高逼格的朋友圈【附代码】",
                "articleContent":"前阵子在网上看到这个有趣的教程，马上就来实践学习一下，并提供给有需要的朋友学习。 昨晚就敲了代码并且发了朋友圈实验了一下，用Candice女神镇",
                "articlePic":"https://upload-images.jianshu.io/upload_images/3283382-0005c074c584552a.jpg!thumbnail?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
                "articleComment":12,
                "articleFollow":123,
                "articleWriter":"木子奇"
              },
              {
                "id":4,
                "articleTitle":"电脑处理器酷睿i5和i7哪一个好？原来懂电脑的人都这么选！",
                "articleContent":"大家在买电脑的时候，应该会出现这种情况，不知道电脑处理器i5和i7哪一个好？而酷睿i7又是目前最新的处理器，性能肯定不耐，其实今天小编想告诉你",
                "articlePic":"https://upload-images.jianshu.io/upload_images/3283382-0005c074c584552a.jpg!thumbnail?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
                "articleComment":12,
                "articleFollow":123,
                "articleWriter":"木子奇"              },
              {
                "id":5,
                "articleTitle":"树洞-是不是和别人睡过的女孩就不是好女孩了？",
                "articleContent":"我快大学毕业了，和男朋友在一起两年多了，在一起半年之后发生关系，他跟我说这很正常，不要有心理负担，但是我看见一些文章，似乎对待我这样的人并不友好...",
                "articlePic":"https://upload-images.jianshu.io/upload_images/3283382-0005c074c584552a.jpg!thumbnail?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
                "articleComment":12,
                "articleFollow":123,
                "articleWriter":"木子奇"
              },
              {
                "id":6,
                "articleTitle":"树洞-是不是和别人睡过的女孩就不是好女孩了？",
                "articleContent":"我快大学毕业了，和男朋友在一起两年多了，在一起半年之后发生关系，他跟我说这很正常，不要有心理负担，但是我看见一些文章，似乎对待我这样的人并不友好...",
                "articlePic":"https://upload-images.jianshu.io/upload_images/3283382-0005c074c584552a.jpg!thumbnail?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
                "articleComment":12,
                "articleFollow":123,
                "articleWriter":"木子奇"
              },
              {
                "id":7,
                "articleTitle":"树洞-是不是和别人睡过的女孩就不是好女孩了？",
                "articleContent":"我快大学毕业了，和男朋友在一起两年多了，在一起半年之后发生关系，他跟我说这很正常，不要有心理负担，但是我看见一些文章，似乎对待我这样的人并不友好...",
                "articlePic":"https://upload-images.jianshu.io/upload_images/3283382-0005c074c584552a.jpg!thumbnail?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
                "articleComment":12,
                "articleFollow":123,
                "articleWriter":"木子奇"
              },
              {
                "id":8,
                "articleTitle":"树洞-是不是和别人睡过的女孩就不是好女孩了？",
                "articleContent":"我快大学毕业了，和男朋友在一起两年多了，在一起半年之后发生关系，他跟我说这很正常，不要有心理负担，但是我看见一些文章，似乎对待我这样的人并不友好...",
                "articlePic":"https://upload-images.jianshu.io/upload_images/3283382-0005c074c584552a.jpg!thumbnail?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240",
                "articleComment":12,
                "articleFollow":123,
                "articleWriter":"木子奇"
              }
            ]
          }
      }
    }
</script>

<style scoped>
.collection img{
  width: 100px;
  height: 100px;
}
</style>
