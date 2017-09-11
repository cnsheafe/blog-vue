<template>
  <div class="bloglist">
    <form v-on:submit.prevent="AddPost">
      Title<input type="text" v-model="form.title" /> Author
      <input type="text" v-model="form.author" /> Body
      <input type="text" v-model="form.body" />
      <button type="submit">Add</button>
    </form>
    <ul id="posts">
      {{this.posts}}
    </ul>
  </div>
</template>

<script>

export default {
  name: "BlogList",
  data() {
    return {
      form: {
        body: undefined,
        author: undefined,
        title: undefined
      },
      posts: []
    }
  },
  methods: {
    AddPost(event) {
      event.preventDefault();
      this.posts.push({
        title: this.form.title,
        author: this.form.author,
        body: this.form.body
      });
      this.form.title = undefined;
      this.form.author = undefined;
      this.form.body = undefined;
    }
  },
  // components: {
  //   "BlogPost": require("./BlogPost")
  // }
}
</script>

<style>

</style>
