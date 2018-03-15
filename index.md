Publishing with GitHub Pages, now as easy as 1, 2, 3
 Dec 09, 2016

Publishing a website or software documentation with GitHub Pages now requires far fewer steps — three to be exact:

Create a repository (or navigate to an existing repository)
Commit a Markdown file via the web interface, just like you would any other file
Activate GitHub Pages via your repository’s settings
And that’s it — you now have a website. If you’re already familiar with GitHub Pages, you may be interested to know that behind the scenes, we’re now doing a few things to simplify the publishing experience and bring it more in line with what you may expect from authoring Markdown content elsewhere on GitHub:

All Markdown files are now rendered by GitHub Pages, saving you from needing to add YAML front matter (the metadata at the top of the file separated by ---s) to each file.
We’ll use your README file as the site’s index if you don’t have an index.md (or index.html), not dissimilar from when you browse to a repository on GitHub.
If you don’t specify a theme in your site’s config (or don’t have a config file at all), we’ll set a minimal, default theme that matches the look and feel of Markdown elsewhere on GitHub.
If a given file doesn’t have a layout specified, we’ll assign one based on its context. For example, pages will automatically get the page layout, or the default layout, if the page layout doesn’t exist.
If your page doesn’t have an explicit title, and the file begins with an H1, H2, or H3, we’ll use that heading as the page’s title, which appears in places like browser tabs.
These improvements should allow you to quickly and easily publish your first (or 100th) website with just a few clicks, or to document your software project by simply adding Markdown files to a /docs folder within your repository. Of course, you can continue to control the look and feel by opting in to additional customizations (such as overriding the default theme with your own layouts or styles).

While these changes shouldn’t affect how most existing sites build, there are two potential gotchas for some more advanced Jekyll users:

If your site iterates through all pages (e.g., for page in site.pages), you may find that there are now additional pages (such as the README of a vendored dependency) in that list. You can explicitly exclude these files with your config file’s exclude directive.
If you don’t specify a page’s layout or title, and expect either to be unset (e.g., if you need to serve unstyled content), you’ll need to explicitly set those values as null.
And if for any reason you don’t want these features, you can disable them by adding a .nojekyll file to your site’s root directory.

So that the GitHub Pages build process can be as transparent and customizable as possible, all the above features are implemented as open source Jekyll plugins, namely Jekyll Optional Front Matter, Jekyll README Index, Jekyll Default Layout, and Jekyll Titles from Headings.

Again, these changes shouldn’t affect how most existing sites build (although you can safely begin to use these features), but if you have any questions, please get in touch with us.

Happy three-step publishing!
