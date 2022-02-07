<template>
  <el-row type="flex" justify="center">
    <el-col :xs="24" :sm="18" :md="12" :lg="10">
      <article class="post">
        <div class="post__title">
          <h1>Post Title</h1>
          <a href="/"><span class="el-icon-back"></span></a>
        </div>
        <div class="post__metrics">
          <small>
            <span class="el-icon-time"></span>
            {{ new Date().toLocaleDateString() }}
          </small>
          <small>
            <span class="el-icon-view"></span>
            42
          </small>
        </div>
        <div class="post__poster">
          <img
            src="http://cheats-by-cs.ru/_ld/0/61.jpg"
            alt="Читерский нагиб"
          />
        </div>
        <div class="post_content">
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sint hic
            sunt facilis dolores? Numquam voluptates earum doloremque, rem
            molestiae quos laborum, eos cumque nam mollitia in culpa sint
            similique facilis eligendi atque voluptatem nihil dolore sunt?
            Laboriosam explicabo adipisci eveniet.
          </p>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sint hic
            sunt facilis dolores? Numquam voluptates earum doloremque, rem
            molestiae quos laborum, eos cumque nam mollitia in culpa sint
            similique facilis eligendi atque voluptatem nihil dolore sunt?
            Laboriosam explicabo adipisci eveniet.
          </p>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sint hic
            sunt facilis dolores? Numquam voluptates earum doloremque, rem
            molestiae quos laborum, eos cumque nam mollitia in culpa sint
            similique facilis eligendi atque voluptatem nihil dolore sunt?
            Laboriosam explicabo adipisci eveniet.
          </p>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sint hic
            sunt facilis dolores? Numquam voluptates earum doloremque, rem
            molestiae quos laborum, eos cumque nam mollitia in culpa sint
            similique facilis eligendi atque voluptatem nihil dolore sunt?
            Laboriosam explicabo adipisci eveniet.
          </p>
        </div>
        <div class="comments" v-if="true">
          <app-comments-form />
          <app-comments v-for="comment in 5" :key="comment" />
        </div>
        <div class="no-comments text-center" v-else>Комментариев нет</div>
      </article>
    </el-col>
  </el-row>
</template>

<script>
import AppComments from "@/components/main/Comment.vue";
import AppCommentsForm from "@/components/main/CommentForm.vue";
export default {
  validate({ params }) {
    return Boolean(params.id);
  },
  components: {
    AppComments,
    AppCommentsForm,
  },
};
</script>

<style lang="scss" scoped>
.post__title,
.post__metrics {
  display: flex;
  justify-content: space-between;
  margin-bottom: 0.2rem;
}
.post__poster {
  padding: 1rem;
  display: flex;
  justify-content: center;
  align-items: center;
}
.post_content {
  padding: 1rem;
  p + p {
    margin: 1rem 0;
  }
}
.no-comments {
  color: rgb(117, 38, 38);
}
</style>

