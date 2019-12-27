<template>
  <div class="services">
    <h4>Our Services</h4>
    <div class="wrapper">
      <div class="box a">A</div>
      <div class="box b">B</div>
      <div class="box c">C</div>
      <div class="box d">D</div>
      <div class="box e">E</div>
      <div class="box f">F</div>
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