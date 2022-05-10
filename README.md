# Upcards - A Simple Card-Based Hugo Theme

**Note: this Hugo theme is currently developed solely for the developer’s personal use.** Feel free to use it, but please note that its functionality and appearance are subject to change.


## Expected Usage

Upcards expects the configuration to be like the following:

```
disableKinds = ["RSS", "taxonomy", "section"]
ignoreErrors = ["error-disable-taxonomy"]

[taxonomies]
  tag = 'tags'

[permalinks]
  posts = '/posts/:year/:month/:day/:filename/'
```

i.e., it expects the tag to be the sole taxonomy and the pages for taxonimies or sections to be disabled.


## Dependencies and Their License

Upcards depends on the following libraries:

- [The Bootstrap Authors](https://github.com/twbs/bootstrap/graphs/contributors). [Bootstrap v5.0.2](https://getbootstrap.com/). Licensed under MIT, 2011-2021.
- Cole Bemis. [Feather](https://feathericons.com/). Licensed under MIT, 2013-2017.
- David DeSandro. [Masonry v4.2.2](https://masonry.desandro.com/). Licensed under MIT, 2022.
- Mozilla Foundation. [PDF.js](https://mozilla.github.io/pdf.js/). Licensed under the Apache License (Version 2.0), 2022.
