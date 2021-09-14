<template>
  <Layout>
    <!-- Page Header -->
    <!-- <header class="masthead" style="background-image: url('/img/home-bg.jpg')">
      <div class="overlay"></div>
      <div class="container">
        <div class="row">
          <div class="col-lg-8 col-md-10 mx-auto">
            <div class="site-heading">
              <h1># {{ $page.tag.title }}</h1>
            </div>
          </div>
        </div>
      </div>
    </header> -->

    <!-- Main Content -->
    <!-- <div class="container">
      <div class="row">
        <div class="col-lg-8 col-md-10 mx-auto">
          <div v-for="post in $page.tag.posts" :key="post.id" class="post-preview">
            <g-link :to="`/post/${post.id}`">
              <h2 class="post-title">
               {{ post.title }}
              </h2>
            </g-link>
            <p class="post-meta">
              Posted on
              {{post.created_at}}
            </p>
            <hr>
          </div>
        </div>
      </div>
    </div> -->
  </Layout>
</template>

<script>
export default {
  name: 'TagPage'
}
</script>

<style></style>
