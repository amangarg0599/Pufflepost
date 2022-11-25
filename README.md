# Memoirs Jekyll Theme

[Live Demo](https://wowthemesnet.github.io/jekyll-theme-memoirs/) | [Docs & Download](https://bootstrapstarter.com/bootstrap-templates/jekyll-theme-memoirs/) |  [Buy me a coffee](https://www.wowthemes.net/donate/)

#### How to use “Memoirs” theme

- [Download](https://github.com/wowthemesnet/jekyll-theme-memoirs/archive/master.zip) or `git clone https://github.com/wowthemesnet/jekyll-theme-memoirs.git`

From the rood of your downloaded/cloned folder, open your terminal and install:

```cmd
gem install bundler
```

Cmd

Copy

Then:

```cmd
bundle install
```

Cmd

Copy

Edit `_config.yml` options. If your site is in root: `baseurl: ''`. Also, change your Google Analytics code, disqus username, authors, Mailchimp list etc.

Again, from your terminal:

```cmd
bundle exec jekyll serve --watch
```

Cmd

Copy

You should be able to see your Jekyll project now, if you didn’t change the folder name you should see it live at `http://127.0.0.1:4000/jekyll-theme-memoirs`.

Start populating your blog by adding your `.md` files in `_posts`. Memoirs already has a few examples.

**YAML front matter options**:

- post image - `image: assets/images/mypic.jpg`
- external post image - `image: "https://externalwebsite.com/image4.jpg"`
- disable page comments - `comments:false`
- meta description (optional) - `description: "this is my meta description"`

##### YAML Post Example:

```mardown
---
layout: post
title:  "We all wait for summer"
author: john
categories: [ Lifestyle, Travel ]
tags: [ France ]
image: assets/images/5.jpg
description: "Something about this post here"
---
```

Mardown

Copy

##### YAML Page Example

```markdown
---
layout: page
title: About Memoirs
comments: false
---
```

Markdown

Copy

##### Rating

```markdown
---
layout: post
title:  "We all wait for summer"
author: john
categories: [ Jekyll, tutorial ]
image: assets/images/5.jpg
description: "Something about this post here"
rating: 4.5
---
```

Markdown

Copy

[Rating Post Demo](https://wowthemesnet.github.io/jekyll-theme-memoirs/review-oscar/)

##### Adsense

Enable this option by editing `_config.yml`.

```markdown
# Adsense (change to "enabled" to activate, also your client id and ad slot. Create a new ad unit from your Adsense account to get the slot.)
adsense: "disabled"
adsense-data-ad-client: "ca-pub-3412143450191416"
adsense-data-ad-slot: "1363087678"
```

Markdown

Copy

##### Lazy Load Images

Enable this option by editing `_config.yml`.

```markdown
# Lazy Images ("enabled" or "disabled")
lazyimages: "enabled"
```

Markdown

Copy

##### Table of Contents

Add `toc:true` on your post YAML.

```markdown
---
layout: post
title:  "Education must also train one for quick, resolute and effective thinking."
author: john
categories: [ Jekyll, tutorial ]
image: assets/images/3.jpg
beforetoc: "Markdown editor is a very powerful thing. In this article I'm going to show you what you can actually do with it, some tricks and tips while editing your post."
toc: true
---
```

Markdown

Copy

`beforetoc` adds a paragraph before the TOC is displayed.

##### Editing stylesheet

You’ll only work with a single file to edit/add theme style: `assets/css/theme.scss`.
