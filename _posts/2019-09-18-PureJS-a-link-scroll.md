---
layout:     post
title:      PureJS a Link Scroll
categories: [/category/JSLib]
tags: [/category/JSLib]
---


var scrollDown = document.querySelectorAll('a.scroll-down[href^="#"]');
scrollDown.forEach(anchor => {
    anchor.addEventListener('click', function (e) {
        e.preventDefault();
        document.querySelector(this.getAttribute('href')).scrollIntoView({
            behavior: 'smooth'
        });
    });
});