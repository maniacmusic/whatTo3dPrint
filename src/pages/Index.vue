<template>
  <Layout>
    <ProjectsGrid :projects="$page.projects.edges" />
    <LatestJournals :journals="$page.journals.edges" class="hidden" />
  </Layout>
</template>

<page-query>
query Posts {
	projects : allProjectPost {
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
import ProjectsGrid from "@/components/ProjectsGrid";
import LatestJournals from "@/components/LatestJournals";

export default {
  components: {
    ProjectsGrid,
    LatestJournals,
  },
};
</script>

<style>
.index-icon {
  width: 100px;
}
</style>