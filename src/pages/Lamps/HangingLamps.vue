<template>
  <Layout>
    <ProjectsGrid :projects="$page.projects.edges" />
  </Layout>
</template>

<page-query>
query Posts {
	projects : allProjectPost(filter: { categories: { contains: ["hanglamp"] }}) {
    edges {
      node {
        id
        date (format: "YYYY")
        title
        categories
        thumbnail (width: 350, height: 350, quality: 90)
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
