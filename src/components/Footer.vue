<template>
<footer>
  <div class="footer-content">
    <p>&copy; 2024 Orchid Tahoma Jaya</p>
    <ul class="footer-links">
      <li><a href="#">Privacy Policy</a></li>
      <li><a href="#">Terms of Service</a></li>
      <li><a href="#">Contact Us</a></li>
    </ul>
  </div>
</footer>
</template>

<script>
export default {
    name: 'Footer'
}
</script>

<style scoped>
footer {
  background-color: #FAF3E0;
  color: darkgreen;
  padding: 10px;
  text-align: center;
  /* padding-top: 5rem; */
}

.footer-content {
  max-width: 750px;
  margin: 0 auto;
}

.footer-content p {
  margin: 0;
}

.footer-links {
  list-style-type: none;
  padding: 0;
  margin-top: 5px;
  margin-bottom: 0;
}

.footer-links li {
  display: inline;
  margin-right: 10px;
}

.footer-links li:last-child {
  margin-right: 0;
}

.footer-links li a {
  color: darkgreen;
  text-decoration: none;
}

.footer-links li a:hover {
  text-decoration: underline;
}
</style>