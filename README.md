# Game On! blog

Customized github minimal theme. Built using Docker to avoid the annoyance of maintaining a local ruby development environment (with apologies to lovers of Ruby).

## Updating/Running jekyll

```
docker-compose build
docker-compose up
```

This will perform any updates to the gemfile and start jekyll listening on port 4000.

The `--drafts` option is included, so you will see any draft posts.
