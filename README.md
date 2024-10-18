# Chuyan's Fork of Hook

This is a fork of [hook](https://github.com/InputUsername/zola-hook.git), which was created by Koen Bolhuis. This fork includes certain modifications and functions for myself.

## Changes made in this fork

- Added KaTeX support for formulas.
  Note that Zola will escape `&` into `&amp;` which disrupts a multi-line formula environment if alignment is used. The easist way to mitigate that is to wrap your `$$` with a pair of `<p></p>` so that Zola treats content inside as raw HTML and keeps it intact.
- Added page percentage calculation and "back to top" button.
- Added "should-invert" in CSS so that images could go inverted with theme change.
- Added "side-by-side-container" in CSS to allow horizontally centered multiple images arranged size by side.
  Note that to use these CSS styles you need (for now) to write raw HTML :(
- Changed default fonts.
- Changed CSS styles.
- Changed 404 page (just for stylish reason).

--------

# Original README

Below is the original README file from [hook](https://github.com/InputUsername/zola-hook.git) by the time this fork was created.

--------

# Hook

A clean and simple personal site/blog theme for [Zola](https://getzola.org).

[Demo](https://inputusername.github.io/zola-hook/)

## Setup

Clone this repo into your `themes` folder:
```sh
cd themes
git clone https://github.com/InputUsername/zola-hook.git hook
```

Then, enable it in your `config.toml`:
```toml
theme = "hook"
```

## Features

The following templates are built-in:
- `index.html` - the homepage;
- `page.html` - pages and posts (extends `index.html`);
- `section.html` - archive of pages in a section, mostly for a blog (extends `page.html`);
- `404.html` - 404 page (extends `page.html`).

Templates have the following Tera blocks:
- `title` - to override the default `<title>` (`config.title`);
- `extra_head` - to override styles and anything else in `<head>`;
- `header` - to change the header (best to put this in a `<header>`);
- `content` - to change the content (best to put this in a `<main>`).

You can define links to include in the header on the homepage in `config.toml`:
```toml
[extra]

links = [
    { title = "Link display text", href = "http://example.com" },
    # ...
]
```

Pages in the root section can define `extra.in_header = true` to be included in the header links on the homepage.

The content in the root `_index.md` is included in the homepage if present.

Below that is a list of the 20 most recent posts. For this, the `blog/_index.md` section is expected to exist
(will error if it doesn't exist). There is also a link to an archive of all blog posts by year.

Hook supports light/dark mode based on the user's preference. There is also a manual toggle button
(requires JavaScript).

## Screenshots

### Homepage

![Homepage](screenshot.png)

### Blog post
![Blog post](screenshot2.png)

### Blog archive
![Blog archive](screenshot3.png)

### Dark mode
![Dark mode](screenshot4.png)

## License

MIT license, see [`LICENSE`](https://github.com/InputUsername/zola-hook/blob/main/LICENSE).
