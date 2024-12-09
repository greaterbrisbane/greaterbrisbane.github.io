# Website

Currently, <https://greaterbrisbane.org> is a GitHub Pages website using Jekyll. 

More specifically, we're running on Jekyll v4 with a modestly customised Minima v3 base theme. 

**By contributing to this repository, you grant permission for Greater Brisbane Urbanists, Inc. to use your contribution indefinitely.**

## Adding content

### Posts

Most content on the site should take the form of a *post*.

To do this, add a file (typically Markdown) in the `_posts` folder. 

Include the publish date (YYYY-MM-DD) at the start of the filename, and some additional metadata at the start of the file in YAML format:

```yaml
---
layout: post
title: "Insert Title Here"
categories:
  - Insert
  - Categories
  - Here
image: /assets/images/path/to/image.jpg
description: "Insert Description Here."
---

```

Category names are case sensitive. Try to use one of the existing ones. 
(Events, Principles, Priorities, Advocacy.)

If you have **images** they go in the `assets/images` folder. If an image is general then it can go at the folder directly, or you might like to make a subfolder named for the post if you think the image won't be reused.

The `image` key lets you specify an image which will be used for link previews and such. Note the leading slash on `/assets/...` --- this is a Jekyll thing. 
If you don't specify an image, the default is a Greater Brisbane logo. 

The `description` should be a one-sentence summary of the post (or its first sentence in a pinch).

Image and description are shown for the latest post on the homepage. 

### Pages

Less commonly we will need a new page. This can be written in Markdown or HTML. 

Again, you will need some metadata. The `permalink` key is often useful for pages.

By default, pages are included in the header navigation. To prevent this, set `exclude: true`.

```yaml
---
layout: page
title: "Insert Title Here"
permalink: "https://greaterbrisbane.org/some-special-link"
exclude: true
---

```

## Building / developing 

This is a Jekyll site, so you'll need Ruby and Jekyll (see also `.ruby-version`). 

- <https://jekyllrb.com/docs/installation>
- `gem install jekyll bundler`

Clone this repository to where you'd like it to be: 

`git clone git@github.com:greaterbrisbane/greaterbrisbane.github.io.git`

Make sure you're running on the correct Ruby version. One option is [chruby](https://github.com/postmodern/chruby) which recognises `.ruby-version` files.

Install the various dependencies: `bundle install`

Launch the dev site: `bundle exec jekyll serve`
