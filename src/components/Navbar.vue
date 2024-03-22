<template>
  <nav :class="{ 'hidden': scrolled }">
      <div class="logo">
          <img src="../assets/lb.png" alt="Logo" width="30" height="30">
      </div>
      <ul class="nav-links">
        <li><router-link :to="{path: '/'}">Home</router-link></li>
          <li><a href="#">About</a></li>
          <li><a href="#">Contact</a></li>
          <li><RouterLink :to="{path: '/shop'}">Shop</RouterLink></li>
      </ul>
  </nav>
</template>

<script>
export default {
    name: 'Navbar',
    data() {
        return {
            scrolled: false
        };
    },
    created() {
        window.addEventListener('scroll', this.handleScroll);
    },
    destroyed() {
        window.removeEventListener('scroll', this.handleScroll);
    },
    methods: {
        handleScroll() {
            this.scrolled = window.scrollY > 50; // Change 50 to your desired scroll threshold
        }
    }
}
</script>

<style scoped>
body {
  margin: 0;
  padding: 0;
  font-family: Arial, sans-serif;
}

nav {
  background-color: #FAF3E0;
  color: darkgreen;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 20px;
  top: 0;
  position: fixed;
  width: 100%;
  z-index: 1;
  transition: transform 0.3s ease; /* Smooth transition */
}

.logo {
  font-weight: bold;
  font-size: 1.25rem;
}

.nav-links {
  list-style-type: none;
  margin: 0;
  padding: 0;
  display: flex;
}

.nav-links li {
  margin-right: 15px;
}

.nav-links li:last-child {
  margin-right: 0;
}

.nav-links li a {
  color: darkgreen;
  text-decoration: none;
  padding: 5px 10px;
  border-radius: 25px;
  transition: background-color 0.3s ease;
}

.nav-links li a:hover {
  background-color: darkgreen;
  color: #FAF3E0;
}

.navbar.hidden {
    transform: translateY(-100%); /* Move navbar out of view */
}
</style>
