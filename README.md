# CIS 565 GPU Programming and Architecture Fall 2023

This website uses Hydejack Starter Kit, a quicker, cleaner way to get started blogging with [Hydejack](https://hydejack.com/).

## Quick Start

### Running locally (Windows only)

1. Clone repository (git users), or [download] and unzip.
2. If you don't have Ruby, install from here: https://rubyinstaller.org/ 
3. Open terminal, `cd` into root directory (where `_config.yml` is located)
4. Install Bundler if you haven't: `gem install bundler`
5. Run `bundle install` [^1]
6. Run `bundle exec jekyll serve`
7. Open <http://localhost:4000/>

### GitHub Pages

1. Fork this repository.
2. Go to **Settings**, rename repository to `<your github username>.github.io` (without the `<` `>`)
3. Edit `_config.yml` (you can do this directly on GitHub)
    1. Change `url` to `https://<your github username>.github.io` (without the `<` `>`)
    2. Change `baseurl` to `''` (empty string)
    3. **Commit changes**.
4. Go to **Settings** again, look for **GitHub Pages**, set **Source** to **master branch**.
5. Click **Save** and wait for GitHub to set up your new blag.