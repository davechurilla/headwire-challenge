<template>
 <div>
    <div class="hero-img"><img src="../assets/hero-1.jpg" alt=""></div>
    <div class="hero-copy">
      <h1>Professional Business Consulting</h1>
      <p>Businet provides reliable business planning, management and advisory services backed by years of experience in the industry.</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'hero',
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