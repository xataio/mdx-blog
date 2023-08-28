This repository contains the blog content for xata.io.

## Contributing

### Linting

There's a hefty dose of linting through `eslint`, `prettier` and `remark`. If you'd like to see lint errors as you work run `pnpm install` as you work. `husky` should make checks on your commits. Similarly, there are GitHub actions that will run on PRs to this repo.

### Frontmatter

Each MDX document needs to include the following frontmatter at the top of the page. Most fields should be self-explanatory. The `blog.schema.yaml` file defines its shape.

```yaml
---
title: 'Build Next.js apps with JWT authentication, Auth.js, and Xata'
description: 'Use Xata and Auth․js on two Next․js apps: app directory and pages directory.'
image:
  src: https://raw.githubusercontent.com/xataio/mdx-blog/main/images/xata-authjs-nextjs.png
  alt: Xata and ChatGPT logos
ogImage: https://user-images.githubusercontent.com/2750668/263696819-1d1c6978-4095-4442-ba6b-cd07c988c14a.jpg
author: Attila Fassina
date: 03-23-2023
published: true
slug: xata-authjs-nextjs
---
```

#### Slugs

The `slug` field should be written without the `/blog/` prefix and should not contain a forward slash, both of which will be added programmatically.

#### published

Setting this to false will deploy the blog post live to the website, but will hide it from the `/blog` index and any associated feeds (like RSS).

## Images

For now, images need to be absolute URLs that point to their raw URL on GitHub. In a future build of the website, relative images will be pushed to Xata directly.

### Code syntax

Snippets can have the following syntax on the first line to enable various abilities

    tsx  title="my/file.tsx" showLineNumbers {3-5,7} /highlightWord/
