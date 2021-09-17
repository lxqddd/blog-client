<template>
  <Layout>
    <!-- Page Header -->
    <header
      class="masthead"
      style="background-image: url('/img/post-bg.jpg')"
      :style="{
        backgroundImage: `url('${$page.post.cover.url}')`
      }"
    >
      <div class="overlay"></div>
      <div class="container">
        <div class="row">
          <div class="col-lg-8 col-md-10 mx-auto">
            <div class="post-heading">
              <h1>{{ $page.post.title }}</h1>
              <!-- <h2 class="subheading">Problems look mighty small from 150 miles up</h2> -->
              <span class="meta"
                >Posted on
                <!-- <a href="#">Start Bootstrap</a> -->
                {{ $page.post.created_at }}</span
              >
            </div>
          </div>
        </div>
      </div>
    </header>

    <!-- Post Content -->
    <article>
      <div class="container">
        <div class="row">
          <div class="col-lg-8 col-md-10 mx-auto" v-html="mdToHtml($page.post.content)"></div>
        </div>
      </div>
    </article>
  </Layout>
</template>

<page-query>
query ($id: ID!) {
  post: strapiPost (id: $id) {
    id
    title
    content
    created_at
    cover {
      url
    }
    tags {
      title
    }
  }
}
</page-query>

<script>
import MarkdownIt from 'markdown-it'
const md = new MarkdownIt()
export default {
  name: 'PostPage',
  methods: {
    mdToHtml(mdContent) {
      return md.render(mdContent)
    }
  }
}
</script>

<style></style>
