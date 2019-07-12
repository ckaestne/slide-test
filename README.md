# Markdown Slides Testbed

Basic setup for creating slides with markdown.

Using a slightly patched version of `reveal-md` ([original version](https://github.com/webpro/reveal-md), [patched version](https://github.com/ckaestne/reveal-md)) which is based on `reveal.js` ([github](https://github.com/hakimel/reveal.js/)). 

## Usage

Each slide deck is in a separate subdirectory. Can use all the usual markdown features of `reveal.js` plus a few custom ones created with scripts in the `_assets` directory.

Basics:
* Slide separators are `---` for chapters and `----` for slides within a chapter.

Custom extensions in `/_assets/plugin/mymarkdown.js`:
* `<!-- small -->`, `<!-- smaller -->`, and `<!-- smallish -->` can be used to adjust font sizes in a slide
* `<!-- split -->` can be used to make a two column slide
* Explicit column handling, included nested columns and more than two columns, is possible between `<!-- colstart -->` and `<!-- colend -->` with `<!-- col -->` as the separator
* `<!-- fit -->` in a title tries to make long titles fit to a slide by scaling it down
* Empty items in a list can be used as a space/separator between two list
* `<!-- left -->` and `<!-- right -->` change the alignment
* Mermaid diagrams can be integrated with a code blog in the `mermaid` language

## Reveal-md patch

Some smaller changes to `reveal-md` were necessary, primarily to update to a newer version of `reveal.js` which had a necessary newer version of the markdown parser and some minor changes in file handling.

## Editing

Run `reveal-md . --watch` to run a local webserver that shows the slides and automatically updates on changes to the .md files.

## Static sites and circle-CI automation

To produce static slides, run `reveal-md . --static` (or `npm run generate`). The slides will be created in the `_static` directory. Circle-ci automates the process and pushes the results to the `gh-pages` branch.

