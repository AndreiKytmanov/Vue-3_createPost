<template>
  <div v-show="posts.length > 0">
    <h3>Список постов</h3>
    <post-item
      v-for="post in posts"
      :post="post"
      :key="post.id"
      @remove="$emit('remove', post)"
    />
  </div>
  <h2 v-show="posts.length === 0" style="color: red">Список пуст, создайте новый пост</h2>
</template>

<script>
import PostItem from "@/components/PostItem";
export default {
  components: { PostItem },
  props: {
    posts: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style lang="css" scoped></style>
