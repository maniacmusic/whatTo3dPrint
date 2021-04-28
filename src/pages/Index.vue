<template>
  <Layout>
    <div class="container">
      <Hero />
      <div class="categories">
        <div class="category"><g-link to="/tools/">Tools</g-link></div>
        <div class="category"><g-link to="/lamps/">Lamps</g-link></div>
      </div>
      <ProjectsGrid :projects="$page.projects.edges" />
    </div>
    <LatestJournals :journals="$page.journals.edges" />
  </Layout>
</template>

<page-query>
query Posts {
	projects : allProjectPost(filter: { categories: { contains: ["pink"] }}) {
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
  },
  journals: allJournalPost (perPage: 4) {
    edges {
      node {
        id
        path
        title
      }
    }
  }
}
</page-query>

<script>
import Hero from "@/components/Hero";
import ProjectsGrid from "@/components/ProjectsGrid";
import LatestJournals from "@/components/LatestJournals";

export default {
  components: {
    Hero,
    ProjectsGrid,
    LatestJournals,
  },
};
</script>
