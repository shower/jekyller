---
layout: slide
theme: bright
title: Shower Jekyller
subtitle: A shower slide generator
badge:
  text: Fork me on Github
  url: https://github.com/shower/jekyller
mathjax: true
---

## Shower Jekyller
{:.cover #Cover}

*A [Jekyll](http://jekyllrb.com) Generator based on [Shower Presentation Engine](http://github.com/shower/shower)*

![](/pictures/cover.jpg)
<!-- photo by John Carey, fiftyfootshadows.net -->

<style>
#Cover h2 {
  margin:30px 0 0;
  color:#FFF;
  text-align:center;
  font-size:70px;
}
#Cover p {
  margin:10px 0 0;
  text-align:center;
  color:#FFF;
  font-style:italic;
  font-size:20px;
}
#Cover p a {
  color:#FFF;
}
</style>


## With Jekyll

It's simple to make Shower slides using Markdown. 

---
    What in the .md file is,

    ## With Jekyll

    It's simple to make Shower slides using Markdown. 


## You can get more

- Name your slides automatically, e.g. `#you-can-get-more`
- Use \\(\LaTeX\\) freely
- Highlight your code
{% highlight css linenos %}
#Cover p a {
  color:#FFF;
}
{% endhighlight %}


## How to get started?

- Create your md file, such as `/_slides/test.md`
- Write down the text
- Run the Jekyll server
- See it on [http://0.0.0.0:4000/slides/test.html](http://0.0.0.0:4000/slides/test.html)


## Examples in `/_examples`

<ul>
  <li><a href="/examples/shower.html">Offical Shower demo</a></li>
  <li>Theme demos<ul>
    {% for example in site.examples %}{% if example.theme %}<li><a href="{{ example.url }}">{{ example.theme | capitalize }}</a></li>{% endif %}{% endfor %}
  </ul></li>
</ul>


## Slides in `/_slides`
<ul>
  {% for slide in site.slides %}{% if slide.title %}<li><a href="{{ slide.url }}">{{ slide.title }}</a></li>{% endif %}{% endfor %}
</ul>

