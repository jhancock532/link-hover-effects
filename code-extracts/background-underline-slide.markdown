---
layout: code-display
title: Background Underline Slide
---

This code was largely based on [Colin Horn's](https://codepen.io/colinhorn) [Gradient Underline Animation](https://codepen.io/colinhorn/pen/YxYYMj). I also experimented with a double gradient background approach [here](https://codepen.io/jhancock532/pen/poyEegg), however it gives the link a non-transparent background.

{% highlight scss %}
.link {
  &--background-underline-from-right {
    padding-bottom: 2px;
    background-image: linear-gradient(to right, transparent 0%, transparent 50%, 
                                      $color--secondary 50%, $color--secondary 100%);
    background-size: 200% 4px;
    background-repeat: no-repeat;
    background-position: left bottom;
    transition: background-position 360ms ease-in-out;

    &:hover {
      background-position: right bottom;
    }
  }

  &--background-underline-from-left {
    padding-bottom: 2px;
    background-image: linear-gradient($color--secondary, $color--secondary);
    background-size: 0% 4px;
    background-repeat: no-repeat;
    background-position: left bottom;
    transition: background-size 360ms ease-in-out;

    &:hover {
      background-size: 100% 4px;
    }
  }

  &--background-underline-from-strikethrough {
    padding-bottom: 1px;
    background-image: linear-gradient($color--secondary, $color--secondary);
    background-size: 100% 3px;
    background-repeat: no-repeat;
    background-position: left 58%;
    transition: background-position 360ms ease-in-out;

    &:hover {
      background-position: left bottom;
    }
  }
}{% endhighlight %}