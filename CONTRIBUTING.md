# Contributing to this blog

This blog is Jekyll-based, and supports multiple authors.

Jekyll references:

* http://jekyllrb.com/docs/structure/
* http://jekyllrb.com/docs/permalinks/

## Post as yourself

a) Make sure you are listed in `_data/authors.yml`
b) Specify yourself as the `author:`  in the post's frontmatter

## Use tags

Specify `tags:` in the post's frontmatter as an array:
```
tags: [fun, profit]
```

## Saving drafts

Create draft (unpublished) posts in the `_drafts` folder. The file name should be a URL-friendly filename with no leading date.

## Publishing posts

Posts should be moved to `_posts` when ready for publication. The naming convention of these files is important, and must follow the format: YEAR-MONTH-DAY-title.md
