<!-- eslint-disable -->
<template>
  <div class="app">
    <post-form
      @create="createPost"
    />
    <post-list
      :posts="posts"
      @create="createPost"
    />
  </div>
</template>
<!-- eslint-disable -->
<style lang='scss' src="./app.scss"></style>
<!-- eslint-disable -->
<script>
import PostForm from "@/components/PostForm/PostForm";
import PostList from "@/components/PostList/PostList";

export default {
  components: {
    PostList, PostForm
  },

  data() {
    return {
      posts: [
        {id: 1, title: "JavaScript", body: "Описание поста"},
        {id: 2, title: "JavaScript 2", body: "Описание поста 2"},
        {id: 3, title: "JavaScript 3", body: "Описание поста 3"},
      ],
    }
  },
  methods: {
    createPost(post) {
      this.posts.push(post); 
    },
  }
};
</script>