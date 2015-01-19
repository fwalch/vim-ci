# vim-ci

This is an attempt to bring some build automation to Vim.

You can use this to check the build status of the latest Vim version or to test your own patches.
It currently only builds for Linux, but might eventually support OS X (through Travis) and Windows (through AppVeyor).

Feedback and contributions welcome!

## Build of the latest Vim version

[![Build Status](https://travis-ci.org/fwalch/vim-ci.svg)](https://travis-ci.org/fwalch/vim-ci)

You can see the build results at https://travis-ci.org/fwalch/builds. Builds are currently triggered manually,
but might eventually run at fixed intervals (e.g. once every day).

## How to test Vim patches

 1. Fork and clone this repository.
 2. Add the patches you want to test to the `patches/` directory.
 3. Commit these changes and create a pull request to this repository.

This will trigger a Travis build, which will apply the patch, compile Vim and run the tests. For an example pull request, see [pull request #1][example-pr].

To avoid too many pull requests, please consider re-using one of your existing pull requests. [Force-pushing][force-push] to an existing pull request's branch will trigger a new build.

As an alternative, you can [enable Travis CI][travis-enable] for your forked repository.

[example-pr]: https://github.com/fwalch/vim-ci/pull/1
[force-push]: https://help.github.com/articles/using-git-rebase/#pushing-rebased-code-to-github
[travis-enable]: travis-ci.org/profile
