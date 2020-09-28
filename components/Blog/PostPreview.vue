<template>
  <nuxt-link to="id">
    <article class="post-preview">
      <div class="uk-tile uk-tile-default ">
        <div>
          <h3>{{ title }}</h3>
          <p>{{ excerpt }}</p>
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

.uk-tile {
  border: 2px solid #999999;
}
.uk-tile p {
  font-size: 1rem;
  line-height: normal;
  color: black;
}

.uk-tile h3 {
  font-family: 'Georgia', Georgia, serif;
  font-size: 0.7rem;
  text-transform: uppercase;
  letter-spacing: 3px;
  line-height: normal;
  color: #999999;
}
</style>