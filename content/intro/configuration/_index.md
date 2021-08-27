---
title: Doc's configuration
---

### Configuration options for this documentation page

Here are some features of this theme, that might be useful to use in content. This should be for quick reference to not always look into this themes [documentation](https://geekdocs.de/) and [source code](https://github.com/thegeeklab/hugo-geekdoc/tree/main/exampleSite).

## Build ToC for file tree

```tpl
{{</* toc-tree */>}}
```

## Columns

```html
{{</* columns */>}} <!-- begin columns block -->
# Left Content
Dolor sit, sumo unique argument um no ...

<---> <!-- magic sparator, between columns -->

# Mid Content
Dolor sit, sumo unique argument um no ...

<---> <!-- magic sparator, between columns -->

# Right Content
Dolor sit, sumo unique argument um no ...
{{</* /columns */>}}
```

## Expand

```tpl
{{</* expand "Custom Label" "..." */>}}
## Markdown content
Dolor sit, sumo unique ...
{{</* /expand */>}}
```

## Hints

```tpl
{{</* hint [info|warning|danger] */>}}
**Markdown content**\
Dolor sit, sumo unique argument um no. Gracie nominal id xiv. Romanesque acclimates investiture.
 Ornateness bland it ex enc, est yeti am bongo detract re.
{{</* /hint */>}}
```
