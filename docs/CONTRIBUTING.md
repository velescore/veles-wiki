# Contributing to Veles Wiki

This document explains the practical process and guidelines for contributing.We recommend read the [Veles Wiki documentation](https://github.com/mdfkbtc/veles-wiki/blob/master/docs/README.md) to learn more about the syntax and about writing Veles Core Wiki articles.

## Contributor Workflow

The codebase is maintained using the "contributor workflow" where everyone
without exception contributes patch proposals using "pull requests". This
facilitates social contribution, easy testing and review.

To contribute a patch, the workflow is as follows:

  1) **Fork repository [only the first time](https://help.github.com/en/articles/fork-a-repo)**.
  2) **Create topic branch**
  3) **Commit patches**

In general [commits should be atomic](https://en.wikipedia.org/wiki/Atomic_commit#Atomic_commit_convention)
and diffs should be easy to read. For this reason do not mix any formatting
fixes or code moves with actual code changes.

Commit messages should be verbose by default consisting of a short subject line
(50 chars max), a blank line and detailed explanatory text as separate
paragraph(s), unless the title alone is self-explanatory (like "Corrected typo
in Home.md") in which case a single title line is sufficient. Commit messages should be
helpful to people reading your code in the future, so explain the reasoning for
your decisions. Further explanation [here](https://chris.beams.io/posts/git-commit/).

If a particular commit references another issue, please add the reference. For
example: `refs #1234` or `fixes #4321`. Using the `fixes` or `closes` keywords
will cause the corresponding issue to be closed when the pull request is merged.

Commit messages should never contain any `@` mentions.

Please refer to the [Git manual](https://git-scm.com/doc) for more information
about Git.

  1) **Push changes to your fork**
  2) **Create pull request**
  
The title of the pull request should be prefixed by the component or area that
the pull request affects. Valid areas as:

  - `doc` for changes to the documentation
  - `articles` for changes to articles
  - `images` for changes to images
  - `translation` for add new translation

Examples:

    doc: Add CONTRIBUTING.md
    articles: Fix typo for 'en' Masternode-Setup-Guide.md 
    images: Add new image for Home.md
    translation: Translate dVPN-Setup-Guide.md to English  

The body of the pull request should contain enough description about what the
patch does together with any justification/reasoning. 

## Squashing Commits

If your pull request is accepted for merging, you may be asked by a maintainer
to squash and or [rebase](https://git-scm.com/docs/git-rebase) your commits
before it will be merged. The basic squashing workflow is shown below.

    git checkout your_branch_name
    git rebase -i HEAD~n
    # n is normally the number of commits in the pull request.
    # Set commits (except the one in the first line) from 'pick' to 'squash', save and quit.
    # On the next screen, edit/refine commit messages.
    # Save and quit.
    git push -f # (force push to GitHub)

Please update the resulting commit message if needed, it should read as a
coherent message. In most cases this means that you should not just list the
interim commits.

If you are facing some issues or need help, please contact support on [Discord](https://discord.gg/P528fGg) and they will assist you. 