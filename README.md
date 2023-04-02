# Multipage Website Final Project Frontend Developer Course Progate Indonesia 

Project Multipage Website ini adalah project akhir HTML&CSS serta Javascript DOM dari [Frontend Developer Course Learning Path Progate Indonesia](https://progate.com/paths/frontend). Dibangun dengan menslicing design dari figma menjadi sebuah multipage website    

## Table of contents

- [Overview](#overview)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)

## Overview

### Screenshot

![Proyek Akhir HTML CSS Progate - Google Chrome 2023-04-02 11-29-54 (2)](https://user-images.githubusercontent.com/106422023/229332696-bab16719-bb2a-4757-a39b-3c99d511b04f.gif)

### Links

- Live Site URL: [live site URL here](https://eloquent-tarsier-5913bf.netlify.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid

### What I learned

- Cara membuat accordion dengan javascript

```js
const accordion = document.getElementsByClassName("accordion");

for (let i = 0; i < accordion.length; i++) {
  accordion[i].addEventListener("click", function () {
    const panel = this.nextElementSibling;

    if (panel.style.display === "block") {
      panel.style.display = "none";
    } else {
      panel.style.display = "block";
    }
  });
}
```

- Membuat css animation scroll dengan javascript

```css
.reveal {
  position: relative;
  opacity: 0;
}
.reveal.active {
  opacity: 1;
}
.active.fade-bottom {
  animation: fade-bottom 0.7s ease-in;
}
.active.fade-left {
  animation: fade-left 0.7s ease-in;
}
.active.fade-right {
  animation: fade-right 0.7s ease-in;
}

@keyframes fade-bottom {
  0% {
    transform: translateY(50px);
    opacity: 0;
  }
  100% {
    transform: translateY(0);
    opacity: 1;
  }
}
@keyframes fade-left {
  0% {
    transform: translateX(-50px);
    opacity: 0;
  }
  100% {
    transform: translateX(0);
    opacity: 1;
  }
}
@keyframes fade-right {
  0% {
    transform: translateX(50px);
    opacity: 0;
  }
  100% {
    transform: translateX(0);
    opacity: 1;
  }
}
```

```js
function reveal() {
  var reveals = document.querySelectorAll(".reveal");

  for (var i = 0; i < reveals.length; i++) {
    var windowHeight = window.innerHeight;
    var elementTop = reveals[i].getBoundingClientRect().top;
    var elementVisible = 200;

    if (elementTop < windowHeight - elementVisible) {
      reveals[i].classList.add("active");
    } else {
      reveals[i].classList.remove("active");
    }
  }
}
```

### Useful resources

- [How to Create CSS Animations on Scroll](https://alvarotrigo.com/blog/css-animations-scroll/) - Sumber artikel ini saya pakai untuk belajar bagaimana cara membuat css animation scroll dengan javascript
