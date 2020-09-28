<template>
  <div>
    <div>
      <div class="uk-position-relative">
        <img
          src="https://www.yslbeta.com/article/wp-content/uploads/2020/09/Free-People-Well-Traveled-241906ce.jpeg"
          alt
        />
        <div class="uk-position-top">
          <TheHeader />
        </div>
      </div>

      <div id="posts">
        <PostPreview
          v-for="post in posts"
          :key="post.id"
          :title="post.title"
          :excerpt="post.previewText"
          :thumbnailImage="post.thumbnailUrl"
          :id="post.id"
        />
      </div>
    </div>
  </div>
</template>

<script>
import TheHeader from '@/components/TheHeader/TheHeader'
import PostPreview from '@/components/Blog/PostPreview'

export default {
  components: {
    TheHeader,
    PostPreview
  },

  data() {
    return {
      posts: [
        {
          title: 'This is Title One',
          previewText:
            'Lorem another sentence about this long. Maybe longer, said again.',
          thumbnailUrl:
            'https://uploads-ssl.webflow.com/5f0cb248a836dd6c0e0b9d77/5f0cb248a836dd2e7b0bab6c_2%20Rolling-Stones-Tie-Dye-Tee-9a2eb1e8.jpeg',
          id: 'post-one'
        },

        {
          title: 'This is Title Two',
          previewText:
            'Lorem another sentence about this long. Maybe longer, said again.',
          thumbnailUrl:
            'https://uploads-ssl.webflow.com/5f0cb248a836dd6c0e0b9d77/5f0cb248a836dd6d7d0bab5a_MTP8407_40_1000x1500.jpg',
          id: 'post-two'
        }
      ]
    }
  }
}
</script>

<style scoped>
#posts {
  padding-top: 2rem;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
@media (min-width: 35rem) {
  #posts {
    flex-direction: row;
  }
}
</style>
