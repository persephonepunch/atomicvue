<template>
  <div>
    <header class="main-header">
      <nav class="main-nav">
        <div class="uk-navbar-left">
          <ul class="uk-navbar-nav">
            <nuxt-link to="/" tag="li"><a>Home</a></nuxt-link>
            <nuxt-link to="/about" tag="li"><a>About</a></nuxt-link>
          </ul>
        </div>
      </nav>
    </header>
  </div>
</template>

<script>
export default {}
</script>

<style>
.main-header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
}

.uk-navbar-nav.nuxt-link-exact-active a {
  color: #06c4d1;
}
</style>