<template>
  <div class="bloglist">
    <form action="">
      Title<input type="text" v-model="title" /> Author
      <input type="text" v-model="author" /> Body
      <input type="text" v-model="body" />
      <button @submit="AddPost()">Add</button>
    </form>
    <ul id="posts">
      {{this.posts}}
    </ul>
  </div>
</template>

<script>

export default {
  data() {
    return {
      posts: []
    }
  },
  methods: {
    AddPost() {
      this.posts.push({
        title: this.title,
        author: this.author,
        body: this.body
      });
    }
  },
  mounted() { }
  ,
  components: {
    "BlogPost": require("./BlogPost")
  }
}
</script>

<style>

</style>
