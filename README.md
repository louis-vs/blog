# Hugo Blog

This is a Hugo-based blog project configured for deployment to GitHub Pages.

## Development

To run the site locally:

```bash
hugo server -D
```

This will start a local development server at http://localhost:1313/ with live reloading enabled.

## Deployment

This site is automatically deployed to GitHub Pages using GitHub Actions. The workflow is configured in `.github/workflows/hugo-deploy.yml`.

### How it works

1. When you push changes to the `main` branch, the GitHub Action workflow is triggered
2. The workflow builds the Hugo site using the `peaceiris/actions-hugo` action
3. The built site is then deployed to the `gh-pages` branch using the `peaceiris/actions-gh-pages` action
4. GitHub Pages serves the content from the `gh-pages` branch

### Setup Requirements

For the GitHub Actions deployment to work correctly:

1. Make sure your repository has GitHub Pages enabled in the repository settings
2. Set the GitHub Pages source to the `gh-pages` branch and `/` (root) folder
3. The GitHub token is automatically provided by GitHub Actions, no additional setup required

## Project Structure

- `content/`: Contains all the content for your site
- `layouts/`: Custom layout templates
- `static/`: Static files like images, CSS, JavaScript
- `themes/`: Hugo themes
- `public/`: Generated site (don't edit directly, this is what gets deployed)
