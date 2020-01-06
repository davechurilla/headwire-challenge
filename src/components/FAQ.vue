<template>
  <div class="faq">
    <ul class="accordion">
      <li class="faq-item active">
        <div class="question">
          <div class="title">What am I allowed to do?</div>
          <button class="caron xbig">&caron;</button></div>
        <div class="clear"></div>
        <div class="answer expanded"><p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</p></div>
      </li>
      <li class="faq-item">
        <div class="question">
        <div class="title">Do you provide any scripts with your templates?</div>
        <button class="caron xbig">&caron;</button></div>
        <div class="clear"></div>
        <div class="answer"><p>Our templates do not include any additional scripts. Newsletter subscriptions, search fields, forums, image galleries (in HTML versions of Flash products) are active. Basic scripts can be easily added at www.zemez.io. If you are not sure that the element you're interested in is active, please contact our Support Chat for clarification.</p></div>
      </li>
      <li class="faq-item">
        <div class="question">
          <div class="title">What do I receive when I order a template from Zemez?</div>
          <button class="caron xbig">&caron;</button></div>
        <div class="clear"></div>
        <div class="answer"><p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</p></div>
      </li>
      <li class="faq-item">
        <div class="question">
          <div class="title">In what formats are your teamplates available?</div>
          <button class="caron xbig">&caron;</button></div>
        <div class="clear"></div>
        <div class="answer"><p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</p></div>
      </li>
    </ul>

  </div>
</template>

<script>
export default {
  name: 'faq',
  mounted() {
    // The following logic drives the accordion functionality, works in conjunction with the CSS trnsition to open and close the panels.
    function faqUpdate(event) {
      // define the current clicked element
      const clickedParent = event.target.parentElement.parentElement

      // clear all styles for expanded active active FAQ
      const faqItems = document.querySelectorAll('.faq-item')
      const answers = document.querySelectorAll('.answer')
      Array.from(faqItems).forEach(function(element) {
        element.classList.remove('active')
      });
      Array.from(answers).forEach(function(element) {
        element.classList.remove('expanded')
        element.removeAttribute('style')
      });          
      // add class to currently clicked target element so CSS is applied to expand the answer and apply styles
      clickedParent.classList.add('active')
      clickedParent.children[2].classList.add('expanded')
      const answerDivHeight = clickedParent.offsetHeight/1.25
      document.getElementsByClassName('expanded')[0].style.height = answerDivHeight + 'px'
    }
    // apply initial styles to first FAQ question and answer to be expanded by default.
    const initAnswer = document.getElementsByClassName('expanded')[0]
    console.log(initAnswer.parentElement.offsetHeight)
    initAnswer.style.height = initAnswer.parentElement.offsetHeight + 'px'

    // define the caron as the click area for expanding the FAQ element
    const faqQuestions = document.getElementsByClassName('caron')
    // add listener to the caron click area so we can then trigger an event handler that will toggle classes
    Array.from(faqQuestions).forEach(function(element) {
      element.addEventListener('click', faqUpdate)
    });   
  }
}
</script>