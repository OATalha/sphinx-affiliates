# sphinx-affiliates

[![Github-CI][github-ci]][github-link]
[![Coverage Status][codecov-badge]][codecov-link]
[![PyPI][pypi-badge]][pypi-link]

Allow search to include documents from more than one [Sphinx
documentation](http://www.sphinx-doc.org) html site. This is useful when
you have a number of github repositories under one org, are using sphinx
to build documentation for all of them, and [github
pages](https://pages.github.com/) to serve the artifacts. When you configure
a [custom domain](https://docs.github.com/en/github/working-with-github-pages/about-custom-domains-and-github-pages),
say `https://my.site.org`, for one repo in the org, any other repo's github pages
(say repo2) will be visible as `https://my.site.org/repo2`. But the
`search.html` from the sites will not know about eachother: they will be
completely independent. This extension will solve that by
- changing the search engine to allow loading more than one index
- changing the search index generation process to generate an additional index
- add configuration options to add the additional indices, from affiliate
  sites, to the `search.html` page.

