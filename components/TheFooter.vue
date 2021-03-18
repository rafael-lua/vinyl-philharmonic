<template>
  <footer class="footer shadow">
    <div class="container footer-content">
      <div class="footer-links">

        <div class="footer-about fullfill footer-link">
          <ul>
            <nuxt-link to="/"><li>About Us</li></nuxt-link>
            <nuxt-link to="/"><li>Privacy Policy</li></nuxt-link>
            <nuxt-link to="/"><li>History</li></nuxt-link>
            <nuxt-link to="/"><li>Location</li></nuxt-link>
            <nuxt-link to="/"><li>Musicians</li></nuxt-link>
          </ul>
        </div>

        <div class="footer-concerts fullfill footer-link">
          <ul>
            <nuxt-link to="/"><li>Tickets and Concerts</li></nuxt-link>
            <nuxt-link to="/"><li>Events</li></nuxt-link>
            <nuxt-link to="/"><li>Live Broadcasts</li></nuxt-link>
            <nuxt-link to="/"><li>Recordings</li></nuxt-link>
            <nuxt-link to="/"><li>News</li></nuxt-link>
          </ul>
        </div>

        <div class="footer-academy fullfill footer-link">
          <ul>
            <nuxt-link to="/"><li>About Academy</li></nuxt-link>
            <nuxt-link to="/"><li>Online Resources</li></nuxt-link>
            <nuxt-link to="/"><li>For Kids</li></nuxt-link>
            <nuxt-link to="/"><li>Teachers</li></nuxt-link>
            <nuxt-link to="/"><li>FAQ & Contact</li></nuxt-link>
          </ul>
        </div>

        <nuxt-link to="/" class="fullfill"><img src="~/assets/logotipo-mini.png" alt="logo"></nuxt-link>
      </div>
      <div class="footer-copy">
        <hr>
        <p>&copy; 2021 - ALL RIGHTS RESERVED.</p>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "TheFooter"
}
</script>

<style>
.footer {
  position: relative;
  height: 300px;
  background-color: white;
  z-index: 10;
  color: var(--primary-color);
}

.footer-content {
  height: 100%;
  padding: 3em 0 1em 0;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.footer-links {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.footer-copy {
  font-size: 0.85em;
  font-weight: 700;
  text-align: center;
}

.footer-link a {
  text-decoration: none;
  color: var(--secondary-color);
  font-weight: 300;
  border-bottom: 1px solid grey;
}

.footer-link a:hover {
  color: var(--primary-color);
  border-bottom: 1px solid black;
  font-weight: 700;
}

.fullfill {
  width: 100%;
  text-align: center;
}

</style>