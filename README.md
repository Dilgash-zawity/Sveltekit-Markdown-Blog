# Sveltekit Markdown Blog

## Getting Started

1. Clone the repository:

   ```bash
   git clone [repository_url]
   ```

2. Install the dependencies:

   ```bash
   npm install
   ```

3. Start the development server:

   ```bash
   npm run dev
   ```

## Adding Posts

Inside the `posts` folder, you can add any `.md` file. Each file must start with the following frontmatter:

```markdown
---
title: [title]
description: [description]
date: '[date]'
categories:
  - [category1]
  - [category2]
  - [category3]
published: [true or false]
---
```

Replace the placeholders with your content. For example:

```=
---
title: "My First Blog Post"
description: "This is a description of my first blog post."
date: '2024-07-24'
categories:
  - "SvelteKit"
  - "Markdown"
  - "Blog"
published: true
---
```

## Configuring Languages

In `svelte.config.js`, configure the languages for syntax highlighting as follows:

```javascript
langs: ['javascript', 'typescript']
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
# Sveltekit-Markdown-Blog
# Sveltekit-Markdown-Blog
