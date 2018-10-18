<template>
  <b-row>
    <b-col cols="8">
      <v-carousel></v-carousel>
      <v-topic></v-topic>
      <v-article></v-article>

      <div class="split-line"></div>
    </b-col>

    <!--右边-->
    <b-col>
      <v-right></v-right>
    </b-col>
  </b-row>
</template>

<script>
  import vCarousel from '../common/Carousel';
  import vTopic from '../common/Topic';
  import vArticle from '../common/Article'
  import vRight from '../common/Right'
  export default {
    name: "Index",
    components: {
      vCarousel,
      vTopic,
      vArticle,
      vRight
    }
  }
</script>

<style scoped>

</style>
