# OpenCore Docs Hub Maintenance Guide

This document explains how to add, update, or remove an external documentation source in the OpenCore Docs Hub.

The hub code is located in:

```text
hackinos-website/assets/js/opencore-hub.js
```

The external-source configuration is the `SOURCES` object near the beginning of that file.

## Important principles

- Only use public repositories or documentation sources that permit public viewing.
- Keep the original repository and source link visible in the reader.
- Do not present upstream documentation as original HackinOS content.
- Test every raw Markdown path before publishing.
- Prefer a small, verified navigation list over a large list of broken links.
- Use the repository's actual default branch: commonly `main` or `master`.

## Add a new source

Add a new object inside `SOURCES`.

```js
example: {
  label: "Example Documentation",
  rawBase: "https://raw.githubusercontent.com/OWNER/REPOSITORY/main/",
  sourceBase: "https://github.com/OWNER/REPOSITORY/blob/main/",
  groups: [
    {
      title: "Overview",
      items: [
        {
          icon: "⌂",
          title: "Introduction",
          file: "README.md"
        }
      ]
    }
  ]
}
```

Then add the source to the selector in:

```text
hackinos-website/guides-opencore.html
```

```html
<option value="example">Example Documentation</option>
```

## Add a page to an existing source

Add an item inside one of the source groups:

```js
{
  icon: "▣",
  title: "Page title shown in the sidebar",
  file: "relative/path/to/file.md"
}
```

Example:

```js
{
  icon: "⚙",
  title: "Configuration reference",
  file: "docs/configuration.md"
}
```

The `file` value must be relative to the repository root.

## Test raw Markdown first

Before adding a navigation item, open its raw URL in a browser:

```text
https://raw.githubusercontent.com/OWNER/REPOSITORY/main/relative/path/to/file.md
```

A correct URL displays the Markdown text.

A `404: Not Found` response means one of these is wrong:

- Repository owner or repository name
- Branch name
- Folder path
- File name
- Letter case

## Images and internal links

The Docs Hub resolves Markdown relative images and links based on the source document path.

For best results:

- Use normal relative Markdown image paths, such as `images/example.png`.
- Use normal relative Markdown links, such as `../README.md`.
- Keep pages that should open in the internal reader listed in the same source navigation.
- Links to pages not listed in the sidebar will open the upstream source directly in a new browser tab.

## Add a new source safely

1. Add the new source object to `SOURCES`.
2. Add only one known working Markdown file, usually `README.md`.
3. Add the `<option>` to `guides-opencore.html`.
4. Run `bundle exec jekyll serve --livereload`.
5. Select the new source in the Docs Hub.
6. Verify the source link, Markdown rendering, images, and code-copy button.
7. Add more sidebar pages after the first page is confirmed.