---
layout: slide-deck
title: "Code, meet English"
desc: "An activity to practice converting interactions into English and really trying to break each step into pieces."

slides:
  - type: super-big-text
    content: |
      **Code, meet English**

  - content: |
      ## What & why

      Writing out coding problems in basic English before code helps put our brains in the right mindset.

      We then have a readable roadmap of what code needs to be written and where to write it.

      **Writing code and program flow in English is the first step to writing actual code.**

  - content: |
      ## Set up

      1. Form into pairs
      2. [Print & cut these code snippets](https://assets.learn-the-web.algonquindesign.ca/workshops/think-like-a-programmer/code-meet-english-lines-of-code.zip)
      3. You’ll be shown a Javascript interaction
      4. Write out the code you’d need—in English
      5. Piece together the code snippets to match

      **Don’t look ahead—the answers are in here!**

  - type: figure
    image: "circle-move.gif"
    caption: "**Circle mover**—think about what CSS properties to change"

  - content: |
      ## Circle mover in English

      1. **When the button is clicked:**
          - Get the current `left` CSS coordinate of the circle
          - Add `10px` to the current left
          - Change the circle’s `left` to the new one

  - type: code
    js: |
      $('.btn').on('click', function () {
        var oldLeft = $('.ball').offset().left;
        var newLeft = oldLeft + 10;
        $('.ball').css('left', newLeft);
      });

  - type: figure
    image: "bubble-pop.gif"
    caption: "**Bubble popper**—think about CSS transitions"

  - content: |
      ## Bubble popper in English

      1. **When a circle is clicked:**
          - Add a class to the circle
          - The class causes a transition to trigger,
            <br>hiding the circle

  - type: code
    js: |
      $('.bubble').on('click', function () {
        $(this).addClass('fade-away');
      });

  - type: figure
    image: "circle-bounce.gif"
    caption: "**Circle bouncer**—think about CSS animations"

  - content: |
      ## Circle bouncer in English

      1. **When the button is clicked:**
          - Add a class to the circle
          - The class causes and animation to trigger,
            <br>bouncing the circle

  - type: code
    js: |
      $('.btn').on('click', function () {
        $(this).addClass('bounce');
      });

  - type: figure
    video: "https://assets.learn-the-web.algonquindesign.ca/workshops/think-like-a-programmer/carousel.mp4"
    caption: "**Carousel**—break it down, one at a time"

  - content: |
      ## Carousel in English

      1. **When the 1st button is clicked:**
          - Hide all the slides
          - Show the first slide

      *Repeated 5 times…*

  - type: code
    js: |
      var hideAllSlides = function () {
        $('.slide-1').css('display', 'none');
        $('.slide-2').css('display', 'none');
        $('.slide-3').css('display', 'none');
        $('.slide-4').css('display', 'none');
        $('.slide-5').css('display', 'none');
      };

      $('.btn-1').on('click', function () {
        hideAllSlides();
        $('.slide-1').css('display', 'block');
      });

      /* Repeat the 4 lines above 4 times for each different button/slide combo… */

  - content: |
      ## Don’t Repeat Yourself

      *DRY:* A tenet of programming.

      - In the carousel are there repeating patterns in the code?
      - Can we do anything to improve them?
      - How can we reduce the the duplicated lines of code?

---
