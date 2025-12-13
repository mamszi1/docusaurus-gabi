---
slug: automating-documentation-quality
title: Why I Treat My Documentation Like Code
authors: [me]
tags: [docusaurus, ci-cd, github-actions, docs-as-code]
date: 2025-12-13
---

We often talk about code quality, unit tests, and linting for our software. But what about the documentation?

`<!-- truncate -->`

Recently, I realized that **broken links and typos damage user trust just as much as a runtime error.** That's why I decided to upgrade my Docusaurus workflow to include automated quality checks.

## The Problem: "It worked on my machine"

I love Docusaurus for its speed and flexibility. However, as my documentation grew, I started noticing small issues slipping through:

* Links pointing to moved files.
* Images that failed to load because of a typo in the path.
* Embarrassing spelling mistakes in titles.

I realized I was treating documentation as a static asset, not as a dynamic project that needs testing.

## The Solution: CI for Docs

I implemented a GitHub Actions workflow that treats my docs exactly like my code. Now, every time I push to the `main` branch or open a Pull Request, a series of checks run automatically.

### 1. Zero Tolerance for Broken Links

I configured `docusaurus.config.js` to be strict:

```javascript
onBrokenLinks: 'throw',
onBrokenMarkdownLinks