<template>
  <Layout>
    <div>
      <h1 v-html="$page.post.title" />
      <div v-html="$page.post.content" />
    </div>  
  </Layout>
</template>

<page-query>
query ($path: String!) {
  post(path: $path) {
    title
    content
  }
}
</page-query>