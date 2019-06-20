<template>
  <div class="container">
    <div>
      <h1 class="title">
        Blogs
      </h1>

      <nuxt-link
        v-for="blog in bloglist"
        :key="blog.date"
        :to="`blog/${blog.slug}`"
        class="button--green"
      >
        {{ blog.name }} - {{ blog.date }}
      </nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  computed: {
    bloglist() {
      return this.$store.state.bloglist
    }
  }
}
</script>
