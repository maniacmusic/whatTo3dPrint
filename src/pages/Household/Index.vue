<template>
  <Layout>
    <div class="grid grid-cols-1 md:grid-cols-3 xl:grid-cols-4 gap-4">
      <div
        class="project"
        v-for="item in $page.posts.edges"
        :key="item.node.id"
      >
        <g-link :to="item.node.path" class="project-link">
          <g-image
            :src="item.node.thumbnail"
            :alt="item.node.title"
            class="thumbnail rounded"
          />
          <h3 class="project-title">{{ item.node.title }}</h3>
        </g-link>
      </div>
    </div>
  </Layout>
</template>

<page-query>
query Household {
	posts: allHouseholdPost {
    edges {
      node {
        id
        date (format: "YYYY")
        title
        categories
        thumbnail (width: 350, height: 350, quality: 75)
        path
      }
    }
  }
}
</page-query>