<template>
  <div class="naviagtion">
    <div class="md-toolbar md-transparent md-elevation-0" md-alignment="centered">
        <md-buttons md-aligment="centered" class="md-transparent">
          <md-button id="tab-home" md-label="Home" :md-ripple="false">Home</md-button>
          <md-button id="tab-about" md-label="About Us" :md-ripple="false">About Us</md-button>
          <md-button id="tab-team" md-label="Our Team" :md-ripple="false">Our Team</md-button>
          <md-button id="tab-pricing" md-label="Pricing" :md-ripple="false">Pricing</md-button>           
          <md-button id="tab-pages" md-label="Pages" :md-ripple="false">Pages</md-button>
          <md-button id="tab-contact" md-label="Contact Us" :md-ripple="false">Contact Us</md-button>
        </md-buttons>
    </div>
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
      categoryId: ''
    }
  },
  methods: {
    openCategory(categoryId) {
      this.categoryId = categoryId;
      if (!this.categoryId) { return; }
      this.$emit('clicked', this.categoryId);
    }
  }
}
</script>
<style lang="scss">
   .md-button-clean {
    background: #fff;
   }
</style>
 