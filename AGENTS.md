# AGENTS.md

## Cursor Cloud specific instructions

### What this repository is

This is a **docs-only repository**: a static Markdown wiki / curated link index in the
style of FMHY ("FreeMediaHeckYeah"). The entire tracked content is two Markdown files,
`README.md` and `fmhy.md` (currently byte-for-byte identical). There is **no application
code, no package manager, no build system, no tests, no linters, and no CI**.

### Environment / dependencies

- There is nothing to install. The dependency-refresh update script is intentionally a
  no-op. Do not add a package manager or build tooling unless the task explicitly
  introduces an application.
- Everything needed for the natural workflow (editing Markdown) is available out of the
  box: `git`, plus `python3`, `node`, and Google Chrome are pre-installed if you want to
  render/preview.

### Developing / "running" the wiki

The dev workflow is simply: edit a `.md` file, then preview the rendered result. There is
no committed site generator. To preview locally without adding any repo dependency, render
the Markdown with a throwaway harness (do **not** commit it), e.g.:

```bash
# one-off local preview (files live outside the repo so they are never committed)
mkdir -p /tmp/wiki-preview && cd /tmp/wiki-preview
curl -s -o marked.min.js https://cdn.jsdelivr.net/npm/marked/marked.min.js
cp /workspace/README.md .
# create an index.html that fetch()es README.md and calls marked.parse(), then:
python3 -m http.server 8099
# open http://localhost:8099/ in Chrome
```

Reloading the browser after editing the Markdown re-renders the page — that is the full
edit → preview loop for this repo.

### Notes

- The public site (`fmhy.net`) is generated from the upstream `fmhy/edit` VitePress project,
  which is **not** part of this repository. Do not clone/commit that tree here unless a task
  explicitly asks for it.
- Since there are no tests/lint/build, "verification" for content changes means confirming
  the Markdown renders correctly and links are well-formed.
