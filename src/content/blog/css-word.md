---
title: "CSS篇之波浪形文字"
description: "有些官网为了美观，会做一些波浪形动画，下面我们用css来实现一下"
pubDate: "2024 04 11"
heroImage: "/css-word.gif"
---

有些官网为了美观，会做一些波浪形动画，下面我们用 css 来实现一下

## css

```html
<style>
  .wavy span {
      display: inline-block;
      color: rgb(74, 152, 255);
      Font-size: 2em;
      animation: animate 2s ease-in-out infinite;
      animation-delay: calc(0.1s * var(--i));
  }
 
  @keyframes animate {
      0% {
        transform: translateY(0px);
      }
 
      20% {
         transform: translateY(-20px);
      }
 
      40%,
      100% {
          transform: translateY(0px);
      }
    }
</style>
```

#### html 部分

```html
<div class="wavy">
  <span style="--i:1">我</span>
  <span style="--i:2">是</span>
  <span style="--i:3">会</span>
  <span style="--i:4">舞</span>
  <span style="--i:5">动</span>
  <span style="--i:6">的</span>
  <span style="--i:7">文</span>
  <span style="--i:8">字</span>
  <span style="--i:9">啊</span>
  <span style="--i:10">~</span>
</div>
```
