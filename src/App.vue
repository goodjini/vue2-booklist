<template>
  <div id="app" class="black-b">
    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/book">BookList</router-link> |
      <router-link to="/item/1">Item</router-link> |
      <router-link to="/user">User</router-link>
    </nav>
    <div class="blue-b">
      <router-view />
    </div>
      <router-view name="sub"/>
  </div>
</template>

<style>
#app {
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

.black-b {
  border: 1px solid black;
}
</style>
