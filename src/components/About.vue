<template>
  <div class="about-content">
    <div class="about-img"><img src="../assets/stock-1.jpg" alt="Team Image"/></div>
    <div class="about-copy">
      <md-button class="about-label label" md-label="Our Services" :md-ripple="false" disabled>About Businet</md-button>
      <h2 class="headline">A Few Words About Us</h2>
      <div class="copy">
        <p>Our consulting company is a leading firm of business managers and advisors with offices across the USA. We aim to provide you:</p>
        <ul>
          <li>Quality research & analysis</li>
          <li>Business advisory experience</li>
          <li>Reliable company management</li>
        </ul>        
      </div>
      <md-button class="md-raised about-btn white" :md-ripple="false">Read more</md-button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'about'
}
</script>