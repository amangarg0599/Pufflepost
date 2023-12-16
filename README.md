#  Pufflepost Jekyll Site 🐧📝

## How to Use

```
bashCopy code
gem install bundler
```

Then:

```
bashCopy code
bundle install
```

Edit `_config.yml` options. If your site is in the root: `baseurl: ''`. Also, change your Google Analytics code, Disqus username, authors, Mailchimp list, etc.

Again, from your terminal:

```
bashCopy code
bundle exec jekyll serve --watch --incremental
```

You should be able to see your Jekyll project now. If you didn’t change the folder name, you should see it live at http://127.0.0.1:4000/

Start populating your blog by adding your `.md` files in `_posts`. Memoirs already has a few examples.

### *YAML Front Matter Options:*

- Post image - `image: assets/images/mypic.jpg`
- External post image - `image: "https://externalwebsite.com/image4.jpg"`
- Disable page comments - `comments: false`
- Meta description (optional) - `description: "this is my meta description"`

#### YAML Post Example:

```
markdownCopy code---
layout: post
title:  "We all wait for summer"
author: john
categories: [ Lifestyle, Travel ]
tags: [ France ]
image: assets/images/5.jpg
description: "Something about this post here"
---
```

#### YAML Page Example:

```
markdownCopy code---
layout: page
title: About Memoirs
comments: false
---
```

#### Rating

```
markdownCopy code---
layout: post
title:  "We all wait for summer"
author: john
categories: [ Jekyll, tutorial ]
image: assets/images/5.jpg
description: "Something about this post here"
rating: 4.5
---
```

#### Adsense

Enable this option by editing `_config.yml`.

```
markdownCopy code# Adsense (change to "enabled" to activate, also your client id and ad slot. Create a new ad unit from your Adsense account to get the slot.)
adsense: "disabled"
adsense-data-ad-client: "ca-pub-3412143450191416"
adsense-data-ad-slot: "1363087678"
```

#### Lazy Load Images

Enable this option by editing `_config.yml`.

```
markdownCopy code# Lazy Images ("enabled" or "disabled")
lazyimages: "enabled"
```

#### Table of Contents

Add `toc:true` on your post YAML.

```
markdownCopy code---
layout: post
title:  "Education must also train one for quick, resolute and effective thinking."
author: john
categories: [ Jekyll, tutorial ]
image: assets/images/3.jpg
beforetoc: "Markdown editor is a very powerful thing. In this article I'm going to show you what you can actually do with it, some tricks and tips while editing your post."
toc: true
---
```

`beforetoc` adds a paragraph before the TOC is displayed.

### Editing Stylesheet

You’ll only work with a single file to edit/add theme style: `assets/css/theme.scss`. 🎨✨
