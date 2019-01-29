# simple-srd

An easy to use template for quickly creating SRD style documents and webpages. Minimum styling for customizable theming.

test content shamelessly used without permission from the Gold ENnie award winning website [bladesinthedark.com](https://bladesinthedark.com/)

## Usage

Creating a great webpage doesn't require you to know any javascript, css or even html. The are only a couple types of files you will ever need to touch. The first type of file is called a YAML file with the .yml extension. It stores structured data in text format. 

Currently there is only a single file of this type called links.yml. It stores any links that you want to appear in your navigation menu. 

[file](https://github.com/non-binary-trees/simple-srd/blob/master/_data/links.yml)

```Yaml
- label: blades in the dark # This is the text that appears on your site for the link
  url: https://bladesinthedark.com # This is where the link goes to
- label: internal link
  type: internal # For links to your own site use this flag
  url: /index 
```

following that ppatern you can create links for anything you will need.

The other type of file is Markdown with the .md extension. This is mostly just like you would normally type with the addition of being able to mark things you want to be formatted a special way.

```Markdown
# simple-srd

An easy to use template for quickly creating SRD style documents and webpages. Minimum styling for customizable theming.

test content shamelessly used without permission from the Gold ENnie award winning website [bladesinthedark.com](https://bladesinthedark.com/)
```

Is how the first section of this file is written using Markdown.

Your actual website will be made of preset pages. These might include your homepage, a contact form and perhaps an about page. Initially you begin with just a home page called index.md

[file](https://github.com/non-binary-trees/simple-srd/blob/master/index.md)

```Markdown
---
title: Simple SRD
---

The easy way to make an SRD.
```

This file has two parts. The top section between the two '---' is YAML just like you saw before. It just defines a variable for when the page is rendered. For now you just need to know all our Markdown files should define a title variable. Following that section is just plain Markdown like in the previous example.

You can edit this using markdown to create a home page with whatever information you want visitors to see when they first visit your page.
