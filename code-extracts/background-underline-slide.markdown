---
layout: code-display
title: Background Underline Slide
---

Attribution: This code was largely based on [Colin Horn's](https://codepen.io/colinhorn) "[Gradient Underline Animation](https://codepen.io/colinhorn/pen/YxYYMj)" (licensed under <a href="http://creativecommons.org/licenses/by/4.0" target="_blank">CC BY 4.0</a>). I have made several changes in my derivation to make the underscore go from right to left. I also experimented with a double gradient background approach [here](https://codepen.io/jhancock532/pen/poyEegg), however I gave up on it as it gives the link a non-transparent background.

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

### License

Copyright (c) 2020 by Colin Horn [Source](https://codepen.io/colinhorn/pen/YxYYMj)

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.