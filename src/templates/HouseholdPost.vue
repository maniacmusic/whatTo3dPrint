<template>
  <Layout>
    <div class="project">
      <div class="container">
        <div class="project-header">
          <h1 class="text-3xl" v-html="$page.post.title" />

          <a
            :href="$page.post.download_link"
            target="_blank"
            class="text-2xl rounded-lg border-2 border-black p-5 mt-8 mx-2"
            >Download</a
          >

          <div class="project-info">
            <g-image
              :src="$page.post.thumbnail"
              :alt="$page.post.title"
              class="thumbnail"
            />
            <div class="categories-container">
              <div class="categories">
                <span class="label">Categories</span>
                <span
                  class="category"
                  v-for="(category, index) in $page.post.categories"
                  :key="index"
                  v-text="category"
                />
              </div>
            </div>

            <div class="year-container">
              <span class="label">Year</span>
              <div v-html="$page.post.date" />
            </div>
          </div>
        </div>
        <div v-html="$page.post.content" class="content" />
      </div>
    </div>
  </Layout>
</template>

<page-query>
query HouseholdPost ($path: String!) {
  post: householdPost (path: $path) {
    title
    date (format: "YYYY")
    content
    download_link
    source_link
    author
    author_link
    thumbnail (quality: 90)
  }
}
</page-query>


<script>
export default {
  metaInfo() {
    return {
      title: this.$page.post.title,
    };
  },
};
</script>

