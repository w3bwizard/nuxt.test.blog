<template>
  <el-form
    :model="controls"
    :rules="rules"
    ref="form"
    @submit.native.prevent="onSubmit"
  >
    <b>Добавить комментарий</b>
    <el-form-item label="Ник:" prop="name">
      <el-input v-model.trim="controls.name" />
    </el-form-item>
    <el-form-item label="Комментарий:" prop="text">
      <el-input
        type="textarea"
        v-model="controls.text"
        resize="none"
        :rows="2"
      />
    </el-form-item>
    <el-form-item>
      <el-button type="primary" native-type="submit" @click="onSubmit()"
        >Комментировать</el-button
      >
    </el-form-item>
  </el-form>
</template>

<script>
export default {
  data() {
    return {
      controls: {
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
  methods: {
    onSubmit() {
      this.$refs.form.validate((valid) => {
        if (valid) {
          console.log("Коммент отправлен");
        } else {
          console.log("Ошибка валидации");
          return false;
        }
      });
    },
  },
};
</script>

<style lang="scss" scoped>
</style>