/* eslint-disable */
<template>
  <div>
    <v-main class="pt-0">
      <home-page></home-page>
      <popular-places></popular-places>
      <excursions-page></excursions-page>
      <feedback-page></feedback-page>
      <blog-page></blog-page>
      <contact-page></contact-page>
    </v-main>
    <foote-page></foote-page>
  </div>
</template>

<script>
import footePage from "../components/Footer";
import homePage from "../components/HomeSection";
import popularPlaces from "@/components/PopularPlaces";
import excursionsPage from "@/components/Excursions";
import feedbackPage from "@/components/Feedback";
import blogPage from "@/components/Blog";
import contactPage from "@/components/Contact";

export default {
  name: "landing",
  components: {
    footePage,
    homePage,
    popularPlaces,
    excursionsPage,
    feedbackPage,
    blogPage,
    contactPage
  },
  data: () => ({
  }),
  mounted() {
    if (this.$router.currentRoute.query.login) {
      this.$store.state.modals.type.login = this.$router.currentRoute.query.login
    }
  },

}
</script>

<style >
.v-btn {
  text-transform: none;
  letter-spacing: 0;
  font-style: normal;
}
.v-tabs:not(.v-tabs--vertical) .v-tab {
  text-transform: none;
  font-weight: bold;
  color: black;
}
</style>
