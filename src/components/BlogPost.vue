<template>
    <div>
        <h2 class="blogpost-title">{{title}}</h2>
        <h3 class="blogpost-author">{{author}}</h3>
        <p class="blogpost-body">{{body}}</p>
    </div>
</template>


<script>
export default {
    name: "BlogPost",
    data() {
        return {
            title: "Blogpost Title",
            author: "John Doe",
            body: "Hello!"
        }
    },
    mounted() {
      
  }
}
</script>
