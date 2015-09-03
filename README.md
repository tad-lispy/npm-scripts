Installing with npm from local directory vs. git repository
===========================================================

This is a dummy [NPM](http://npmjs.org/) package to investigate different behavior when installing from local direcotry vs Git repository. It is meant to be a supplementary material for discussion around [issue 3055 of npm/npm]( https://github.com/npm/npm/issues/3055).

How to use it
-------------

First please see the [package.json](package.json) file. It's full of lifecycle scripts (all that are mentioned [in the docs](https://docs.npmjs.com/misc/scripts)). Each just outputs it's name.

Then you can review log files from running `npm install` in various ways. Both `stdout` and `stderr` are concatenated in the logs.

* [from within the package directory: `npm i --verbose`](npm-install-from-within.log)
* [from local directory: `npm i --verbose ../npm-scripts`](npm-install-local-directory.log)
* [from Git repository:`npm i --verbose lzrski/npm-scripts`](npm-install-git-repo.log)

Use your preferred diff tool to compare them.

Contributing
------------

Please keep in mind that this is only a test material. Post all npm-related comments to [npm/npm issue tracker](https://github.com/npm/npm/issues/). This includes the results of your investigation using this project.

If you believe this test can be improved then please pull request your changes.
