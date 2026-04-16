# Open3DIY Site

## How to Install Jekyll and Test the <open3diy.org> Documentation Page

Jekyll is used to generate the main site page, leveraging GitHub Pages integration for automatic documentation publishing.

To install and run Jekyll on Linux, follow these steps:

1. Check the official guide at [jekyllrb.com/docs](https://jekyllrb.com/docs/) and, for Ubuntu, see [jekyllrb.com/docs/installation/ubuntu](https://jekyllrb.com/docs/installation/ubuntu/).
2. Install the required dependencies (only the first time) from the terminal, in the project's root folder:

   ```bash
   bundle install
   ```

3. To start the documentation server, run:

   ```bash
   bundle exec jekyll serve --source docs
   ```

4. Access the local page at [http://localhost:4000](http://localhost:4000).

5. For the `githubdoc` plugin, if you are an authorized user, create a **classic token** at <https://github.com/settings/tokens> and add it to your `~/.bashrc` with the following content:

   ```bash
   export JEKYLL_GITHUB_TOKEN=your_token
   source ~/.bashrc
   ```

> If you encounter dependency issues, check the official documentation or seek help from the Jekyll community.

### GitHub Pages Configuration

Although this setup is usually done when creating the repository and enabling GitHub Pages, here are the steps to configure GitHub Pages and use the latest version of Minima, the base Jekyll theme that is not limited by classic GitHub Pages.

1. In the `org` repository of `open3diy`, go to **Settings → Pages → Build and deployment**.

2. Under **Build**, in the **Source** option, select **GitHub Pages Jekyll** and click **Configure**. A valid configuration will be proposed, so click **Commit changes...**.
