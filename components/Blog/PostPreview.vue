<template>
  <nuxt-link to="id">
    <article class="post-preview">
      <div class="uk-card uk-card-default uk-card-body ">
        <div class="uk-card-body">
          <h3 class="uk-card-title">{{ title }}</h3>
          <p class="cardtext">{{ excerpt }}</p>
        </div>
      </div>
    </article>
  </nuxt-link>
</template>

<script>
export default {
  props: {
    title: {
      title: {
        type: String,
        required: true
      },
      excerpt: {
        type: String,
        required: true
      },
      thumbnailImage: {
        type: String,
        required: true
      },
      id: {
        type: String,
        required: true
      }
    }
  }
}
</script>

<style scoped>
.post-preview {
  margin: 0.5rem 0.5rem;
}
</style>