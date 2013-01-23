{% capture theme %}{% if page.theme %}{{ page.theme }}{% else %}{{ site.default_theme }}{% endif %}{% endcapture %}

{% capture author_name %}{% if page.author %}{{ page.author.name }}{% else %}{{ site.author.name }}{% endif %}{% endcapture %}
{% capture author_url  %}{% if page.author %}{{ page.author.url }}{% else %}{{ site.author.url }}{% endif %}{% endcapture %}

{% capture company_name %}{% if page.author.company %}{{ page.author.company.name }}{% else %}{{ site.author.company.name }}{% endif %}{% endcapture %}
{% capture company_url  %}{% if page.author.company %}{{ page.author.company.url }}{% else %}{{ site.author.company.url }}{% endif %}{% endcapture %}

{% capture title %}{% if page.title %}{{ page.title }}{% else %}{{ supertitle }}{% endif %}{% endcapture %}

{% capture subtitle %}{% if page.subtitle %}{{ page.subtitle }}{% else %}[{{ author_name }}]({{ author_url }}){% if company_name %}, [{{ company_name }}]({{ company_url }}){% endif %}{% endif %}{% endcapture %}{% capture subtitle %}{{ subtitle | markdownify }}{% endcapture %}

{% capture fork_url %}{% if page.fork_url %}{{ page.fork_url }}{% else %}{{ site.fork_url }}{% endif %}{% endcapture %}
{% capture progress %}{% if page.progress %}{{ page.progress }}{% else %}{{ site.progress }}{% endif %}{% endcapture %}
