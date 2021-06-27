<template>
  <nav>
    <h1>My Vue</h1>
    <ul class="nav-link">
      <li><router-link to="/">Home</router-link></li>
      <li><router-link to="/contacts">Contacts</router-link></li>
      <li>About</li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'Navbar'
}
</script>

<style scoped>
nav {
  background: #333;
  color: #fff;
  text-align: center;
  padding: 10px;

}

a {
  color: #fff;
  text-decoration: none;
  cursor: pointer;
}

nav ul.nav-link {
  display: flex;
  justify-content: space-around;
  align-items: center;
  list-style: none;
  padding: 0;
}
</style>
