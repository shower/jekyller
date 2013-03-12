# Jekyll Shower

This is a generator for the [Shower HTML presentation engine](https://github.com/shower/shower).

It takes your markdown document and transforms it into the Shower slides. Almost all the things are transformed smoothly, however there could be some things you could configure, either in the YAML front matter or using some extra special formatting.

## Install

Jekyll Shower works at GitHub Pages. Yes, it's using Jekyll and don't need any extra plugins, so using it is really staightforward:

1. [Fork this repo.](https://github.com/kizu/jekyll-shower/fork_select)
2. Make any changes to it (like change your username and all those stuff in the `_config.yml`). You can do it right on the GitHub, btw.
3. Commit & Push the changes — GitHub would initialise Pages only on the first push after the forking action. That could take up to 10 minutes.

That's all — after doing so you could go at your generated pages — replace there the `username` with your username: `http://username.github.com/jekyll-shower/`, and you'll see Jekyll-generated example of the Shower presentation.

## Use

The basic usage is very simple. After you'll configure everything up in the `_config.yml` (I recommend you do so: you should at least change the default `author` entry), you could begin making your slides.

Look at the `index.md` for an example of how you can describe your slides. Your markdown document should need the YAML front matter like this:

``` YAML
---
layout: default
---
```

That's the minimal front-matter you need. You could configure it later.

Note that you don't need to place your title here — Jekyll Shower would get it from the first `H1` found in your markdown document (actually, at the moment, you _need_ to have the first-level header to go right after the YAML front matter).

So, you just write


``` md
# You slides' title
```

And get this as a title for your slides.

If you'll want to make this slide a cover for you slides (and in 99% of cases you'd want), write it like this:

``` md
# You slides' title
{: .cover }
```

Everything else goes smoothly: use second level headers to divide the content into the slides and all the other tags inside to make your presentation.

I'll describe there all the things you could do in your presentation, as well as all the available options later in this Readme, so stay tuned!

## Credits and Licence

This is just a generator for the awesome [Shower](https://github.com/shower/shower) engine by [pepelsbey](https://github.com/pepelsbey) and [other nice people](https://github.com/shower/shower#contributing).

All the themes are [attached as submodules](https://github.com/kizu/jekyll-shower/tree/gh-pages/themes), and all the rights for them are belong to their authors.

Jekyll Shower licensed under [MIT License](http://en.wikipedia.org/wiki/MIT_License), see [license page](licence.md) for details.