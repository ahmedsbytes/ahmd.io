ahmd.io blog
=====================

Install
-------

Create a new project using composer:

```bash
$ composer create-project -s dev sculpin/blog-skeleton my-blog
```

This application uses [Symfony's Webpack Encore](https://symfony.com/doc/current/frontend.html)
to manage CSS, JavaScript and image assets. Install the JS dependencies:

```bash
$ cd my-blog
$ yarn install
```

Build
-----

First, start Encore to compile and update the assets in `source/assets/` into
`source/build/`. The watcher keeps running until you exit it manually:

```bash
$ composer yarn-watch
```

In a new console, start the sculpin watcher to have your content updated as
soon as you save changes:

```bash
$ composer sculpin-watch
```

Your newly generated clone of sculpin-blog-skeleton should now be accessible
at `http://localhost:8000/`.

Documentation
-------------

The skeleton provides you with useful configuration and some example data for
a Sculpin installation.

For more information about getting started with Sculpin, check out the
[Get Started page](https://sculpin.io/getstarted/) and have a look at the full
[documentation](https://sculpin.io/documentation/).
