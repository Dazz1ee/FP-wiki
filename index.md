---
title: Home
layout: home
---

# Типы данных представления синтаксического дерева
## [Token](https://github.com/MAILabs-Edu-2024/fp-compiler-lab-the-best-team/blob/f726a221d576b1aa7b6d6f6b206b76c1fb59af74/Program.fs#L6)
`Token` определяет различные типы токенов, которые могут быть обнаружены в выражении
## [Expr](https://github.com/MAILabs-Edu-2024/fp-compiler-lab-the-best-team/blob/f726a221d576b1aa7b6d6f6b206b76c1fb59af74/Program.fs#L19)
Синтаксическое дерево составляется путем организации узлов типа `Expr` в соответствии 
с правилами синтаксиса языка программирования. Например, операторы и их операнды объединяются в узлы типа 
`OPERATOR`, условные выражения представляются узлами типа `COND`, а функции и их вызовы создают узлы 
типа `FUNC_DEF` и `CALL` соответственно.

1. click "[use this template]" to create a GitHub repository
2. go to Settings > Pages > Build and deployment > Source, and select GitHub Actions

If you want to maintain your docs in the `docs` directory of an existing project repo, see [Hosting your docs from an existing project repo](https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md#hosting-your-docs-from-an-existing-project-repo) in the template README.

----

[^1]: [It can take up to 10 minutes for changes to your site to publish after you push the changes to GitHub](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll#creating-your-site).

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
