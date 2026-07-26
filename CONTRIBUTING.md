<!--lint disable alphabetize-lists-->

# Contributing

Your contributions are always welcome!

## Guidelines

- Add one link per commit.

- Add one commit per Pull Request.

- Add the link: `- [project-name](http://example.com/) — A short description ends with a period.`

  - Keep descriptions concise, maximum number of characters is 350.
  - Each entry must be a real, current project, paper, or resource. Verify it against the actual repository, package page, or publisher listing before submitting — don't rely on memory.
  - Prefer open-source projects; a commercial tool, textbook, or paper is only accepted where there's no comparable OSS equivalent, or where it's a recognized canonical/historical reference (papers, textbooks, and standards are judged by continued citation and relevance rather than "maintenance").
  - Software should show a commit or release within the last ~24 months to count as actively maintained. Fuzzy logic moves slower than mainstream ML, so a quiet-but-stable, still-functional, widely-cited tool is also acceptable — say so explicitly if you're relying on that allowance.

- Add a section or subsection if needed.

  - Add the section description.
  - Add the section title to the `$ ls ./sections` table of contents.

- Search previous suggestions before making a new one, as yours may be a duplicate.

- Check your spelling and grammar.

- Remove any trailing whitespace.

- Send a Pull Request with the reason why the project is worth including.

- Make sure the tests are passing.

## Styleguide

We use [`remark-lint`](https://github.com/remarkjs/remark-lint) to validate the style of `README.md` and `CONTRIBUTING.md`. Lint configuration lives in `.remarkrc`.

Refer to the [remark-lint rule docs](https://github.com/remarkjs/remark-lint#rules) when in doubt.

## Scope

This list started at roughly 50 entries and favors depth and verification over exhaustiveness. A genuinely thin section (for example, the current `JavaScript` subsection) reflects an honest gap in the ecosystem, not an oversight — please don't pad it with unmaintained or off-topic packages just to fill space.

## Testing

To run tests locally you will need [Node.js](https://nodejs.org/) installed, then:

```shell
$ npm install
$ npm test
```
