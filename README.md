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

### Adaptive Pages
### Facebook Comments

## Project philosophy

## Contributing
