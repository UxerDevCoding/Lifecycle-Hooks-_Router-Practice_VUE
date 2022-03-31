<template>
  <div>
    <router-link :to="{ name: 'home' }">List Page</router-link>
    <router-link :to="{ name: 'pokemon-id', params: { id: 2 } }"
      >Detail Page</router-link
    >
    <router-link :to="{ name: 'about' }">About Page</router-link>
  </div>
</template>

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