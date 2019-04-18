# Documentation Guideline

[//]: # "References"
[logo]: https://via.placeholder.com/900x300/000000/FFFFFF/?text=logo+placeholder
[license-badge]: https://img.shields.io/badge/license-BSD-green.svg
[beginners-guide-to-documentation]: https://www.writethedocs.org/guide/writing/beginners-guide-to-docs/
[documentation-style-guide]: https://www.writethedocs.org/guide/writing/style-guides/
[adam-p-markdown-cheatsheet]: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet
[online-markdown-editor]: https://dillinger.io/
[markdown-basics]: https://www.writethedocs.org/guide/writing/Markdown_basics/
[w3-headers]: https://www.w3schools.com/html/html_headings.asp
[license]: ./LICENSE.md
[issue-tracker]: https://github.com/alex-lechner/Documentation-Guideline/issues
[readme-template]: ./template/README.md
[alex-lechner-img]: https://avatars.githubusercontent.com/alex-lechner?s=150
[alex-lechner-link]: https://alexanderlechner.com

![Your project's logo][logo]

![BSD License][license-badge]

This documentation guideline serves as a boilerplate template and tutorial for writing good, structured documentation of your codebase.

## Table of Contents

- [Documentation Guideline](#documentation-guideline)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
  - [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
  - [Documentation](#documentation)
    - [Structure](#structure)
      - [Provide a table of contents](#provide-a-table-of-contents)
        - [Bad example](#bad-example)
        - [Good example](#good-example)
      - [Hierarchical order by using headers](#hierarchical-order-by-using-headers)
        - [Bad example](#bad-example-1)
        - [Good example](#good-example-1)
      - [Provide links to references](#provide-links-to-references)
        - [Bad example](#bad-example-2)
        - [Good example](#good-example-2)
  - [Contribution](#contribution)
  - [Acknowledgement](#acknowledgement)
  - [License](#license)
  - [Citation](#citation)
  - [Contact](#contact)

## Introduction

Good documentation is like a good book: Fun to read and easy to understand but hard (and often annoying) to write. Even though it is the least exciting part in software development it is still the developer's responsibility to ensure a comprehensible and well-documented codebase.

Because I get worked up over badly documented dependencies, libraries, etc. on which my work depends on I decided to come up with a guideline and template that I can use for my own projects as well.

So this project shall help developers to write an easy to understand documentation and provides a template which can be reused and adapted throughout different projects. All the given advice in this document provides a framework which can be altered. It shall give developers a kick start and **DOES NOT** enforce any strict rules.

No more excuses for writing (good) documentation, fellows! 📝😈

## Getting Started

### Prerequisites

This boilerplate is written in Markdown language so what you will need is a text editor and some knowledge on how to write Markdown.

- [Markdown Basics][markdown-basics]
- [adam-p's Markdown Cheatsheet][adam-p-markdown-cheatsheet]
- [Online Markdown editor][online-markdown-editor]

### Installation

This README already serves as a boilerplate and as an example of well-written documentation. However, a template with less text and clear instructions is provided under [template/README.md][readme-template].

So here is the suggested approach for this project:

1. Read through this whole README first to get a grasp of what makes good documentation (in my opinion).
2. Take note of the advice given in this README.
3. Take a look at the README in [template/README.md][readme-template]. (Notice how it has the same structure as this README? The difference is it has less text and clear instructions.)
4. Clone this repository.
5. Copy the README from [template/README.md][readme-template] and paste it into your project.
6. Write documentation that rocks! 🎸

## Documentation

### Structure

The #1 thing that all good documentations have in common: Structure. Whether your project is small or the size of an enterprise solution you want to keep your documentation in order for the reader (and for you too). So here's my advice to start things off:

#### Provide a table of contents

Again, think of your documentation like a book: It might start small with a few words but it grows over time and ends up big. Providing a table of contents helps your team members and contributors to get an overview of the scope of your project and to jump to specific parts in your documentation right away. Every headline (even the smallest sixth-tier header) needs to be **included and linked** in the table of contents. Don't forget to take the respective hierarchy into account!

##### Bad example

```md
- [h2-header](#link-to-your-h1-headline)
- [h1-header](#link-to-your-h2-headline)
  - [h3-header](#link-to-your-h3-headline)
  - [h4-header](#link-to-your-h4-headline)
- [h5-header](#link-to-your-h5-headline)
  - [h6-header](#link-to-your-h6-headline)
```

##### Good example

```md
- [h1-header](#link-to-your-h1-headline)
  - [h2-header](#link-to-your-h2-headline)
    - [h3-header](#link-to-your-h3-headline)
      - [h4-header](#link-to-your-h4-headline)
        - [h5-header](#link-to-your-h5-headline)
          - [h6-header](#link-to-your-h6-headline)
  - [h2-header](#link-to-your-h2-headline)
    - [h3-header](#link-to-your-h3-headline)
    - [h3-header](#link-to-your-h3-headline)
```

Every headline that is a child of the previous headline needs to be indented by two spaces. If you indent list items like the headers in our example then Markdown will know that the indented item is a child of the previous item. The indentation gives the reader an orientation and understanding of the relation of your content.

The hierarchical organization of your documentation leads me to my next point.

#### Hierarchical order by using headers

The hierarchical order of headers are so important but yet so overly misused and misinterpreted. I've seen the wrong use of headers so often in HTML- and web-based projects that it drives me nuts. **Headers are not an element of visual appeal but an element of structure!**

Or to put it in the words of [w3schools.com][w3-headers]:

> Search engines use the headings to index the structure and content of your web pages.
>
> `<h1>` headings should be used for main headings, followed by `<h2>` headings, then the less important `<h3>`, and so on.
>
> **Note: Use HTML headings for headings only. Don't use headings to make text BIG or bold.**

The same applies for Markdown because Markdown is an easy-to-write version of HTML (you can also write HTML-tags in a Markdown file).

The proper order of headers basically means you can not use an h3-header if you have not used an h2-header before. Even though this might seem logical this is commonly misused among "professional" web developers.

##### Bad example

```markdown
# Some big headline

Now some text.

### Some fancy small headline because I think it looks cool

Some text again.

# Some big headline again

So much content, eh?

##### Now I want to be extra fancy with this headline

Last text for this example.
```

##### Good example

```markdown
# Some big headline

Some good text.

## A structured and hierarchical headline

### Search engines will now love your page

Not every header needs to have a paragraph afterward ;)

#### Now I think you are less of an amateur

Here again some sample text.

##### Now you understand the concept

We're done!
```

Even though this is a guideline for documentation you might ask yourself: "But what if the `<h2>`-header is too big and I want a fancy little `<h5>`-header?"

The answer to this question is: Make use of CSS and the `class=""` or `id=""` properties in HTML to set the font size.

#### Provide links to references

Even it might be annoying to look up and link every single page for every dependency, resource, and so on your collaborators will appreciate your effort. But if you don't do it your team members and collaborators spend more time searching up crucial information rather than fixing YOUR bugs just because of your lazy a\*\* mentality! There's a difference between a single person that does a 10-minute search on the internet or 10 people that do a 10-minute search on the internet.

If you have all your links together and you want to hyperlink your text I do not recommend to place the link inline in your Text. I recommend dedicating an own section in your README with a collection of your links assigned to variables (yes, Markdown is capable of this).

The reason I recommend this is because:

1. It keeps things clean and orderly
2. You might want to reuse specific links
3. If you change the value of the link it is applied to all references

##### Bad example

```markdown
# Project title

![Some cat image](./my-cat-folder/cute-cat.png)

[Link to a website](https://my-website.com)

<!--
This comment represents thousands of lines of documentation
--->

[Here I link to the same website again but this time I made a typo unintentionally](https.//my-westsite.com)

<!--
This section is also documented with thousands of line
--->

![I want to show the cat image again but I forgot the link... Now I have to scroll all the way up and search for the correct hyperlink](./my-cool-cat-folder/cutecat.png)
```

##### Good example

```markdown
# Project title

[//]: # "References"
[image-of-a-cat]: ./my-cat-folder/cute-cat.png
[personal-website]: https://my-website.com

![Some cat image][image-of-a-cat]

[Link to a website][personal-website]

<!--
This comment represents thousands of lines of superb documentation
--->

[Here I need the link to the same website again][personal-website]

<!--
Another representation of world-class documentation
--->

![Maybe I want to display the cat image again][image-of-a-cat]
```

I suggest placing your link collection at the very beginning of your document right after your project's title. Having collection like this makes it a single point of error and therefore better traceable in case of broken links.

TODO: Describe how the documentation shall be written (grammar, tenses, formulate for DAU)

TODO: Explain when and how to use a documentation tool

TODO: Give bad, good and best examples if code snippets are included

TODO: How files and code references should be highlighted

TODO: Include examples of well-documented projects

## Contribution

If you think this project lacks some further crucial information or you have some good advice, best-practices or crazy ideas feel free to submit a pull request or file an issue under [github.com/alex-lechner/documentation-guideline/issues][issue-tracker]

## Acknowledgement

| [![Alexander Lechner][alex-lechner-img]<br>Alexander Lechner][alex-lechner-link] |
| :------------------------------------------------------------------------------: |


For this project, I have used some inspiration from other resources as well. Make sure to check out the following resources:

- [A beginner’s guide to writing documentation][beginners-guide-to-documentation]
- [Style Guides for Documentation][documentation-style-guide]
- [cezaraugusto's Guidelines for GitHub Templates](https://github.com/cezaraugusto/github-template-guidelines)

## License

This project is licensed under [Zero Clause BSD][license]. Feel free to do with the project whatever you want and make the world a better-documented place!

## Citation

If you want to cite this project:

```
@manual{DocGuideline,
 author    = {Lechner, Alexander},
 title     = {Documentation Guideline},
 address   = {Vienna},
 year      = {2019}
}
```

## Contact

You can reach out to me under office@alexanderlechner.com
