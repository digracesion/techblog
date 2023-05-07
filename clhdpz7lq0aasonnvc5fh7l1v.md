---
title: "Creating a Website/Portfolio with Jekyll"
seoTitle: "How to Create a Website or Portfolio with Jekyll"
seoDescription: "Here are some steps on how to create a website or portfolio using Jekyll and Github Pages"
datePublished: Sun May 07 2023 18:00:39 GMT+0000 (Coordinated Universal Time)
cuid: clhdpz7lq0aasonnvc5fh7l1v
slug: creating-a-websiteportfolio-with-jekyll
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/w7ZyuGYNpRQ/upload/02bb17e6f7094c91e55d04de335c5016.jpeg
tags: website, jekyll, portfolio, jekyll-tips

---

# Introduction  

Whether for an online portfolio or a website, I've noticed that more and more developers have started using website building frameworks as an alternative to the low-code/codeless website builders, which often require payments for additional customization.

Quite a popular service among these is [Jekyll](https://jekyllrb.com/), which seems to be a popular choice due to its integration with [GitHub Pages](https://pages.github.com/), which enables direct hosting from your GitHub repository.

Of course, there are other services such as [Gatsby](https://www.gatsbyjs.com/) (now integrated with [Netlify](https://www.netlify.com/)), [Hugo](https://gohugo.io/), [MkDocs](https://www.mkdocs.org/), and [Pelican](https://getpelican.com/). However, choosing the best service for your use would largely depend on a number of considerations:

1. **Ease of setup.** Is setting up the environment and installing dependencies easy?
    
2. **Available Integrations.** Is it able to integrate with the technology stack you are using or are familiar with?
    
3. **Learning Curve.** How easy is it to learn how to deploy your portfolio or website with the service?
    
4. **Programming Language**. If you plan on customizing your website a bit more than others do (e.g. without using templates/by creating your own templates), it's also important to consider the programming language/s in which the service is written.
    
5. **Availability of Templates.** If you plan on using templates that are readily available online, how easy is it to access these templates and integrate them into your portfolio?
    
6. **Speed**. How easy is it to load the contents of the website/portfolio using the service?  
    

In this post, we'll be focusing more on Jekyll as I provide a step-by-step guide on how to build your own portfolio with Jekyll.

# Dependencies

> **Note:** As I am using a MacOS system, the instructions I will be providing are based on the MacOS syntax.

1. Install [HomeBrew](https://brew.sh/) in your system.
    
    1. ```bash
        $ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
        ```
        
2. If you have already installed it, then update it to the latest version available.
    
    ```bash
    $ brew update
    $ brew upgrade
    $ brew cleanup
    ```
    
3. Install the LTS version of [Node.js](https://nodejs.org/en)
    
4. Install Ruby
    
    ```bash
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    brew install chruby ruby-install xz
    ruby-install ruby 3.1.3
    echo "source $(brew --prefix)/opt/chruby/share/chruby/chruby.sh" >> ~/.zshrc
    echo "source $(brew --prefix)/opt/chruby/share/chruby/auto.sh" >> ~/.zshrc
    echo "chruby ruby-3.1.3" >> ~/.zshrc # run 'chruby' to see actual version
    ```
    

# Installation

1. In the folder where the website/portfolio is being built, install Jekyll and generate a new site.
    
    ```bash
    $ gem install jekyll
    $ jekyll new <my-site>
    ```
    

This will generate the default theme called "minima".

1. Update the gem file to include Jekyll and Github Pages
    
    1. ```plaintext
        source "https://rubygems.org"
        
        gem "jekyll"
        gem "github-pages"
        ```
        
2. Bundle and install the dependencies
    

```bash
$ bundle install
```

1. Edit the `_config.yaml` file
    

```yaml
baseurl: /
url: https://<siteurl>
```

1. Edit the index file. This will be the main page of your website/portfolio.
    

```xml
---
layout: default
title: My GitHub Pages Site
---
<h1> Lorem Ipsum </h1>

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
```

1. Run the build and preview the file
    

```bash
$ bundle exec jekyll build
$ bundle exec jekyll serve
```

This will show a live preview of your website/portfolio at `http://localhost:4000`

> **Note**: You might encounter an issue with the webrick dependency which might cause the build to fail. If that happens, install the webrick dependency.

```bash
$ bundle add webrick
```

If you're creating from a template, do not generate a new Jekyll template. Instead, run the following steps after installing the dependencies:

1. Fork the template into your repository
    
2. Clone the repository into your local environment
    
3. Install dependencies
    
    ```bash
    $ npm install
    $ bundle install
    $ gem install jekyll
    ```
    
4. Edit the files to your liking.
    
5. Stage the changes to your GitHub repository
    
    ```bash
    $ git add .
    ```
    
6. Commit the changes and provide a comprehensive commit message.
    
    ```bash
    $ git -m "<comment>"
    ```
    
7. In some templates, Gulp needs to be installed. However, this is not the case for all of the templates. Be sure to check the `Readme` file of the template you'll be using.
    

```bash
$ npm install gulp-cli global
$ npm install --save-dev gulp-cli
```

1. Run the build and preview the file.
    

```bash
$ bundle exec jekyll build
$ bundle exec jekyll serve
# or use gulp if it is available
$ gulp
```

If Gulp is used, then the preview is hosted at `http://localhost:3000`  

# References

[MacOS installation](https://jekyllrb.com/docs/installation/macos/)  
[Spencer Pao](https://www.youtube.com/watch?v=g6AJ9qPPoyc)