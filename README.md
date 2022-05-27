# Upcards - A Simple Card-Based Hugo Theme

See [`gfngfn.github.io`](https://gfngfn.github.io/) for example.

**Note: this Hugo theme is currently developed solely for the developer’s personal use.** Feel free to use it, but please note that its functionality and appearance are subject to change.


## Expected Usage

Upcards expects the configuration to be like the following:

```
disableKinds = ["RSS", "taxonomy", "section"]
ignoreErrors = ["error-disable-taxonomy"]

[taxonomies]
  tag = 'tags'

defaultContentLanguage = ...
[languages]
  ...
```

i.e., it expects the tag to be the sole taxonomy and the pages for taxonimies or sections to be disabled.


## Theme-specific Configuration Parameters

### `lastmodPre`/`lastmodPost`

The prefix/suffix for displaying last modified datetimes.

Example:

```toml
...
[languages]
  [languages.en]
    ...
    lastmodPre = "(last modified: "
    lastmodPost = ")"
...
```

### `tocHeading`

The title for the Table of Contents (see also the shortcode `{{< toc >}}`). Default: `"Contents"`


## Theme-specific Front Matter Parameters

### `thumbnail`

The path to the thumbnail image relative to `$YOUR_SITE_REPO/static`. No thumbnail image will be displayed if omitted.


### `math`

Enables rendering of math formulae using KaTeX if set. Math formulae are supposed to be written like the following:

````
The attractive force \\(F\\) between two point-like bodies satisfies:

```
\begin{align*}
F = G \frac{M m}{R^2}
\end{align*}
```

where \\(G\\) is the gravitational constant.
````


### `pageType`

The page type (`"normal"`, `"slides"`, or `"image"`). Default: `"normal"`


### `slidePath`

The path to the PDF file for slides relative to `$YOUR_SITE_REPO/static`. Effective and mandatory when `pageType = "slides"`.

Example:

```yaml
thumbnail: "/media/thumbnail-of-your-slides.png"
pageType: "slides"
slidePath: "/media/slides.pdf"
```


### `showTitleOnCard`

Effective when `pageType = "slides"`. Titles of presentations will be displayed on cards if this option is set. Default: `false` (i.e. titles are not displayed on slide cards)


### `imagePaths`

The list of paths to the image files relative to `$YOUR_SITE_REPO/static`. Effective when `pageType = "image"`.


## Theme-specific Shortcodes

### `{{< toc >}}`

Inserts the Table of Contents. The resulting listing will be shown on where `{{< toc >}}` is written if the screen is relatively narrow (specifically, narrower than 1250px; e.g. smartphone screens), or on the right corner of the viewport otherwise (e.g. display devices for desktop PCs).


### `{{< github-repo user="…" repo="…" >}}`

Displays a card of a GitHub repository by using [`gh-card.dev`](https://gh-card.dev).

Example:

```
{{< github-repo user="gfngfn" repo="hugo_theme_upcards" >}}
```

<img src="https://gh-card.dev/repos/gfngfn/hugo_theme_upcards.svg" />


## Dependencies and Their License

Upcards depends on the following libraries:

- [The Bootstrap Authors](https://github.com/twbs/bootstrap/graphs/contributors). [Bootstrap v5.0.2](https://getbootstrap.com/). Licensed under MIT, 2011-2021.
- Cole Bemis. [Feather](https://feathericons.com/). Licensed under MIT, 2013-2017.
- David DeSandro. [Masonry v4.2.2](https://masonry.desandro.com/). Licensed under MIT, 2022.
- Mozilla Foundation. [PDF.js](https://mozilla.github.io/pdf.js/). Licensed under the Apache License (Version 2.0), 2022.
- Khan Academy and other contributors. [KaTeX](https://katex.org/). Licensed under MIT, 2013-2020.
