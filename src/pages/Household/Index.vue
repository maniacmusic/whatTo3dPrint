<template>
  <Layout>
    <ProjectsGrid :household="$page.posts.edges" />
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
        thumbnail (width: 350, height: 350, quality: 75)
        path
      }
    }
  }
}
</page-query>

<script>
import ProjectsGrid from "@/components/ProjectsGrid";

export default {
  components: {
    ProjectsGrid,
  },
};
</script>
