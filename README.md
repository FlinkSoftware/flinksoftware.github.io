# flinksoftware.com

Static site built with Jekyll and Tailwind CSS, hosted on GitHub Pages from the `docs/` folder.
GitHub Pages builds the HTML on push; the CSS in `docs/css/app.css` is compiled locally and committed.

## Requirements

- Node.js 20+
- Ruby 3.3, the version GitHub Pages uses. The Ruby bundled with macOS (2.6) is too old, and the
  `github-pages` gem does not support Ruby 4 yet. On macOS:

  ```bash
  brew install ruby@3.3
  echo 'export PATH="/opt/homebrew/opt/ruby@3.3/bin:$PATH"' >> ~/.zshrc
  ```

  Open a new terminal afterwards and check with `ruby -v`.

## Setup

```bash
npm install
cd docs && bundle install
```

## Development

Run these in two terminals, from the repository root:

```bash
npm run dev
```

```bash
cd docs && bundle exec jekyll serve --livereload
```

The site runs at http://localhost:4000.

## Before committing

```bash
npm run build
```

===
Maintained by [flinksoftware.com](https://flinksoftware.com)