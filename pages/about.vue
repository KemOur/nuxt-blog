<template>
  <div class="container">
    <div>
      <Logo />
      <h1 class="title" style="font-size: 3vw"> Welcome to Junior-Blog </h1>
      <div>
        <template>
          <nuxt-link to="/">Retourner à l'accueil</nuxt-link>
          <small>Made with ❤️ in Paris</small>
        </template>
      </div>
      <div class="links">
      </div>
    </div>
  </div>
</template>

<script>
  export default {}
</script>

<style>
  .container {
    margin: 0 auto;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
  }

  .title {
    font-family:
      'Quicksand',
      'Source Sans Pro',
      -apple-system,
      BlinkMacSystemFont,
      'Segoe UI',
      Roboto,
      'Helvetica Neue',
      Arial,
      sans-serif;
    display: block;
    font-weight: 300;
    font-size: 100px;
    color: #35495e;
    letter-spacing: 1px;
  }

  .subtitle {
    font-weight: 300;
    font-size: 42px;
    color: #526488;
    word-spacing: 5px;
    padding-bottom: 15px;
  }

  .links {
    padding-top: 15px;
  }
</style>
