---
layout: post
title:  "Setting up your blog with Jekyll and Github"
author: Aman
categories: [ Github, jekyll ]
image: assets/images/githubjekyll.webp

---

 Most of us are aware of blogging platforms such as WordPress, while they are very easy to setup and provides simple medium to interact with the platform. But what most people do not know that they come with their own disadvantages. That is a major reason why many of the leaders are looking for other alternatives. 

There are many reasons that may drive you away from dynamic blogs like WordPress – 

- Cost is high

- Speed is slower 

- Less control over the platform

- The free version is very restricted and does not even allows your own domain name


### What is the alternative?

While there are many one of my most preferred is using a static site generator like Jekyll with GitHub Pages. GitHub provides excellent way to host site such as your personal projects but can also be used to host Jekyll site without even needing any of the other deployment tools such as Netlify. Also, one of the reasons to choose Jekyll is that it is also very Noob friendly i.e. that it is also very easy to use for the person who does not have much knowledge of web development.

What we need ?

- A GitHub account 

  

   <!--Custom domain ( if we want give our blog a professional look, else it would look something like “yourusername.github.io” )-->


Now first of all we need to setup the environment for Jekyll, To do that we have to setup a full Ruby environment. 

#### Setting up the environment –

Head over [here](https://rubyinstaller.org/) and download the latest release.

Then open the installer and proceed with default parameters.

Verify ruby version with command from command prompt.

```powershell
ruby -v
```

![ruby test]({{ site.baseurl}}/assets/images/2/ruby.webp)

Since our environment is setup next step is to download theme/ Template for our Blog. There are many websites to download themes from, the one recommended by the official Jekyll docs are - 

-  jamstackthemes.dev
- jekyllthemes.org
- jekyllthemes.io
- jekyll-themes.com

Now head to any of the site you want and download the theme of your choice. For the ease of tutorial we are using this [theme](https://jamstackthemes.dev/theme/dark-poole/). 

![Jekyll theme screenshot]({{ site.baseurl}}/assets/images/2/themess.webp)

Now click download button as highlighted above and extract the code after downloading, it will look like as shown in screenshot.

![Directory]({{ site.baseurl}}/assets/images/2/extract.png)

Now open a command prompt here by typing cmd in the address bar.

after that type following commands in the order shown - 

```
gem install bundler
bundle install
bundle exec jekyll serve --incremental
```
![Commands Demo]({{ site.baseurl}}/assets/images/cmd1.webp)

![Commands Demo]({{ site.baseurl}}/assets/images/2/cmd2.webp)

![Commands Demo]({{ site.baseurl}}/assets/images/2/cmd3.webp)



this will run the site locally and we can view the site using the link that will be provided by the last command. This will allow us to view our content locally so that if we want to do some modifications we can do easily.
![Local site screenshot]({{ site.baseurl}}/assets/images/site.webp)
 Now after that we have to publish our code on GitHub to do that simply push that folder to a GitHub repo. To do that we will use git commands which we can learn from [here](https://www.datacamp.com/community/tutorials/git-push-pull) on how to publish our folder to a git repo.

**_post is the directory to store all the posts in the markdown format(an easy way to write web articles)**

**Note** - the name of your repo should be  in the format *yourusername.github.io* this will allow to access your blog directly through this link.

