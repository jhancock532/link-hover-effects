---
layout: code-display
title: Highlight with Mix-Blend-Mode
---

{% highlight scss %}
.link {
  &--highlight-from-left {
    position: relative;
    display: inline-block; //Preventing line break
    //This stops some issues with absolute positioning.
    
    &:after {
      content: "";
      position: absolute;
      left: -4px;
      top: -4px;
      width: 0;
      height: calc(100% + 8px);
      background-color: $color--primary;
      transition: width 0.36s ease-in-out;
      mix-blend-mode: multiply;
    }
    
    &:hover::after, &:focus::after {
      width: calc(100% + 8px);
    }
  }

  &--highlight-from-right {
    position: relative;
    display: inline-block;
    
    &:after {
      content: "";
      position: absolute;
      right: -4px;
      top: -4px;
      width: 0;
      height: calc(100% + 8px);
      background-color: $color--primary;
      transition: width 0.36s ease-in-out;
      mix-blend-mode: multiply;
    }
    
    &:hover::after, &:focus::after {
      width: calc(100% + 8px);
    }
  }

  &--highlight-from-bottom {
    position: relative;
    display: inline-block;

    &:after {
      content: "";
      position: absolute;
      left: -4px;
      bottom: -4px;
      width: calc(100% + 8px);
      height: 0%;
      background-color: $color--primary;
      transition: height 0.36s ease-in-out;
      mix-blend-mode: multiply;
    }
    
    &:hover::after, &:focus::after {
      height: calc(100% + 8px);
    }
  }

  &--highlight-from-top {
    position: relative;
    display: inline-block;
    
    &:after {
      content: "";
      position: absolute;
      left: -4px;
      top: -4px;
      width: calc(100% + 8px);
      height: 0%;
      background-color: $color--primary;
      transition: height 0.36s ease-in-out;
      mix-blend-mode: multiply;
    }
    
    &:hover::after, &:focus::after {
      height: calc(100% + 8px);
    }
  }
}{% endhighlight %}