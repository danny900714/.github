# CONTRIBUTING GUIDELINES

🎉 Thanks for taking the time to contribute! 🎉

Before submitting your contribution, please make sure to take a moment and read through the following guidelines:

- [Code of Conduct](./CODE_OF_CONDUCT.md)
- [Reporting Issues](#reporting-issues)
  - [You have a problem](#you-have-a-problem)
  - [You have a suggestion](#you-have-a-suggestion)
- [Submitting Pull Requests](#submitting-pull-requests)
  - [Getting started](#getting-started)
  - [You have a solution](#you-have-a-solution)
  - [You have an addition](#you-have-an-addition)
- [AI/LLM Contributions Policy](#aillm-contributions-policy)
- [Use the Search, Luke](#use-the-search-luke)
- [Commit Guidelines](#commit-guidelines)
  - [Format](#format)
  - [Style](#style)

## Reporting Issues

### You have a problem

Please be so kind as to [search](#use-the-search-luke) for any open issue already covering
your problem.

If you find one, comment on it, so we know more people are experiencing it.

If not, you can go ahead and create an issue with as much detail as you can provide.
It should include the data gathered as indicated above, along with the following:

1. How to reproduce the problem
2. What the correct behavior should be
3. What the actual behavior is

Please copy to anyone relevant (e.g. plugin maintainers) by mentioning their GitHub handle
(starting with `@`) in your message.

We will do our very best to help you.

### You have a suggestion

Please be so kind as to [search](#use-the-search-luke) for any open issue already covering
your suggestion.

If you find one, comment on it, so we know more people are supporting it.

If not, you can go ahead and create an issue. Please copy to anyone relevant (e.g. plugin
maintainers) by mentioning their GitHub handle (starting with `@`) in your message.

## Submitting Pull Requests

### Getting started

You should be familiar with the basics of
[contributing on GitHub](https://help.github.com/articles/using-pull-requests) and have a fork
[properly set up](https://github.com/ohmyzsh/ohmyzsh/wiki/Contribution-Technical-Practices).

You MUST always create PRs with _a dedicated branch_ based on the latest upstream tree.

If you create your own PR, please make sure you do it right. Also be so kind as to reference
any issue that would be solved in the PR description body,
[for instance](https://help.github.com/articles/closing-issues-via-commit-messages/)
_"Fixes #XXXX"_ for issue number XXXX.

### You have a solution

Please be so kind as to [search](#use-the-search-luke) for any open issue already covering
your [problem](#you-have-a-problem), and any pending/merged/rejected PR covering your solution.

If the solution is already reported, try it out and +1 the pull request if the
solution works ok. On the other hand, if you think your solution is better, post
it with reference to the other one so we can have both solutions to compare.

If not, then go ahead and submit a PR. Please copy to anyone relevant (e.g. plugin
maintainers) by mentioning their GitHub handle (starting with `@`) in your message.

### You have an addition

Please be so kind as to [search](#use-the-search-luke) for any pending, merged or rejected Pull Requests
covering or related to what you want to add.

If you find one, try it out and work with the author on a common solution.

If not, then go ahead and submit a PR. Please copy to anyone relevant (e.g. plugin
maintainers) by mentioning their GitHub handle (starting with `@`) in your message.

For any extensive change, such as a new plugin, you will have to find testers to +1 your PR.

## AI/LLM Contributions Policy

AI tools can be pretty helpful for coding tasks, and we're not here to gatekeep how you get your work done. But here's the thing—this project is maintained by volunteers who do this in their spare time. We want to make sure we're spending our limited time effectively.

If you used AI tools meaningfully in your contribution (code generation, agentic coding assistants, etc.), please mention it in your PR description. Basic autocomplete doesn't count, but if an AI wrote substantial parts of your code, just let us know.

**Examples of good disclosure:**
- "Used ChatGPT to help generate the initial regex pattern for parsing git status output"
- "Claude assisted with writing the unit tests for this feature"  
- "Generated with Gemini and then reviewed/tested manually"
- Or simply: "AI-assisted" in your PR description

Here's what we're looking for:

- **You understand your code**: You should be able to explain what your contribution does and how it works. We want to collaborate with humans who are invested in the project.
- **Context matters**: Tell us what problem you're solving, how you tested it, and link to relevant docs. Small, incremental changes work better than massive generated overhauls.
- **Quality over quantity**: We'd rather have one thoughtful, well-tested contribution than ten AI-generated PRs that need extensive review.

The disclosure helps us know how much guidance to offer. If we're just reviewing AI output that you can't explain or improve, that changes the dynamic—and frankly, it's not a great use of anyone's time.

As always, we reserve the right to decline any contribution. Any submission that is in violation of this policy will be closed, and the submitter may be blocked from this repository without warning.

----

## Use the Search, Luke

_May the Force (of past experiences) be with you_

GitHub offers [many search features](https://help.github.com/articles/searching-github/)
to help you check whether a similar contribution to yours already exists. Please search
before making any contribution, it avoids duplicates and eases maintenance. Trust me,
that works 90% of the time.

If all fails, your thing has probably not been reported yet, so you can go ahead
and [create an issue](#reporting-issues) or [submit a PR](#submitting-pull-requests).

----

## Commit Guidelines

This project uses the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)
specification. The automatic changelog tool uses these to automatically generate
a changelog based on the commit messages. Here's a guide to writing a commit message
to allow this:

### Format

```
type(scope)!: subject
```

- `type`: the type of the commit is one of the following:

  - `feat`: new features.
  - `fix`: bug fixes.
  - `docs`: documentation changes.
  - `refactor`: refactor of a particular code section without introducing
    new features or bug fixes.
  - `style`: code style improvements.
  - `perf`: performance improvements.
  - `test`: changes to the test suite.
  - `ci`: changes to the CI system.
  - `build`: changes to the build system.
  - `chore`: for other changes that don't match previous types. This doesn't appear
    in the changelog.

- `scope`: section of the codebase that the commit makes changes to. If it makes changes to
  many sections, or if no section in particular is modified, leave blank without the parentheses.

- `!`: this goes after the `scope` (or the `type` if scope is empty), to indicate that the commit
  introduces breaking changes.

  Optionally, you can specify a message that the changelog tool will display to the user to indicate
  what's changed and what they can do to deal with it. You can use multiple lines to type this message;
  the changelog parser will keep reading until the end of the commit message or until it finds an empty
  line.

  Example (made up):

  ```
  style(agnoster)!: change dirty git repo glyph

  BREAKING CHANGE: the glyph to indicate when a git repository is dirty has
  changed from a Powerline character to a standard UTF-8 emoji. You can
  change it back by setting `ZSH_THEME_DIRTY_GLYPH`.

  Fixes #420

  Co-authored-by: Username <email>
  ```

- `subject`: a brief description of the changes. This will be displayed in the changelog. If you need
  to specify other details, you can use the commit body, but it won't be visible.

  Formatting tricks: the commit subject may contain:

  - Links to related issues or PRs by writing `#issue`. This will be highlighted by the changelog tool:
    ```
    ci: run release job when pushing tags (#3)
    ```

  - Formatted inline code by using backticks: the text between backticks will also be highlighted by
    the changelog tool:
    ```
    docs: add `CONTRIBUTING.md`
    ```

### Style

Try to keep the first commit line short. It's harder to do using this commit style but try to be
concise, and if you need more space, you can use the commit body. Try to make sure that the commit
subject is clear and precise enough that users will know what changed by just looking at the changelog.
