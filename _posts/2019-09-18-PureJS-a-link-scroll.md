---
layout:     post
title:      PureJS a Link Scroll
categories: [Lib]
permalink: '/Lib/Javascript'
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