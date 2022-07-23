<template>
<div class="box">
  <nav>
    <router-link to="/hello/home">Home</router-link> |
    <router-link to="/hello/about">About</router-link> |
    <router-link to="/hello/world">HelloWorld</router-link>
    <br/><br/>
<router-link to="/">BACK</router-link>
  </nav>
  <router-view/>
</div>

</template>


<style scoped>
.box {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
