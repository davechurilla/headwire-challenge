<template>
  <div class="faq">
    <ul>
      <li>What am I allowed to do?</li>
      <li>Do you provide any scripts with your templates?</li>
      <li>What do I receive when I order a temmplate from Zemez?</li>
      <li>In what formats are your teamplates available?</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'faq',
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