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
[latex-editor]: https://www.codecogs.com/latex/eqneditor.php
[dont-make-me-think-book]: https://www.amazon.de/Dont-Make-Me-Think-Usability/dp/0321965515
[npm-documentation]: https://docs.npmjs.com/files/package.json
[grammarly-app]: https://app.grammarly.com
[sphinx]: https://www.sphinx-doc.org/en/master/
[mkdocs]: https://www.mkdocs.org/
[gitbook]: https://www.gitbook.com/
[read-the-docs]: https://readthedocs.org/
[footnote-1]: #footnote-1
[slack-api-doc]: https://api.slack.com/#read_the_docs
[traefik-doc]: https://github.com/containous/traefik
[digitalocean-doc]: https://www.digitalocean.com/docs/
[secure-linux-server-doc]: https://github.com/imthenachoman/How-To-Secure-A-Linux-Server
[license]: ./LICENSE.md
[issue-tracker]: https://github.com/alex-lechner/Documentation-Guideline/issues
[readme-template]: ./template/README.md
[alex-lechner-img]: https://avatars.githubusercontent.com/alex-lechner?s=150
[alex-lechner-link]: https://alexanderlechner.com

![Your project's logo][logo]

[![BSD License][license-badge]][license]

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
    - [Wording](#wording)
      - [Write for the DAU (dumbest assumable user)](#write-for-the-dau-dumbest-assumable-user)
        - [Bad](#bad)
        - [Good example](#good-example-3)
      - [Grammar and spelling](#grammar-and-spelling)
    - [Documentation tools](#documentation-tools)
      - [Bad Example](#bad-example)
      - [Good example](#good-example-4)
    - [Highlighting](#highlighting)
      - [Code blocks](#code-blocks)
        - [Bad example](#bad-example-3)
        - [Good example](#good-example-5)
      - [Filenames & line numbers](#filenames--line-numbers)
        - [Bad example](#bad-example-4)
        - [Good example](#good-example-6)
    - [Real world examples](#real-world-examples)
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
4. Clone this repository by executing the following command in your terminal or command line:
   ```sh
   git clone https://github.com/alex-lechner/Documentation-Guideline.git
   ```
5. Copy the README from [template/README.md][readme-template] and paste it into your project.
6. Write documentation that rocks! 🎸

## Documentation

### Structure

The #1 thing that all good documentations have in common: Structure. Whether your project is small or the size of an enterprise solution you want to keep your documentation in order for the reader (and for you too). So here's my advice to start things off:

#### Provide a table of contents

Again, think of your documentation like a book: It might start small with a few words but it grows over time and ends up big. Providing a table of contents helps your team members and contributors to get an overview of the scope of your project and to jump to specific parts in your documentation right away. Every headline (even the smallest sixth-tier header) needs to be **included and linked** in the table of contents. Don't forget to take the respective hierarchy into account!

##### Bad example

**Markdown**

```markdown
- [h2-header](#link-to-your-h1-headline)
- [h1-header](#link-to-your-h2-headline)
  - [h3-header](#link-to-your-h3-headline)
  - [h4-header](#link-to-your-h4-headline)
- [h5-header](#link-to-your-h5-headline)
  - [h6-header](#link-to-your-h6-headline)
```

**Output**

> - [h2-header](#link-to-your-h1-headline)
> - [h1-header](#link-to-your-h2-headline)
>   - [h3-header](#link-to-your-h3-headline)
>   - [h4-header](#link-to-your-h4-headline)
> - [h5-header](#link-to-your-h5-headline)
>   - [h6-header](#link-to-your-h6-headline)

##### Good example

**Markdown**

```markdown
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

**Output**

> - [h1-header](#link-to-your-h1-headline)
>   - [h2-header](#link-to-your-h2-headline)
>     - [h3-header](#link-to-your-h3-headline)
>       - [h4-header](#link-to-your-h4-headline)
>         - [h5-header](#link-to-your-h5-headline)
>           - [h6-header](#link-to-your-h6-headline)
>   - [h2-header](#link-to-your-h2-headline)
>     - [h3-header](#link-to-your-h3-headline)
>     - [h3-header](#link-to-your-h3-headline)

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

**Markdown**

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

**Output**

> # Some big headline
>
> Now some text.
>
> ### Some fancy small headline because I think it looks cool
>
> Some text again.
>
> # Some big headline again
>
> So much content, eh?
>
> ##### Now I want to be extra fancy with this headline
>
> Last text for this example.

##### Good example

**Markdown**

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

**Output**

> # Some big headline
>
> Some good text.
>
> ## A structured and hierarchical headline
>
> ### Search engines will now love your page
>
> Not every header needs to have a paragraph afterward ;)
>
> #### Now I think you are less of an amateur
>
> Here again some sample text.
>
> ##### Now you understand the concept
>
> We're done!

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

**Markdown**

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

**Output**

> # Project title
>
> ![Some cat image](https://placekitten.com/200/300)
>
> [Link to a website](https://google.com)
>
> _Placeholder for 1000 lines of documentation_
>
> [Here I link to the same website again but this time I made a typo unintentionally](https.//goole.com)
>
> _Placeholder for 1000 lines of documentation_
>
> ![I want to show the cat image again but I forgot the link... Now I have to scroll all the way up and search for the correct hyperlink](./my-cool-cat-folder/cutecat.png)

##### Good example

**Markdown**

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

**Output**

> # Project title
>
> [//]: # "References"
> [image-of-a-cat]: https://placekitten.com/200/300 > [personal-website]: https://google.com
>
> ![Some cat image][image-of-a-cat]
>
> [Link to a website][personal-website]
>
> _Placeholder for 1000 lines of documentation_
>
> [Here I need the link to the same website again][personal-website]
>
> _Placeholder for 1000 lines of documentation_
>
> ![Maybe I want to display the cat image again][image-of-a-cat]

I suggest placing your link collection at the very beginning of your document right after your project's title. Having collection like this makes it a single point of error and therefore better traceable in case of broken links.

### Wording

I get it. You are an engineer, have some sort of cool Ph.D. and you belong to the people at the top end of the cognitive strata. Luckily, school and university are over! Your team members and contributors don't give a damn about how articulate you are because they want to be productive as fast as possible. Using fancy, old-fashioned words don't get your colleagues anywhere. Make sure to use simple and commonly used words. With that being said this does not mean that you should not include any complicated math formulas that are necessary for your project. If you need to provide math formulas you can do so with a [LaTex editor][latex-editor] but keep in mind that some of your collaborators might not have any clue what the symbols mean. To prevent that always make sure to explain what the formula does and how it can be calculated if you substitute the variables.

#### Write for the DAU (dumbest assumable user)

> _"An alleged scientific discovery has no merit unless it can be explained to a barmaid."_
>
> Ernest Rutherford

Another variant of this is: _"You do not really understand something unless you can explain it to your grandmother."_

And it's totally true. You have to explain everything in plain language. Every single step needs to be documented and easy to understand. Don't assume that your collaborators know what to do, truth is they often don't. In fact, everyone becomes the DAU (dumbest assumable user) when starting a new project. You want to give your reader a step-by-step tutorial on how to set up your project and an instruction on where to start.

Keep in mind: **There's no such thing as too much documentation, only too less.**

Also, readers want to be guided. So giving you're readers too many options and choices to start with will make them think (in a negative way). I always think of documentation like a website (because it is in some sense). You should give clear instructions for the reader and don't make your readers think about what to do.

There's also a book called [Don't make me think by Steve Kruger][dont-make-me-think-book] (no affiliate link) which provides an approach to usability on websites. I think some of the book's principles can be adapted for writing good documentation.

However, what you should avoid is documenting stuff which is already documented by other sources. You can simply provide a link for further information. To give you a quick example: Let's imagine you have a NodeJS project with the famous `package.json` file inside of your project's folder. For someone who is new to NodeJS, this file will be a complete mystery to that person. But instead of writing complete details about this file you can simply write: "The `package.json` file manages all necessary dependencies for production and development and provides basic configurations for the project. For further information please read [the official documentation][npm-documentation]."

##### Bad

**Markdown**

````markdown
## Install

```
npm install bootstrap
```
````

**Output**

> ## Install
>
> ```
> npm install bootstrap
> ```

##### Good example

**Markdown**

````markdown
## Getting started

### Prerequisites

<!--
List all necessary dependencies, libraries, packages, programs, etc. here
that your project relies on.
-->

### Install

1. Clone this repository by executing the following command in your terminal or command line:

   ```sh
   git clone git@github.com:user/repo.git
   ```

2. Navigate into the folder in your terminal or command line with:

   ```sh
   cd the-project-folder
   ```

3. Install Bootstrap with the following command:
   ```sh
   npm install bootstrap
   ```
````

**Output**

> ## Getting started
>
> ### Prerequisites
>
> _Placeholder for list of dependencies and requirements_
>
> ### Install
>
> 1. Clone this repository by executing the following command in your terminal or command line:
>
>    ```sh
>    git clone git@github.com:user/repo.git
>    ```
>
> 2. Navigate into the folder in your terminal or command line with:
>
>    ```sh
>    cd the-project-folder
>    ```
>
> 3. Install Bootstrap with the following command:
>    ```sh
>    npm install bootstrap
>    ```

As the detailed steps in the good example above might look redundant to you, it certainly is not redundant for your collaborators. If your collaborators don't know anything about `npm` they will most certainly run into errors AFTER they have found out that they need to execute `npm install bootstrap` in the terminal or command prompt. So really make sure to explain every single step.

Key takeaways:

1. Explain everything
2. Give step-by-step tutorials
3. If something is already documented provide a link

#### Grammar and spelling

Remember that school and university are over? Even though you are in the real, practical world now this is not an excuse for you to forget about grammar, spelling rules and proper tenses. Since we are all human errors can happen from time to time. To avoid this in the best possible way either try to let another person proofread your documentation or [use Grammarly][grammarly-app] before publishing your documentation. Personally, I prefer the latter because it's fast and convenient.

The good part about not being in school and university anymore is that nobody dictates how many characters you have to write and which words you must not or have to use. People vote with their feet: If they don't like what you write they simply go away (or heavily criticize your documentation). It is your responsibility to find out what makes people engage with your content and adapt to that. You can either write your documentation dry and formal or make it a little more personal. You are the creator!

In my opinion, I enjoy reading documentations with a human touch. Whether the documentation has some emojis, anecdotal side stories or even emotional statements it makes the whole documentation more refreshing. The purpose of documentation is to be informative but sprinkling a little bit of personality on it makes the documentation less boring. But don't overdo it!

### Documentation tools

As your documentation grows bigger and bigger you might consider using a documentation tool at some point. Documentation tools like [Sphinx][sphinx], [Mkdocs][mkdocs] or [Gitbook][gitbook] offer you a convenient way to generate static HTML-files for your documentation. Among the open source community, [Read the Docs][read-the-docs] is very popular and commonly used. So instead of having your documentation in only one Markdown file documentation tools help you to create your own website specifically for your documentation. Furthermore, having a documentation website comes with the benefit of custom designs, navigation bar, sidebar, animations and so on - basically, everything that a website with HTML, CSS, and Javascript is capable of. You can even include a build job in your continuous integration pipeline to automate the HTML-file generation when you update your documentation. In my opinion, there is no golden rule on when to switch to a documentation tool since it is highly dependent on your project's scope. However, if your collaborators will have to scroll through your docs for more than a minute to get to the desired topic then you will probably know that it is time to split up your documentation and generate an own website for it. Basically, you will still have your `README.md` in your project's root folder with all the basic sections in it like `Table of contents`, `Getting started`, `Documentation`, `Contribution`, etc. but you will provide an external link to your documentation website under the section `Documentation` like in the good example below.

#### Bad Example

**Markdown**

```markdown
## Documentation

<!--
More than 500.000 lines of documentation. It's very messy and
collaborators will have to scroll all the way through.
-->
```

**Output**

> ## Documentation
>
> _Placeholder for 500.000 lines of documentation_

#### Good example

**Markdown**

```markdown
## Documentation

[Please find the orderly structured documentation of this project on our website.][documentation-link]
```

**Output**

> [documentation-link]: #
>
> ## Documentation
>
> [Please find the orderly structured documentation of this project on our website.][documentation-link]

### Highlighting

It's not enough to talk about your technical stuff only, you should include some code examples as well. While it might sound easy and self-explanatory there are a good amount of things to consider before posting any code blocks. Trust me, this isn't an easy thing and I have read lots of technical documentation that get this part wrong.

Make sure to use backticks `` to emphasize content, a line number, relevant parts of your code, or even a filename. You will also have to make sure that proper syntax highlighting is activated when you show multiple lines of code in one snippet. What might sound simple and logical to you is not for many software engineers because most of them expect collaborators to have the same knowledge about the project as they do (which is NEVER the case).

#### Code blocks

It's always good to show examples of important parts of your code. But how do you figure out what's important, what to include and how to do it in general? When including code blocks (= multiple lines of code) take the following points as a guideline:

1. The code must be syntax highlighted
2. The code in the snippet must be executable<sup>[\*][footnote-1]</sup>
3. The code in the snippet must deliver the desired result<sup>[\*][footnote-1]</sup>

<b id="footnote-1">\*</b> If placeholders in the code block are substituted.

Sounds easy? Let's take a look at the following examples with python:

##### Bad example

**Markdown**

````markdown
Connect to WebSocket server

```
my_websocket = WebSocket(
  host='localhost',
  port=9000
)
my_websocket.connect()
```
````

**Output**

> Connect to WebSocket server
>
> ```
> my_websocket = CustomWebSocket(
>   host='localhost',
>   port=9000
> )
> my_websocket.connect()
> ```

##### Good example

**Markdown**

````markdown
Execute the following code to successfully connect to the WebSocket server with the `CustomWebSocket`-class from our custom library `coolwebsocketlib`:

```python <!-- Notice this line here for syntax highlighting --->

import asyncio
from coolwebsocketlib import CustomWebSocket

async def example():
  my_websocket = CustomWebSocket(
    host='your-host-server', # For example: 'localhost'
    port='your-port-number'  # For example: 9000
  )
  await my_websocket.connect()

LOOP = asyncio.new_event_loop()
try:
    # Start the web socket connection and keep it open until aborted
    LOOP.create_task(example())
    LOOP.run_forever()
finally:
    LOOP.stop()
    LOOP.close()

```
````

**Output**

> Execute the following code to sucessfully connect to the WebSocket server with the `CustomWebSocket`-class from our custom library `coolwebsocketlib`:
>
> ```python
> import asyncio
> from coolwebsocketlib import CustomWebSocket
>
> async def example():
>   my_websocket = CustomWebSocket(
>     host='your-host-server', # For example: 'localhost'
>     port='your-port-number'  # For example: 9000
>   )
>   await my_websocket.connect()
>
> LOOP = asyncio.new_event_loop()
> try:
>     # Start the web socket connection and keep it open until aborted
>     LOOP.create_task(example())
>     LOOP.run_forever()
> finally:
>     LOOP.stop()
>     LOOP.close()
> ```

The first (bad) example totally lacks some crucial information. Imagine you had to set up the project with the first example only.

The second (good) example clearly mentions which libraries the collaborator needs to imported, gives a clear hint on how to fill the placeholder variables, provides code-specific syntax highlighting and shows that the crucial keywords `async` and `await` needs to be provided. If a collaborator was about to run this code block from above, no errors would occur.

#### Filenames & line numbers

Props to you when you even think of mentioning the filename where others can find a specific part of your code. Even more props to you when you include the line number. Now let's take a look at how to include and format these two things in your Markdown file:

##### Bad example

**Markdown**

```markdown
The WebSocket connection is established on line 420 in connection_handler.py

<!--
Your multiple lines of code (with syntax highlighting!!!!!!) goes here
-->

After you have established the connection you can subscribe to a state with the function subscribe_state() on line 123.

<!--
Another code block (with syntax highlighting!!!!!!)
-->
```

**Output**

> The WebSocket connection is established on line 420 in connection_handler.py
>
> _Placeholder for code block_
>
> After you have established the connection you can subscribe to a state with the function subscribe_state() on line 123.
>
> _Placeholder for code block_

##### Good example

**Markdown**

```markdown
The WebSocket connection is established on `line 420` in `connection_handler.py`

<!--
Your multiple lines of code (with syntax highlighting!!!!!!) goes here
-->

After you have established the connection you can subscribe to a state with the function `subscribe_state()` on `line 123`.

<!--
Another code snippet (with syntax highlighting!!!!!!)
-->
```

**Output**

> The WebSocket connection is established on `line 420` in `connection_handler.py`
>
> _Placeholder for code block_
>
> After you have established the connection you can subscribe to a state with the function `subscribe_state()` on `line 123`.
>
> _Placeholder for code block_

Do you notice how this makes a difference to the reader? With highlighting readers can more easily differentiate normal text from code relevant text.

While it might be overkill to provide every line number - also because they might change regularly - I consider the inclusion of line numbers whenever possible as good practice. Even if you do not include the line numbers make sure to **mention the filename and the described function names** at least.

### Real world examples

This section is dedicated to real world examples of good technical documentation and shall give you an understanding of the concept.

- [slack api][slack-api-doc]
- [traefik (GitHub)][traefik-doc]
- [DigitalOcean Product Documentation][digitalocean-doc]
- [How To Secure A Linux Server (GitHub)][secure-linux-server-doc]

Do you know more real world examples of good documentation? [Let me know](#contact) and I will list them above.

## Contribution

If you think this project lacks some further crucial information or you have some good advice, best-practices or crazy ideas feel free to submit a pull request or file an issue under [github.com/alex-lechner/documentation-guideline/issues][issue-tracker]

## Acknowledgement

<!-- | [![Alexander Lechner][alex-lechner-img]<br>Alexander Lechner][alex-lechner-link] |
| :------------------------------------------------------------------------------: | -->

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
