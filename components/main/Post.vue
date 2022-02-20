<template>
  <el-card class="post" :body-style="{ padding: '0px' }" shadow="hover">
    <header class="post__header" slot="header">
      <h1 class="post__title">
        <a href="/post/" @click.prevent="openPost()">Post Title</a>
      </h1>
      <small
        ><span class="el-icon-time"></span
        >{{ new Date().toLocaleDateString() }}</small
      >
    </header>
    <div class="post__poster">
      <img class="post__img" src="http://cheats-by-cs.ru/_ld/0/61.jpg" />
    </div>

    <div style="padding: 14px">
      <footer class="post__footer">
        <el-button @click.prevent="openPost()" plain>Подробнее </el-button>
        <el-button
          @click.prevent="openPost()"
          class="button"
          type="success"
          plain
          >Скачать чит
        </el-button>
      </footer>
    </div>
  </el-card>
</template>

<!--
  el-icon-chat-square, 
  el-icon-chat-round,
  el-icon-chat-line-square
  el-icon-chat-line-round - иконки чата
-->

<script>
export default {
  methods: {
    openPost() {
      const id = "mega-post";
      this.$router.push(`/post/${id}`);
    },
  },
};
</script>

<style lang="scss" scoped>
.post {
  margin-bottom: 2rem;
}
.post__header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.post__title a {
  text-decoration: none;
  color: #353535;
  transition: color 0.3s linear;
}
.post__title a:hover {
  color: black;
}
.post__poster {
  display: flex;
  padding-top: 1rem;
}
.post__img {
  margin: auto;
  display: block;
}
.post__footer {
  display: flex;
  justify-content: flex-end;
}
</style>