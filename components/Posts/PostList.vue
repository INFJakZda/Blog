<template>
  <section class="post-list">
    <PostPreview
      id="1"
      :is-admin="isAdmin"
      thumbnail="https://cloud.oracle.com/opc/images/trends-hightech-5.jpg"
      title="hello"
      previewText="hello text"/>
    <PostPreview
      id="2"
      :is-admin="isAdmin"
      thumbnail="https://cloud.oracle.com/opc/images/trends-hightech-5.jpg"
      title="hello2"
      previewText="hello2 text"/>
    <PostPreview
      id="3"
      :is-admin="isAdmin"
      thumbnail="https://cloud.oracle.com/opc/images/trends-hightech-5.jpg"
      title="hello3"
      previewText="hello3 text"/>
  </section>
</template>

<script>
import PostPreview from '@/components/Posts/PostPreview';

export default {
  components: {
    PostPreview
  },
  props: {
    isAdmin: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style scoped>
.post-list {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
</style>
