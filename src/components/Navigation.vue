<template>
  <div class="naviagtion">
    <header class="md-toolbar md-transparent md-elevation-0" md-alignment="centered">
        <div md-aligment="centered" class="md-transparent toolbar-button-set">
          <button data-v-76466055="" type="button" class="md-button brand-logo"><div class="md-button-content"><img src="../assets/logo-inverse.png" alt=""></div></button>          
          <md-button id="tab-home" md-label="Home" :md-ripple="false" class="active" href="#">Home</md-button>
          <md-button id="tab-about" md-label="About Us" :md-ripple="false" :href="url">About Us</md-button>
          <md-button id="tab-team" md-label="Our Team" :md-ripple="false" :href="url">Our Team</md-button>
          <md-button id="tab-pricing" md-label="Pricing" :md-ripple="false" :href="url">Pricing</md-button>           
          <md-button id="tab-pages" md-label="Pages" :md-ripple="false" :href="url">Pages</md-button>
          <md-button id="tab-contact" md-label="Contact Us" :md-ripple="false" :href="url">Contact Us</md-button>
          <md-button class="signin-btn" :md-ripple="false">Sign In</md-button>
        </div>
    </header>
  </div>
</template>

<script>
export default {
  name: 'navigation',
  props: {
    prop1: {
      // foo: bar
    }
  },
  data: function() {
    return {
      url: 'http://www.headwire.com'
    }
  },
  methods: {
    openCategory(categoryId) {
      this.categoryId = categoryId;
      if (!this.categoryId) { return; }
      this.$emit('clicked', this.categoryId);
    }
  },
  beforeMount() {
    // The debounce function receives our function as a parameter
    const debounce = (fn) => {

      // This holds the requestAnimationFrame reference, so we can cancel it if we wish
      let frame;

      // The debounce function returns a new function that can receive a variable number of arguments
      return (...params) => {
        
        // If the frame variable has been defined, clear it now, and queue for next frame
        if (frame) { 
          cancelAnimationFrame(frame);
        }

        // Queue our function call for the next frame
        frame = requestAnimationFrame(() => {
          
          // Call our function and pass any params we received
          fn(...params);
        });

      } 
    };

    // Reads out the scroll position and stores it in the data attribute
    // so we can use it in our stylesheets
    const storeScroll = () => {
      document.documentElement.dataset.scroll = window.scrollY;
    }

    // Listen for new scroll events, here we debounce our `storeScroll` function
    document.addEventListener('scroll', debounce(storeScroll), { passive: true });

    // Update scroll position for first time
    storeScroll();
  }
}
</script>

 