<!-- eslint-disable -->
<template>
  <form @submit.prevent>
    <h4>Создание поста</h4>
    <input v-model="post.title" class="input" type="text" placeholder="Название">
    <input v-model="post.body" class="input" type="text" placeholder="Описание">
    <my-button @click="createPost" class="btn btn-big">Создать</my-button>
  </form>  
</template>
<!-- eslint-disable -->
<style lang='scss' src="./post-form.scss" scoped></style>
<!-- eslint-disable -->
<script>
import MyButton from '../UI/MyButton/MyButton.vue';
export default {
  components: { MyButton },
  data() {
    return {
      post: {
        title: "",
        body: "",
      }
    }
  },
  methods: {
    createPost() {
      this.post.id = Date.now();
      this.$emit("create", this.post)
      this.post = {
        title: "",
        body: "",
      }
    }
  }
}
</script>