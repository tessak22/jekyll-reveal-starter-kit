# jekyll-reveal-starter-kit

A starting point for developing GDI slide sets using the reveal.js library and the jekyll static site generator

[Jekyll](http://jekyllrb.com) is a
[static-site generator](https://en.wikipedia.org/wiki/Web_template_system#Static_page_generators)
typically used to generate blogs, but also used heavily by
[Github Pages](https://pages.github.com/) to publish websites.

This starter kit allows the user to create a
[RevealJS](http://lab.hakim.se/reveal-js/) slide set for a class. This
particular version of reveal has been customized specifically by and
for Girl Develop It to keep class materials consisten.

The [GDIMpls Version](https://github.com/gdiminneapolis/reveal.js) of
reveal is embedded in this starter kit as a
[git submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules)
in order to provide the ability to get central updates when the
designs change.

## Pre-requisites

This starter kit needs to have the following software already
installed:

* [Git](https://github.com/gdiminneapolis/jekyll-reveal-starter-kit/wiki/Installing-Git)
* [Ruby](https://github.com/gdiminneapolis/jekyll-reveal-starter-kit/wiki/Installing-Ruby)
* Ruby `bundler` gem:

``` bash
gem install bundler
```

## Starter Kit Installation

To start a new set of class slides, or a new presentation, clone the
[repo] to your local system:

``` bash
git clone https://github.com/gdiminneapolis/jekyll-reveal-starter-kit.git my-awesome-course
```

where `my-awesome-course` is an empty directory you'll use to create
your presentation. When you create the course name, remember to **use
only lower-case letters, numbers, and dashes** in the filename. This
will become part of an externally available URL, so the URL format
must be valid.

Change the remote `origin` to `upstream`:

``` bash
git remote rename origin upstream
```

Create the remote `origin` for this repository. Using the **SSH**
version of the remote url, set the new `origin`;

``` bash
git remote add origin git@github.com:gdiminneapolis/my-awesome-course.git
```

Go ahead and push the current initial version up to your new repo:

``` bash
git push -u origin HEAD
```

## Complete Installtion

To complete the installation, run the `bundle install` command. On
OS/X or Ubuntu, it looks like this:

``` bash
bundle install
bundle binstub jekyll
```

## Configuration

There are some configuration values to set, which are found in the
`_config.yml` and `_config_publish.yml` files in the home
directory. (See
[editing yaml files](https://github.com/gdiminneapolis/jekyll-reveal-starter-kit/wiki/Editing-YAML-files)
in the starter kit wiki.) Edit these files in your code editor and
change the settings to be what you want.

There are only two settings you must absolutely change:

* `title` - change this to the title of your course
* `baseurl` - change this to the repository base name

Using the above example, you'd have:

``` yaml
title: My Awesome Course
baseurl: /my-awesome-course
```

(Thus revealing whey the restriction on the name for your repository:
it's used in the URL for the slide set when published on Github
pages.)
