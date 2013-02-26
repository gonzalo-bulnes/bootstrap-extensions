Bootstrap Extensions Github Pages
=================================

Getting Started
---------------

Get a local copy of the `gh-pages` branch:

```bash
cd bootstrap-extensions
git checkout gh-pages
```

In order to get a development server up quickly, installing the [Jekyll][jekyll] gem is required. To avoid messing up with you system gems, I use [RVM][rvm]; and to never forget a dependency, I recommend using [Bundler][bundler].

  [jekyll]:https://github.com/mojombo/jekyll
  [rvm]: https://rvm.io
  [bundler]: http://gembundler.com/

That's much more easy than it seems:

```bash
# Let RVM create a gemset for you
cd . # RVM will ask you if you want to trust the .rvmrc, answer: Y(es)

# Install Jekyll with Bundler
bundle install

# Compile the LESS files
lessc styles.less > styles.css

# Start the Jekyll server
jekyll --server
```

You server is up at [http://localhost:4000](http://localhost:4000).

### Version control

**Important**: You shall commit an up-to-date `stylesheets/styles.css` file along with `stylesheets/styles.less`.

Jekyll doesn't compile the LESS files, if you don't provide the up-to-date CSS your changes won't appear on the Github pages, the CSS file version won't match the LESS file version and I'll be sad.

```bash
# Before committing your changes...

# ... don't forget to compile the LESS files!
lessc stylesheets/styles.less > stylesheets/styles.css

git add stylesheets/styles*
git commit

```
