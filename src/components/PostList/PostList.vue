<!-- eslint-disable -->
<template>
  <div>
    <h3>Список пользователей</h3>
    <post-item
      v-for="post in posts"
      :post ="post"
      :key="post.id"
      @remove="$emit('remove', post)"
    />
  </div>
</template>
<!-- eslint-disable -->
<style lang='scss' src="./post-list.scss" scoped></style>
<!-- eslint-disable -->
<script>
import PostItem from "@/components/PostItem/PostItem";

export default {
  components: {PostItem},
  props: {
    posts: {
      type: Array,
      required: true,
    }
  }
}
</script>