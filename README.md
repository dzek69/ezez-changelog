# EZEZ Changelog

**version 1.0.0**

> This work is based on [keepachangelog.com](https://keepachangelog.com/en/1.1.0/), created by [Olivier Lacan](https://olivierlacan.com) and MIT licensed.

## What is a changelog?
A changelog is a file which contains a curated, chronologically ordered list of notable changes for each version of a project.

## Why keep a changelog?
To make it easier for users and contributors to see precisely what notable changes have been made between each release (or version) of the project.

## Who needs a changelog?
People do. Whether consumers or developers, the end users of software are human beings who care about what's in the software. When the software changes, people want to know why and how.

## How do I make a good changelog?

### Changelogs are for humans, not machines.
Changelogs are useful for both end products (like applications, where end user can be a non-tech person) and
libraries (where end user is a developer).
However, changelog should not state internal changes that are not relevant to the end user,
even if they are a developer.
Rewriting a class, refactoring a function, changing a private variable name, adding a unit test is something you could
state in a commit message, but not in a changelog.

### Guiding Principles
- There should be an entry for every single version,
- The same types of changes should be grouped,
- Order the groups from most important in given release to least important,
- Order the changes in each group by importance as well,
- Versions and sections should be linkable,
- The latest version comes first,
- The release date of each version is displayed,
- Mention whether you follow [Semantic Versioning](https://semver.org/) or not, do not omit this information, explicitly
state it.

### Types of changes

- `Added` for new features,
- `Changed` for changes in existing functionality that are not breaking,
- `Breaking` for changes which break existing functionality,
- `Removed` for removed features,
- `Fixed` for any bug fixes,
- `Dev` for internal changes that may not be relevant to the end user, but they are worth mentioning (like huge
performance optimization that **really** changes everything).

## How can I reduce the effort required to maintain a changelog?

Add an `Unreleased` section at the top to track upcoming changes.

This serves two purposes:
- People can see what changes they might expect in upcoming releases,
- At release time, you can move the `Unreleased` section changes into a new release version section,
but remove the `Unreleased` section when there are no changes yet to be released to avoid confusion.

## What about yanked releases?

Yanked releases are versions that had to be pulled because of a serious bug or security issue. Often these versions don't even appear in change logs. They should. This is how you should display them:
`## [0.0.5] - 2014-12-13 [YANKED]`
The `[YANKED]` tag is loud for a reason. It's important for people to notice it. Since it's surrounded by brackets it's also easier to parse programmatically.

## Can changelogs be bad?

See [Can changelogs be bad?](https://keepachangelog.com/en/1.1.0/#bad-practices) section on `keepachangelog.com`.

## FAQ

See [FAQ](https://keepachangelog.com/en/1.1.0/#frequently-asked-questions) section on `keepachangelog.com`.

## Differences from `keep a changelog`

> Introduced differences are based on my personal preferences and experience. They are opinionated just like the
> original (see the last FAQ entry of the original).

- Emphasized "Changelogs are for humans, not machines", making it a separate section and adding more detailed explanation
- Guiding Principles: added points on ordering of groups and changes,
- Guiding Principles: asked for explicit Semantic Versioning declaration,
- Removed types of changes:
  - `Deprecated` (I find no use for that, use `Changed` section instead),
  - `Security` (usually `Fixed` section is right place for that),
- Added types of changes:
  - `Breaking` (I do not consider every change a breaking change, i.e.: docs update, displaying different time format in an application),
  - `Dev` (explained in [Types of changes](#types-of-changes) section),
- Extracted section about yanked releases from FAQ.

## License

MIT
