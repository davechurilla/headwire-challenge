<template>
  <div class="faq">
    <ul class="accordion">
      <li class="faq-item active">
        <div class="question">
          <div class="title">What am I allowed to do?</div>
          <div class="caron xbig">&caron;</div></div>
        <div class="clear"></div>
        <div class="answer"><p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</p></div>
      </li>
      <li class="faq-item">
        <div class="question">
        <div class="title">Do you provide any scripts with your templates?</div>
        <div class="caron xbig">&caron;</div></div>
        <div class="clear"></div>
        <div class="answer"><p>Our templates do not include any additional scripts. Newsletter subscriptions, search fields, forums, image galleries (in HTML versions of Flash products) are active. Basic scripts can be easily added at www.zemez.io. If you are not sure that the element you're interested in is active, please contact our Support Chat for clarification.</p></div>
      </li>
      <li class="faq-item">
        <div class="question">
          <div class="title">What do I receive when I order a temmplate from Zemez?</div>
          <div class="caron xbig">&caron;</div></div>
        <div class="clear"></div>
        <div class="answer"><p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</p></div>
      </li>
      <li class="faq-item">
        <div class="question">
          <div class="title">In what formats are your teamplates available?</div>
          <div class="caron xbig">&caron;</div></div>
        <div class="clear"></div>
        <div class="answer"><p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</p></div>
      </li>
    </ul>

  </div>
</template>

<script>
// const faqItems = document.querySelectorAll('.faq-item')
// const faqQuestions = document.querySelectorAll('.faq-item .question')
// faqQuestions.addEventListener('click', faqUpdate);

export default {
  name: 'faq',
  mounted() {
    // The following logic drives the accordion functionality, works in conjunction with the CSS trnsition to open and close the panels.
    function faqUpdate(event) {
      const faqItems = document.querySelectorAll('.faq-item')
      Array.from(faqItems).forEach(function(element) {
        element.classList.remove('active')
      });  
      const clickedParent = event.target.parentElement.parentElement
      clickedParent.classList.add('active')
    }
    const faqQuestions = document.getElementsByClassName('question')

    Array.from(faqQuestions).forEach(function(element) {
      element.addEventListener('click', faqUpdate)
    });   
  }
}
</script>