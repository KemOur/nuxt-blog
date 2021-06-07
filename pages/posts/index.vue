<template>
  <div class="container">
<!--
      <div  v-if="posts.length">
      <ul v-for="post of posts " v-key="post.id">
        <nuxt-link :to="{ path : `/posts/${post.id}`, params : { id: post.id }}">{{ post.title }}</nuxt-link>
      </ul>
      </div>
      <p v-else > No posts.</p>
    </div>
-->
    <div class="my-3 p-3 bg-body rounded shadow-sm">
      <h6 class="border-bottom pb-2 mb-0">Tous les publications</h6>

      <div  v-if="posts.length">
        <ul v-for="post of posts " v-key="post.id">

        <div class="d-flex text-muted pt-3">
        <svg class="bd-placeholder-img flex-shrink-0 me-2 rounded" width="32" height="32" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="Placeholder: 32x32" preserveAspectRatio="xMidYMid slice" focusable="false">
          <title>Placeholder</title><rect width="100%" height="100%" fill="#007bff"></rect><text x="50%" y="50%" fill="#007bff" dy=".3em">32x32</text></svg>
        <div class="pb-3 mb-0 small lh-sm border-bottom w-100">
          <div class="d-flex justify-content-between">
            <strong class="text-gray-dark">
              <nuxt-link :to="{ path : `/posts/${post.id}`, params : { id: post.id }}" style="font-size: 2vw">{{ post.title }}</nuxt-link>
            </strong>
          </div>
        </div>
      </div>
        </ul>
      </div>
        <p v-else > No posts.</p>

      <small class="d-block text-end mt-3">
        <nuxt-link to="/">Retourner à l'accueil</nuxt-link>
      </small>
    </div>
  </div>
</template>

<script>
  export default  {
    data() {
      return {
        posts: []
      }
    },
    async asyncData({ params, $axios }){
      const posts = await $axios.$get("https://jsonplaceholder.typicode.com/posts");
      return { posts }
    }
  }
</script>
