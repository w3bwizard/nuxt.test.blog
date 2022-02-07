<template>
  <el-card class="comment" :body-style="{ padding: '0px' }" shadow="never">
    <header class="comment__header" slot="header">
      <b>Никнейм комментатора</b>
      <small>
        <span class="el-icon-time"></span>
        {{ new Date().toLocaleDateString() }}
      </small>
    </header>
    <div class="comment__text">
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Deleniti dicta
      quidem dolorem rerum quos porro deserunt, exercitationem reiciendis
      cupiditate eos!
    </div>
  </el-card>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.comment {
  margin-bottom: 1rem;
}
.comment__header {
  display: flex;
  justify-content: space-between;
}
.comment__text {
  padding: 1rem;
}
</style>