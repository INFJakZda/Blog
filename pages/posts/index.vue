<template>
  <div class="posts-page">
    <PostList :posts="loadedPosts"/>
  </div>
</template>

<script>
import PostList from "@/components/Posts/PostList";

export default {
  components: {
    PostList
  },
  asyncData(context) {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          loadedPosts: [
            {
              id: "1",
              title: "First Post",
              previewText: "Amazing first post !",
              thumbnail:
                "https://cloud.oracle.com/opc/images/trends-hightech-5.jpg"
            },
            {
              id: "2",
              title: "Second Post",
              previewText: "Amazing second post !",
              thumbnail:
                "https://cloud.oracle.com/opc/images/trends-hightech-5.jpg"
            }
          ]
        });
      }, 1500);
    })
      .then(data => {
        return data;
      })
      .catch(e => {
        return new Error();
      });
  }
};
</script>

<style scoped>
.posts-page {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
