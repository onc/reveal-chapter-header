# reveal.js chapter-headers

Just a little project for adding the current chapter to a presentation.
I like to use Markdown for creating presentations using reveal.js.

But i would like to have the current chapter in the header of the presentation, so i wrote this little plugin.
This is just a quick hack to get done, what i was looking for.

## Usage

To use this plugin you have to structure your `index.html` as follows:

```
div class="slides" data-title="Foo">
  <section data-markdown="foo.md"
           data-separator="^\n\n\n"
           data-separator-vertical="^\n\n"
           data-separator-notes="^Note:"
           data-charset="utf-8">
  </section>
/div>

div class="slides" data-title="Bar">
  <section data-markdown="bar.md"
           data-separator="^\n\n\n"
           data-separator-vertical="^\n\n"
           data-separator-notes="^Note:"
           data-charset="utf-8">
  </section>
/div>
```

All `section`s included in a `slides`-div are considered to be in the same chapter.

## Installation

- Put the `chapter-headers` folder into the `plugin` folder of your reveal-project.
- Add the following line to the `head` of your `index.html`.

```
<link rel="stylesheet" href="plugin/chapter-header/chapter-header.css">
```

- Add the following line to the `dependencies` section on the bottom of your `index.html`

```
{ src: 'plugin/chapter-header/chapter-header.js', async: true, callback: function() { chapterHeader.init(); } }
```

## Preview

![screenshot](https://raw.githubusercontent.com/onc/reveal-chapter-headers/master/preview.png)
