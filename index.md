---
layout: adaptive
title: Home
leftcolumn:
  - content
rightcolumn:
  - affiliation
  - post_list
---
# The Plimpton322 Theme
Plimpton322 is a Jekyll theme for GitHub Pages that is primarily targeted towards academic and scientific blogging. [You can preview the theme to see what it looks like](https://adrian-dalessandro.github.io/Plimpton322/ "Preview Plimpton322"), or even fork the project and use it today.

## Scientific Blogging
The philosophy behind this project is to support scientific bloggers & scientific communication. To do so, we provide a theme with out-of-the-box support for:
1. Latex-style equation support via MathJax ([see this post for an example](https://adrian-dalessandro.github.io/Plimpton322/2021/12/31/example-latex-math.html))
2. Markdown-style code blocks ([see this post for an example](https://adrian-dalessandro.github.io/Plimpton322/2021/12/30/example-python-blog-post.html))

beyond this, our goal is to provide an aesthetic & somewhat minimalist theme with built in customization options.

## Writing Posts
By default, this theme follows the default [Jekyll method for post writing](https://jekyllrb.com/docs/posts/). Briefly summarizing, all posts can be directly committed to your github account as either a markdown file or an html files. Each post must be saved in the `_post/` directory with the following format:
```
YEAR-MONTH-DAY-title.MARKUP
```

For example, the following are valid posts:

```
2021-12-31-example-latex-math.md
2021-12-30-example-python-blog-post.md
```

## Customizing
### Configuration variables
By default, the global configuration variables are stored in `_config.yml`. These are accessed through the `site._your_variable_` liquid variable throughout the project. The basic set of global configuration variables are:

```yaml
title: Plimpton 322 # This is the title of the site and controls the emphasized text in the site header
description: A jekyll theme for scientific blogging # This is a short site description that follows the title text
accent: green # This selects the sites colour-scheme, as explained below
paginate: 5 # This is the number of pages to dislay per page on the blog list page
paginate_path: "/blog/page:num/" # This controls the path to the different pages of the blog post
fb_comments_on: "true" # This toggles whether or not to use the facebook comments plugin
```

### Accents
Accents are a simple variable class that specifies the colour scheme of the website. Simply assign an accent keyword to the global `accent` variable. The available accent keywords are listed below:

| __green__ _(default)_: | __orange__: | __teal__: |
| :-------------: |:-------------:| :-----:|
| ![Green Accents](./assets/images/green_accent.png) | ![Orange Accents](./assets/images/orange_accent.png) | ![Teal Accents](./assets/images/teal_accent.png) |
| __red__:   | __purple__:  |   |
| ![Red Accents](./assets/images/red_accent.png) | ![Purple Accents](./assets/images/purple_accent.png)  |  |


### Author Cards
Author cards can be included in several places through the website. By default, any page with an adaptive layout can include an author card by merely adding an `affiliation` keyword to one of the header variables (discussed later). An author card is specified by modifying the yaml file found at `_data/authorship.yml`, which contains the following details:

```yaml
picture: /assets/images/headshot.png
name: Adrian D'Alessandro
biography: I'm a Graduate Student at SFU studying computer vision, deep learning, weak supervision, and plant agriculture.
affiliations:
  - title: Medical Image Analysis Lab @ SFU
    url: https://www.medicalimageanalysis.com/
outgoing:
  - title: Github
    url: https://github.com/adrian-dalessandro/
    icon: github
  - title: Twitter
    url: https://twitter.com/AdrianoDAlessa3
    icon: twitter
  - title: Email
    url: mailto:acdaless@sfu.ca
    icon: envelope
```

The `picture` variable is simple. Push a headshot, professional photo, or any other image to `/assets/images` and it will appear whereever the authorcard is specified. Likewise, the `name` variable is where you put your name, and the `biography` variable is a short description explaining something about you or your work.  

The more interesting varaibles the the `affiliations` and `outgoing` variables. The `affiliations` variable stores an array of affiliations, with each array element taking the following format:
```yaml
- title: your-affiliations-title
  url: the-path-to-affiliate-website.com
```
You may add as many affiliations as you wish and they will be listed underneathe your name in the title card. Similarly, the `outgoing` variable allows you to create a list of icons that link to some outgoing website. Similarly, this is specified as an array with each array element taking on the following format:
```yaml
  - title: title-of-website
    url: path-to-website.com
    icon: some-icon
```
The most complicated part of these variable entries is the `icon` entry. All icons reference the name of icons that can be found through the [Font Awesome website](https://fontawesome.com/icons). If you wish to use an icon, simply go to Font Awesome website and copy the name of the icon of interest and add it as the entry for the `icon` variable.

### Adaptive Pages

Adaptive pages are a template markup for placing sub-units of the website on different parts of a page. All adaptive pages are split into 2 columns and each page has a header for specifying which kinds of sub-units to place in the right and left column of the page. Consider the following example:
```yaml
---
layout: adaptive
title: About
leftcolumn:
  - content
rightcolumn:
  - affiliation
  - post_list
---
```
The left column of the page will hold the content (which refers to anything written in your markdown file), and the right column will hold your author card and a list of the 3 most recent posts to the website.

### Navigation & Adding New Pages
New pages are easy to create. You need to do two things. First, create a new markdown file in the root directory, for example `about.md`. Then in the `_data/navigation.yml` simply add the following array element to the `nav` variable:
```yaml
- title: About
  url: /about.html
```


### Facebook Comments
Because Jekyll is a static website generator, there is no backend or database within which to store comments. The simplest alternative is to support an external commenting solution. For our purposes, we opted to go with Facebook comments. Set the global variable `fb_comments_on` to true, and visit the file at `_includes/fbcomments.html` to change the appID to one you have registered yourself through the facebook API.


## Contributing
We welcome any and all contributions.
