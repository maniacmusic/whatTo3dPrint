<template>
  <Layout>
    <div class="container">
      <div class="sub-cat">
        <g-link to="/lamps/tablelamps/">Table Lamps</g-link>
      </div>
      <ProjectsGrid :projects="$page.projects.edges" />
    </div>
  </Layout>
</template>

<page-query>
query Posts {
	projects : allProjectPost(filter: { categories: { contains: ["lamps"] }}) {
    edges {
      node {
        id
        date (format: "YYYY")
        title
        categories
        thumbnail (quality: 90)
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
