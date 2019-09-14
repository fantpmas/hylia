---
title: 'Translatable text in CSS'
date: '2015-06-26'
tags:
  - tech


---

Seriously folks, don't put translatable text in CSS files. I really hate that.

```css
p.tip 
{
Letter-spacing: normal;
padding-left: 0.8em;
padding-right: 0.8em;
padding-bottom: 0.3em;
padding-top: 0.3em;
border-bottom-style: Solid;
border-bottom-width: 1px;
border-top-style: Solid;
border-top-width: 1px;
border-bottom: solid 1px;
mc-auto-number-format: '{b}Tip: {/b}';
border-bottom-color: #0064b9;
border-top-color: #0064b9;
margin-left: 0;
margin-bottom: 0;
margin-top: 0
}
```