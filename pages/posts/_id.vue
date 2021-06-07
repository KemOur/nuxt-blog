<template>

  <div class="container">
    <div class="bg-light p-5 rounded">
      <h1 style="font-size: 3vw">{{post.title}}</h1>
      <p class="lead" style="font-size: 3vw"> {{post.body}} </p>
      <nuxt-link to="/posts">Publications</nuxt-link>
    </div>
  </div>


</template>

<script>
  export default  {
    data() {
      return {
        post: {}
      }
    },
    async asyncData({ params, $axios }){
      const post = await $axios.$get(`https://jsonplaceholder.typicode.com/posts/${params.id}`);
      return { post }
    }
  }
</script>
