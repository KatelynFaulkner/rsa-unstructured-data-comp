# Contributing to rsa-unstructured-data-comp
This outlines how to propose a change to rsa-unstructured-data-comp.

## Fixing typos
You can fix typos, spelling mistakes, or grammatical errors in the documentation directly using the GitHub web interface, as long as the changes are made in the source file. This generally means you’ll need to edit roxygen2 comments in an .R, not a .Rd file. You can find the .R file that generates the .Rd by reading the comment in the first line.

## Bigger changes
If you want to make a bigger change, it’s a good idea to first file an issue and make sure someone from the team agrees that it’s needed. If you’ve found a bug, please file an issue that illustrates the bug with a minimal reprex (this will also help you write a unit test, if needed).

## Pull request process
Fork the package and clone onto your computer. If you haven’t done this before, we recommend using usethis::create_from_github("batpigandme/tidyverse", fork = TRUE).

Install all development dependences with devtools::install_dev_deps(), and then make sure the package passes R CMD check by running devtools::check(). If R CMD check doesn’t pass cleanly, it’s a good idea to ask for help before continuing.

Create a Git branch for your pull request (PR). We recommend using usethis::pr_init("brief-description-of-change").

Make your changes, commit to git, and then create a PR by running usethis::pr_push(), and following the prompts in your browser. The title of your PR should briefly describe the change. The body of your PR should contain Fixes #issue-number.

For user-facing changes, add a bullet to the top of NEWS.md (i.e. just below the first header). Follow the style described in https://style.tidyverse.org/news.html.

## Code style
New code should follow the tidyverse style guide. You can use the styler package to apply these styles, but please don’t restyle code that has nothing to do with your PR.

We use roxygen2, with Markdown syntax, for documentation.

We use testthat for unit tests. Contributions with test cases included are easier to accept.

# Code of Conduct
Please note that the tidyverse project is released with a [Contributor Code of Conduct](https://github.com/KatelynFaulkner/rsa-unstructured-data-comp/blob/main/.github/CODE_OF_CONDUCT.md). By contributing to this project you agree to abide by its terms.
