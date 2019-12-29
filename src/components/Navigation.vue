<template>
  <div class="naviagtion">
    <header class="md-toolbar md-transparent md-elevation-0" md-alignment="centered">
        <div md-aligment="centered" class="md-transparent toolbar-button-set">
          <md-button id="tab-home" md-label="Home" :md-ripple="false" href="#">Home</md-button>
          <md-button id="tab-about" md-label="About Us" :md-ripple="false" :href="url">About Us</md-button>
          <md-button id="tab-team" md-label="Our Team" :md-ripple="false" :href="url">Our Team</md-button>
          <md-button id="tab-pricing" md-label="Pricing" :md-ripple="false" :href="url">Pricing</md-button>           
          <md-button id="tab-pages" md-label="Pages" :md-ripple="false" :href="url">Pages</md-button>
          <md-button id="tab-contact" md-label="Contact Us" :md-ripple="false" :href="url">Contact Us</md-button>
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
  mounted() {
    document.addEventListener('scroll', () => {
    document.documentElement.dataset.scroll = window.scrollY;
    });
  }
}
</script>
<style lang="scss">
   .md-button-clean {
    background: #fff;
   }
</style>
 