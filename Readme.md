# Jekyller

This is a generator for the [Shower HTML presentation engine](https://github.com/shower/shower).

It takes your markdown document and transforms it into the Shower slides. Almost all the things are transformed smoothly, however there could be some things you could configure, either in the YAML front matter or using some extra special formatting.

## Install

### At GitHub Pages

Jekyll Shower works at GitHub Pages. Yes, it's using Jekyll and don't need any extra plugins, so using it is really staightforward:

1. [Fork this repo.](https://github.com/shower/jekyller/fork_select)
2. Make any changes to it (like change your username and all those stuff in the `_config.yml`). You can do it right on the GitHub, btw.
3. Commit & Push the changes — GitHub would initialise Pages only on the first push after the forking action. That could take up to 10 minutes.

That's all — after doing so you could go at your generated pages — replace there the `username` with your username: `http://username.github.com/jekyller/`, and you'll see Jekyll-generated example of the Shower presentation.

### Local usage

If you'd like to preview the changes or compile it locally, so you'd have static HTML of your slides (and you could access them without an internet access), you should clone this repo (or a fork) locally:

    git clone --recursive git://github.com/shower/jekyller.git
    
Note that you'll need either to use the `--recursive` flag, 'cause there are submodules to fetch, or you'll need to use `git submodule init && git submodule update` in order to fetch them manually if you didn't use this flag.

After cloning all you'll need to do is to run Jekyll in the cloned folder. On how to install and run Jekyll [read it's readme](https://github.com/mojombo/jekyll#getting-started).

## Use

The basic usage is very simple. After you'll configure everything up in the `_config.yml` (I recommend you do so: you should at least change the default `author` entry), you could begin making your slides.

Look at the `index.md` for an example of how you can describe your slides. Your markdown document should need the YAML front matter like this:

``` YAML
---
layout: default
---
```

That's the minimal front-matter you need. You could configure it later.

Note that you don't need to place your title here — Jekyller would get it from the first `H1` found in your markdown document (actually, at the moment, you _need_ to have the first-level header to go right after the YAML front matter).

So, you just write

``` md
# You slides’ title
```

And get this as a title for your slides as well as make this slide a cover for the whole presentation.

If you won't want to make this slide a cover, but a generic slide, just add a `.slide` class (however, I think you'd rarely would want this — covers are nice!):

``` md
# You slides’ title
{:.slide}
```

Everything else goes smoothly: use second level headers to divide the content into the slides and all the other tags inside to make your presentation.

I'll describe there all the things you could do in your presentation, as well as all the available options later in this Readme, so stay tuned!

## Features

### GitHub Pages support

See [install](#install) notes on how you can use Shower with Jekyller in just a few easy steps.

### Organize your presentations

With Jekyller you can have all your presentations in one place: just create a new `.md` file in the project, add a proper YAML front matter as mentioned above and start writing you slides!

## Credits and License

This is just a generator for the awesome [Shower](https://github.com/shower/shower) engine by [pepelsbey](https://github.com/pepelsbey) and [other nice people](https://github.com/shower/shower#contributing).

All the themes are [attached as submodules](https://github.com/shower/jekyller/tree/gh-pages/themes), and all the rights for them are belong to their authors.

Jekyll Shower licensed under [MIT License](http://en.wikipedia.org/wiki/MIT_License), see [license page](License.md#the-mit-license) for details.
