<template>
  <div class="services">
  <md-button class="services-label" md-label="Our Services" :md-ripple="false" disabled>Our Services</md-button>
    <h2>What We Do</h2>
    <div class="wrapper service-grid">
      <div class="box a">
          <div class="service-img"><img src="../assets/service_analysis.png" alt="Market Analysis"/></div>
          <h3>Market Analysis</h3>
          <p>We support your business with fact-based market research.</p>
      </div>
      <div class="box b">
        <div class="service-img"><img src="../assets/service_funds.png" alt="Funds Management"/></div>
        <h3>Funds Management</h3>
        <p>Allowing you to successfully deal with your company's funds.</p>
      </div>
      <div class="box c">
        <div class="service-img"><img src="../assets/service_marketing.png" alt="PR & Marketing"/></div>
        <h3>PR & Marketing</h3>
        <p>Helping clients expand awareness and manage their reputation.</p>
      </div>
      <div class="box d">
        <div class="service-img"><img src="../assets/service_bizplan.png" alt="Business Planning"/></div>
        <h3>Business Planning</h3>
        <p>Creating an efficient business plan designed to fit your company.</p>
      </div>
      <div class="box e">
        <div class="service-img"><img src="../assets/service_audit.png" alt="Audit"/></div>
        <h3>Audit</h3>
        <p>Deep and detailed investigation of your company's activity.</p>
      </div>
      <div class="box f">
        <div class="service-img"><img src="../assets/service_consulting.png" alt="Consulting"/></div>
        <h3>Consulting</h3>
        <p>Focusing on our clients' most critical issues and opportunities.</p>
      </div>
    </div>      
  </div>

</template>

<script>
export default {
  name: 'services',
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