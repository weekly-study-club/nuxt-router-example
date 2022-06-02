<template>
  <v-app>
    <v-app-bar
      app
    >
      <v-btn
        text
        to="/"
      >메인 페이지</v-btn>
      <v-btn
        text
        to="/sub1"
      >서브 1</v-btn>
      <v-btn
        text
        to="/sub2"
      >서브 2</v-btn>
      <v-spacer></v-spacer>
      <div
        v-if="isSubOnePage"
        class="text"
      >
        서브1 페이지에 있어요
      </div>
    </v-app-bar>
    <v-main>
      <nuxt></nuxt>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  computed: {
    isSubOnePage() {
      return this.$route.path.includes('/sub1');
    },
  },
};
</script>
