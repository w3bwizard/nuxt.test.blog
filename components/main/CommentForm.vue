<template>
  <el-form
    :model="ruleForm"
    :rules="rules"
    ref="ruleForm"
    label-width="120px"
    class="demo-ruleForm"
  >
    <el-form-item label="Ник:" prop="name">
      <el-input v-model="ruleForm.name"></el-input>
    </el-form-item>
    <el-form-item label="Комментарий:" prop="desc">
      <el-input type="textarea" v-model="ruleForm.text"></el-input>
    </el-form-item>
    <el-form-item>
      <el-button type="primary" @click="submitForm('ruleForm')"
        >Create</el-button
      >
    </el-form-item>
  </el-form>
</template>

<script>
export default {
  data() {
    return {
      ruleForm: {
        name: "",
        text: "",
      },
      rules: {
        name: [
          {
            required: true,
            message: "Укажите никнейм",
            trigger: "blur",
          },
        ],
        text: [
          {
            required: true,
            message: "Добавте текст комментария",
            trigger: "blur",
          },
        ],
      },
    };
  },
};
</script>

<style lang="scss" scoped>
</style>