<!-- eslint-disable -->
<template>
  <div class="post">
    <div><strong>Название:</strong>{{ post.title }}</div>
    <div><strong>Описание:</strong>{{ post.body }}</div>
  </div>
</template>
<!-- eslint-disable -->
<style lang='scss' src="./post-item.scss" scoped></style>
<!-- eslint-disable -->
<script>
export default {
  props: {
    post: {
      type: Object,
      required: true,
    }
  }
}
</script>