# just-the-docs-template

## Adding a plugin

The Just the Docs theme automatically includes the [`jekyll-seo-tag`] plugin.

To add an extra plugin, you need to add it in the `Gemfile` *and* in `_config.yml`. For example, to add [`jekyll-default-layout`]:

- Add the following to your site's `Gemfile`:
  
  ```ruby
  gem "jekyll-default-layout"
  ```

- And add the following to your site's `_config.yml`:
  
  ```yaml
  plugins:
    - jekyll-default-layout
  ```

## Publishing your site on GitHub Pages

1. If your created site is `YOUR-USERNAME/YOUR-SITE-NAME`, update `_config.yml` to:
   
   ```yaml
   title: YOUR TITLE
   description: YOUR DESCRIPTION
   theme: just-the-docs
   
   url: https://YOUR-USERNAME.github.io/YOUR-SITE-NAME
   
   aux_links: # remove if you don't want this link to appear on your pages
     Template Repository: https://github.com/YOUR-USERNAME/YOUR-SITE-NAME
   ```

2. Push your updated `_config.yml` to your site on GitHub.

3. In your newly created repo on GitHub:
   
   - go to the `Settings` tab -> `Pages` -> `Build and deployment`, then select `Source`: `GitHub Actions`.
   - if there were any failed Actions, go to the `Actions` tab and click on `Re-run jobs`.

## Building and previewing your site locally

Assuming [Jekyll] and [Bundler] are installed on your computer:

1. Change your working directory to the root directory of your site.

2. Run `bundle install`.

3. Run `bundle exec jekyll serve` to build your site and preview it at `localhost:4000`.
   
   The built site is stored in the directory `_site`.

## Licensing and Attribution

This repository is licensed under the [MIT License].

----

[^1]: [It can take up to 10 minutes for changes to your site to publish after you push the changes to GitHub](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll#creating-your-site).

[Jekyll]: https://jekyllrb.com
[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[Bundler]: https://bundler.io
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
[`jekyll-default-layout`]: https://github.com/benbalter/jekyll-default-layout
[`jekyll-seo-tag`]: https://jekyll.github.io/jekyll-seo-tag
[MIT License]: https://en.wikipedia.org/wiki/MIT_License
[starter workflows]: https://github.com/actions/starter-workflows/blob/main/pages/jekyll.yml
[actions/starter-workflows]: https://github.com/actions/starter-workflows/blob/main/LICENSE
