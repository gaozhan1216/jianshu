<template>
  <div>
    <h2>
      个人中心,id为{{this.id}}
    </h2>
    <p>{{this.user.nickname}}</p>
    <p><img :src="this.user.avatar"/></p>
    <font-awesome-icon icon="coffee" style="color: #CB62CB;font-size:30pt"/>
    <font-awesome-icon icon="plus" style="color: #42c02e;font-size:15pt"/>
    <font-awesome-icon icon="heart" style="color: #FF0000;font-size:15pt"/>
    <font-awesome-icon icon="bell" style="color: #DDD;font-size:30pt"/>
    <font-awesome-icon icon="fire" style="color: #FF0000;font-size:20pt"/>
    <font-awesome-icon icon="comment" style="color: #FF0000;font-size:20pt"/>
  </div>

</template>

<script>
  export default {
    name: "User",
    data() {
      return {
        id: this.$route.params.id,
        user: {
          "userId": this.id,
          "nickname": "",
          "avatar": ""
        }
      }
    },
    activated() {
      this.id = this.$route.params.id
      console.log(this.id);
      if (this.id == 1) {
        this.user.nickname = "王诗翔";
        this.user.avatar = "https://upload.jianshu.io/users/upload_avatars/3884693/b425c707-d998-46a6-98b1-9b1e241513c3.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96/format/webp";
      } else {
        this.user.nickname = "";
        this.user.avatar = "";
      }
    }
  }
</script>

<style scoped>

</style>
