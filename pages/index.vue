<template>
  <div>
    <el-row type="flex" justify="center">
      <el-col :xs="24" :sm="20" :md="14" :lg="12">
        <app-post 
          v-for="post in 3"
          :key="post"
        />
      </el-col>
    </el-row>
  </div>
</template>

<script>
import AppPost from '@/components/main/Post'
export default {
  head: {
    title: 'Главная'
  },
  components: {
    AppPost
  }
}
</script>
