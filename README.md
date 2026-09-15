# Aarav Vikram — Personal Gateway

A minimal, terminal-inspired "About Me" and linktree-style gateway website built with Jekyll.

## 🛠️ Local Development

1. **Install dependencies**:
   ```bash
   bundle install
   ```

2. **Run local server (with local config override)**:
   ```bash
   bundle exec jekyll serve --config _config.yml,_config.dev.yml
   ```

3. Visit [http://localhost:4000](http://localhost:4000) in your browser.

## 🚀 Production Build

To build the static site for deployment (GitHub Pages with `/AVVM` baseurl):
```bash
bundle exec jekyll build
```
The production output will be generated in `_site/`.
