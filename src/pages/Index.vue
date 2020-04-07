<template>
  <Layout>

    <!-- Learn how to use images here: https://gridsome.org/docs/images -->
    <g-image alt="Example image" src="~/favicon.png" width="135" />

    <h1>Hello, Gridsome!</h1>

    <p>
      Welcome to the starter template. This is the first starting point in your Gridsome site.
    </p>

    <h2>Pages</h2>
    <p>You can create any number of pages you want. All you need to do is just create a new file inside pages directory.</p>

    <p class="home-links">
      <a href="https://gridsome.org/docs/" target="_blank" rel="noopener">Gridsome Docs</a>
      <a href="https://github.com/gridsome/gridsome" target="_blank" rel="noopener">GitHub</a>
    </p>

    <h2>Posts</h2>
    <p>We can create the posts using markdown files.</p>
    <g-link to="/posts">View All Posts</g-link>

  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Hello, world!'
  }
}
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
