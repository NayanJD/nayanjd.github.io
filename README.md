# My Personal Blog

This blog is powered by [Hugo](https://gohugo.io/) and [Adritian-Free-Hugo-Theme](https://themes.gohugo.io/themes/adritian-free-hugo-theme/). This blog is **not complete** yet. I am working on it as I get time from work.

## How it was bootstrapped

The [Adritian-Free-Hugo-Theme](https://themes.gohugo.io/themes/adritian-free-hugo-theme/) page already describes the bootstrap process. However, I am recording it here if it changes for future version of the theme.

Steps:

1. Create a new Hugo site (this will create a new folder): hugo new site <your website's name>
2. Enter the newly created folder: cd <your website's name>/
3. Initialize the Hugo Module system in your site if you haven’t already: hugo mod init github.com/username/your-site (you don’t need to host your website on GitHub, you can add anything as a name)
4. Install the theme as a module: hugo mod get -u github.com/zetxek/adritian-free-hugo-theme
5. Add the following to your hugo.toml, to set the theme as active:
```toml
[module]
[[module.imports]]
path = "github.com/zetxek/adritian-free-hugo-theme"
```
6. Prepare the package.json file: hugo mod npm pack
7. Install the dependencies: npm install. This will include Bootstrap (needed for styling) and the helper script adritian-theme-helper.
8. Run the initial content downloader: ./node_modules/adritian-theme-helper/dist/scripts/download-content.js. This will download the demo content from the adritian-demo repository and copy it to your site, for a quick start (including translations, images, configuration and content)

## Deployment

The blog is deployed to Github Pages using Github Actions upon pushing to `main` branch.
