# Tekkie Offensive Website 

## Work in Progress
We forked this site from the gdg-x project zeppelin. Because we're still in transition it might be a bit outdated and blurred here but this will be better from time to time ;) Please be patient.

## Adding content
Find below a brief description how you can add content to the different sections. In order to use the dynamics and automatics provided by [Jekyll](http://jekyllrb.com/) we are using markdown in every kind of post. But we're differentiate between several kinds of posts. And we're going to introduce them here as well very briefly. For everything we're adding you should keep some conventions in mind:

### Filename
The file you're going to add has to follow this naming convention:
```bash
YEAR-MONTH-DAY-title.MARKUP
```
In real life it should look like
```bash
2012-09-12-how-to-write-a-blog.textile
```
### Adding blog posts
A blog post is something very short and personal. If you want to to add a blog post you have to add a file containing the post to
```bash
_posts/blog
```
And there is a very specific content that has to be in this file as well which is the so-called "Front Matter". Here you're adding some kind of metainformation regarding the content. For a blog post it should look like 
```bash
---
layout: post                # What kind of layout should be used for your post?
title:  "Meaningful Names"  # What's the name that should be shown?
date:   2015-01-01 09:00:00 # The publishing date...
author: Daniel Zappold      # The authors name (in most case yours ;)
isStaticPost: false         # Is this static or not? A blog is more or less dynamic
categories:					# What is this kind of post?
- blog                      # A blog post!
---
```
### Adding articles
Articles are more specific and unpersonal. It should be used for more general topics so we can create an index out of it. As blog posts we should follow some conventions as well. So please add an article to
```bash
_posts/articles
```
The "Front Matter" is almost the same compared to the blog posts. There's only a single change:
```bash
---
<... same content as blog posts ...>

categories:					# What is this kind of post?
- article                   # An article!
---
```
## Old Read me content

### About 
Project Zeppelin allows you to setup awesome GDG DevFest site in 5 minutes. 

Project is builded on top of [Jekyll](http://jekyllrb.com/) - simple, blog-aware, static site generator. Jekyll also happens to be the engine behind GitHub Pages, which means you can use Jekyll to host your website from GitHub’s servers for free. [Learn more about Jekyll](http://jekyllrb.com/).

Template is brought by [GDG Lviv](http://lviv.gdg.org.ua/) team.

### Live demo http://gdg-x.github.io/zeppelin/

### Features
* Easy to setup
* Simple and responsive design
* Integrated speakers and sessions management
* SVG icons
* SEO friendly


### Quick-start guide
1. [Fork](https://github.com/gdg-x/zeppelin/fork) this repo
2. Clone locally
3. Update ```_config.yml``` 
4. Select what content blocks do you need
5. Push changes to ```gh-pages``` branch
6. Enjoy your awesome DevFest site at ```http://[your github name].github.io/zeppelin/```

Or watch project presentation from [GDG[x] Townhall meeting](http://www.youtube.com/watch?v=xYmhheoLjcI). Slides available [here](https://docs.google.com/presentation/d/19aM7yNl_orDaCNND5LpCY3fShb6PyMltnzYfKvV8R_8/edit?usp=sharing)


## Local development

Check if you have [all requirments for local environment](http://jekyllrb.com/docs/installation/), install [Jekyll server](http://jekyllrb.com/docs/quickstart/) gem.
Install GitHub pages
```bash
  gem install github-pages
``` 

Run this command from project root folder:
```bash
    jekyll serve -w
```
Site will be available at http://127.0.0.1:4000/zeppelin/ or http://localhost:4000/zeppelin/ (on Windows)

**NOTE:** in this mode all changes to html and data files will be automatically regenerated, but after changing ```_config.yml``` you have to restart server.

### Sass(Compass) support
Install the latest version of [Compass](http://compass-style.org/). Ruby uses Gems to manage its various packages of code like Sass. In your open terminal window type:
```bash
  gem install compass --pre
```

Then for combining media queries you can use [Sass::MediaQueryCombiner](https://github.com/aaronjensen/sass-media_query_combiner) plugin. Install with command
```bash
  gem install sass-media_query_combiner
```

And for prefixing css3 properties use [Autoprefixer](https://github.com/ai/autoprefixer)
```bash
  gem install autoprefixer-rails
```

**Note:** Also you need to install [Node.js](http://nodejs.org/download/)

To watch changes of `.sass` files and compile it to the `.css` on a fly change property `safe: true` to `safe: false` in `_config.yml`.
**Note: It works only on local machine, because GitHub runs Jekyll in `--save` [mode](https://help.github.com/articles/using-jekyll-with-pages/#configuration-overrides)**

Learn more about Sass development from [documentation](https://github.com/gdg-x/zeppelin/wiki/Sass-development).


### Resource optimizations (optional)

You can optimize images and minify css and javascript automaticaly (for now only on Windows).
But for Mac OS users available amazing tool - [imageoptim](https://imageoptim.com/). Thanks [@raphaelsavina](https://github.com/raphaelsavina) for link.
Optimize all images by running this script from `/automation/images/` folder:
```bash
    all_image_optimization.bat -d -jtran -pout -pquant -optip -gsicle -svgo
```

To minify CSS and JS run `minify_all.bat` from `/automation/minifying/` folder:
```bash
    minify_all.bat
```

Learn more about available optimization options from [documentation](https://github.com/gdg-x/zeppelin/wiki/Resources-optimizations).

### Documentation
Quick-start guide is not enough? Checkout [full documentation](https://github.com/gdg-x/zeppelin/wiki).


### TODO List
* Optimization scripts for mac and linux

### Known issues
* Scrolling on open navbar

### Used libraries
* [Bootstrap](https://github.com/twbs/bootstrap)
* [Animate.css](https://github.com/daneden/animate.css)
* [Waves](https://github.com/publicis-indonesia/Waves)
* [jquery.appear](https://github.com/bas2k/jquery.appear)
* [jQuery countTo Plugin](https://github.com/mhuggins/jquery-countTo)
* [Typed.js](https://github.com/mattboldt/typed.js)
* [Sticky-kit](https://github.com/leafo/sticky-kit)

### Who is using template?
Going to use template? Go on! The only thing we ask - let us know at [*lviv@gdg.org.ua*](mailto:lviv@gdg.org.ua) so we can include you to this list, or make a pull request.

| | | |
|------|------|------|
| [GDG DevFest Ukraine 2014](http://devfest.gdg.org.ua/) | [GDG DevFest Istanbul 2014](http://devfesttr.com/) | [GDG Bangalore Site](http://gdgbangalore.github.io/) |
| [GDG DevFest Omsk 2014](http://gdg-devfest-omsk.org/) | [2014 南阳 GDG Devfest 大会](http://devfest.gdgny.org) | [DevFest Nordeste 2014](http://2014.devfestne.com.br/) |
| [GDG DevFest The Netherlands](http://www.devfest.nl/) | [DevFest Centro-Oeste 2014](http://www.devfestcentrooeste.com.br/) | [Android DevFest Space Coast](http://gdg-space-coast.github.io/zeppelin/) |
| [DevFest SP 2014](http://sp.devfest.com.br/) | [DevFest in Baroda](http://devfest.gdgbaroda.com/) | [GDG Hi Pic (France)](http://maximemularz.github.io/zeppelin/) |
| [GDG DevFest Córdoba 2014](http://gdgcordoba.github.io/zeppelin/) | [GDG DevFest Düsseldorf 2014](http://www.gdg-dus.de/DevFest2014/) | [GDG Makerere DevFest 2014](http://gdgmakerere.github.io/) |
| [GDG Dublin DevFest 2014](http://gdg-dublin.appspot.com/) | [GDG Busitema DevFest 2014](http://gdgbusitema.github.io/) | [DevFest Vienna 2014](http://www.devfest.at/) |
| [Android Wear DevFest](http://devfest.gdgnorthjersey.com/wear2014/) | [GDG SLAU DevFest 2014](http://gdgslau.github.io/) | [Lima DevFest](http://limadevfest.com/) |
| [GDG Korea DevFair 2014](http://devfair2014.gdg.kr/) | [GDG DevFest Kota Kinabalu 2014](http://devfest.gdgkk.info/) | [GDG DevFest Belgium](http://gdg-brussels.org/DevFest2014/) |
| [DevFest Praha 2014](http://devfest.cz/) | [GDG DevFest Kosice](http://devfest.sk/) | [GDG DevFest Cagayan de Oro](http://devfest.gdgcdo.org/) |
| [DevFest Birgunj](http://gdgbirgunj.github.io/DevFest2014/) | [GDG DevFest Poland](http://devfest.pl/) | [GDG DevFest Silicon Valley](http://devfest2014.gdgsv.com/) |
| [DevFest Chennai 2014](http://devfest.gdgchennai.com/) | [GDG DevFest Bari](http://gdgbari.github.io/zeppelin/) | [GDG DevFest Ahmedabad](http://devfest.gdgahmedabad.com/) |
| [GDG DevFest Sri Lanka](http://www.devfestlk.org/) | [GDG DevFest Tunis](http://devfest.gdgtunis.org/) | [GDG DevFest Kozhikode](http://devfest.gdgkozhikode.org/) | 
| [GDG DevFest Argentina](http://devfest.gdg.com.ar/) | [GDG DevFest Bhubaneswar](http://devfest2014.gdgbbsr.com/) | [GDG DevFest Miage Gi](http://gdgmiagegilab.github.io/) | 
| [GDG DevFest NORTE](http://norte.devfest.com.br/) | [GDG Devfest Nyeri 2014](http://devfest.gdgkimathiuniversity.com/) | [GDG DevFest Paris](http://devfest.gdgparis.com/) |
|[GDG Akure](http://gdgakure.github.io/)||


### Contributors
* Design and web development: [Oleh Zasadnyy](https://github.com/ozasadnyy)
* Idea: [Vitaliy Zasadnyy](https://github.com/zasadnyy)

### Licence
Project is published under the [MIT licence](https://github.com/gdg-x/zeppelin/blob/master/LICENSE.txt). Feel free to clone and modify repo as you want, but don't forget to add reference to authors :)


