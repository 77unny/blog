---
layout:     post
title:      PureJS a Link Scroll
categories: [Lib]
---



### Javascript A Tag href(link) Scroll Event 

> A태그에 걸린 href ID 값을 이용하여 스크롤 이벤트 

##### Pure javascript

```javascript
var scrollDown = document.querySelectorAll('a.scroll-down[href^="#"]');
scrollDown.forEach(anchor => {
    anchor.addEventListener('click', function (e) {
        e.preventDefault();
        document.querySelector(this.getAttribute('href')).scrollIntoView({
            behavior: 'smooth'
        });
    });
});
```



##### for jQuery

```javascript
$(document).on('click', 'a[href^="#"]', function (event) {
    event.preventDefault();

    $('html, body').animate({
        scrollTop: $($.attr(this, 'href')).offset().top
    }, 500);
});
```

