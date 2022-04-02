<template>
  <div>
    <!-- <router-link :to="{ name: 'home' }">List Page</router-link>
    <router-link :to="{ name: 'pokemon-id', params: { id: 2 } }"
      >Detail Page</router-link
    >
    <router-link :to="{ name: 'about' }">About Page</router-link> -->

    <CustomLink v-for="link in links" :key="link.to" :link="link" />
  </div>
</template>

<script>
import { defineAsyncComponent } from "vue";

export default {
  data() {
    return {
      links: [
        { to: "pokemon-home", name: "home" },
        { to: "pokemon-id", name: "pokemon-id", id: 151 },
        { to: "pokemon-about", name: "about" },

        { to: "dbz-characters", name: "Personajes" },
        { to: "dbz-about", name: "DBZ-About" },

        { to: "https://google.com", name: "Google" },
      ],
    };
  },
  components: {
    CustomLink: defineAsyncComponent(() => import("./CustomLink.vue")),
  },
};
</script>

<style scoped>
div {
  padding: 30px 30px;
}

a {
  font-family: "Lucida Sans", "Lucida Sans Regular", "Lucida Grande",
    "Lucida Sans Unicode", Geneva, Verdana, sans-serif;
  color: rgb(76, 76, 80);
  font-size: 18px;
  font-weight: bold;
  margin: 0 20px;
}

a.router-link-exact-active {
  color: rgb(68, 156, 127);
}
</style>
