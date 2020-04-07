<template>
  <Layout>
    <div>
      <div v-for="edge in $page.posts.edges" :key="edge.node.id">
        <h2>{{ edge.node.title }}</h2>
        <a v-bind:href="edge.node.path">View Post</a>
      </div>
    </div>
  </Layout>
</template>

<page-query>
query {
  posts: allPost {
    edges {
      node {
        id
        title
        path
      }
    }
  }
}
</page-query>