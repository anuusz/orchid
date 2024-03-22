<template>
  <main id="main">
    <section class="hero">
      <div class="content">
        <h1>Welcome to Our Website</h1>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
        <a href="../views/ShopView.vue" class="btn">Shop Now</a>
      </div>
    </section>
  </main>

  <about id="about">
    <div class="about-card">
      <div class="card-content">
        <div class="card-image">
          <img src="../assets/mainsection.png" alt="About Image">
        </div>
        <div class="card-text">
          <h2>About Us</h2>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
          <p>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
        </div>
      </div>
    </div>
  </about>

  <features id="features">
    <div class="feature-container">
      <div class="feature">
        <div class="feature-image">
          <img src="../assets/about.jpg" alt="Image 1">
        </div>
        <div class="feature-text">
          <h2>Feature 1</h2>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </div>
      </div>
      <div class="feature">
        <div class="feature-image">
          <img src="../assets/about.jpg" alt="Image 2">
        </div>
        <div class="feature-text">
          <h2>Feature 2</h2>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </div>
      </div>
      <div class="feature">
        <div class="feature-image">
          <img src="../assets/about.jpg" alt="Image 3">
        </div>
        <div class="feature-text">
          <h2>Feature 3</h2>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </div>
      </div>
    </div>
  </features>

    <contact id="contact" class="contact-container">
      <div class="contact-card chat">
        <div class="card-content">
          <div class="card-text">
            <h2>Chat with Us</h2>
            <p>Start a conversation with our support team.</p>
            <button class="btn btn-chat">Talk to us now</button>
          </div>
        </div>
      </div>
      <div class="contact-card support">
        <div class="card-content">
          <div class="card-text">
            <h2>Get Support</h2>
            <p>Get assistance with your inquiries or issues.</p>
            <button class="btn btn-support">Talk to Support</button>
          </div>
        </div>
      </div>
  </contact>
</template>

<script>
export default {
  name: 'MainSection'
}
</script>

<style scoped>
#main,
#about,
#features {
  background-color: #FAF3E0
}

main {
  padding-top: 0px;
  background-image: url('../assets/mainsection.png');
  background-size: cover;
  background-position: center;
}

.hero {
  padding: 50px;
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh; 
}

.content {
  max-width: 600px; 
}

.hero h1 {
  margin-bottom: 20px;
}

.hero p {
  margin-bottom: 30px;
}

.btn {
  display: inline-block;
  padding: 10px 20px;
  background-color: green;
  color: #FAF3E0;
  text-decoration: none;
  border-radius: 25px;
}

.btn:hover {
  background-color: darkgreen;
  color: #FAF3E0;
}

/* about */
about {
  background-color: #FAF3E0;
  /* padding: 2.5rem 0; */
}

.about-card {
  background-color: #FAF3E0;
  max-width: 1000px;
  margin: 6.25rem auto;
  overflow: hidden;
  border-radius: 25px;
}

.card-content {
  display: flex;
}

.card-image {
  flex: 1;
}

.card-image img {
  width: 100%;
  height: auto;
}

.card-text {
  flex: 1;
  padding: 20px;
}

.card-text h2 {
  margin-top: 0;
  margin-bottom: 10px;
}

.card-text p {
  margin-bottom: 10px;
}

/* feature */
.feature-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 10rem;
}

.feature {
  flex: 1;
  margin: 0 10px;
  background-color: #FAF3E0;
  border-radius: 25px;
  overflow: hidden;
}

.feature-image {
  text-align: center;
}

.feature-image img {
  max-width: 100%;
  height: auto;
}

.feature-text {
  padding: 20px;
  text-align: center;
}

.feature-text h2 {
  margin-top: 0;
}

.feature-text p {
  margin-bottom: 0;
}

/* contact */
.contact-container {
  display: flex;
  justify-content: space-between;
  margin: 50px 0;
}

.contact-card {
  flex: 1;
  margin: 0 10px;
  position: relative;
}

.contact-card.chat::before,
.contact-card.support::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-size: cover;
  z-index: -2;
  border-radius: 10px;
}

.contact-card.chat::before {
  background-image: url('../assets/about.jpg');
  background-color: red;
  filter: opacity(0.5);
}

.contact-card.support::before {
  background-image: url('../assets/about.jpg');
  background-color: green;
  filter: opacity(0.5);
}


.card-content {
  position: relative;
  z-index: 1;
}

.card-text {
  padding: 20px;
  text-align: left;
}

.card-text h2,
.card-text p {
  margin-top: 0;
  margin-bottom: 10px;
}

.btn-chat {
  font-size: 12px;
  display: inline-block;
  padding: 7.5px 12.5px;
  background-color: red;
  color: #faf3e0;
  text-decoration: none;
  border-radius: 25px;
  border: none;
}

.btn-chat:hover {
  background-color: darkred;
}

.btn-support {
  font-size: 12px;
  display: inline-block;
  padding: 7.5px 12.5px;
  background-color: green;
  color: #faf3e0;
  text-decoration: none;
  border-radius: 25px;
  border: none;
}

.btn-suport:hover {
  background-color: darkgreen;
}
</style>
