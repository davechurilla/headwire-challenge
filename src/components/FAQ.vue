<template>
  <div class="faq">
    <ul class="accordion">
      <li class="accordion-item active">
        <div class="question"><h4>What am I allowed to do?</h4><span class="caron xbig">&caron;</span></div>
        <div class="clear"></div>
        <div class="answer"><p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</p></div>
      </li>
      <li class="accordion-item">
        <div class="question"><h4>Do you provide any scripts with your templates?</h4><span class="caron xbig">&caron;</span></div>
        <div class="clear"></div>
        <div class="answer"><p>Our templates do not include any additional scripts. Newsletter subscriptions, search fields, forums, image galleries (in HTML versions of Flash products) are active. Basic scripts can be easily added at www.zemez.io. If you are not sure that the element you're interested in is active, please contact our Support Chat for clarification.</p></div>
      </li>
      <li class="accordion-item">
        <div class="question"><h4>What do I receive when I order a temmplate from Zemez?</h4><span class="caron xbig">&caron;</span></div>
        <div class="clear"></div>
        <div class="answer"><p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</p></div>
      </li>
      <li class="accordion-item">
        <div class="question"><h4>In what formats are your teamplates available?</h4><span class="caron xbig">&caron;</span></div>
        <div class="clear"></div>
        <div class="answer"><p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</p></div>
      </li>
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