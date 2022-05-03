# Upcards - A Simple Card-Based Hugo Theme

**Note: this Hugo theme is currently developed solely for the developer’s personal use.**


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


## Dependencies

Upcards contains the following, all of which are licensed under The MIT License:

- Bootstrap
- Feather
- Masonry
