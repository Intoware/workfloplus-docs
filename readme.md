![](https://img.shields.io/github/license/intoware/workfloplus-docs) ![](https://img.shields.io/github/deployments/intoware/workfloplus-docs/github-pages)

# WorkfloPlus Developer Documentation

This repo contains the code to the [WorkfloPlus Developer documentation](https://intoware.github.io/workfloplus-docs). The code in this repo is automatically deployed to GitHub pages, but can be built and deployed locally.

## Build Instructions

1. Clone the Repository
1. Install Ruby
1. From the repository location (cd workfloplus-docs)
    1. Run `gem install bundler jekyll --user-install` to install Jekyll and Bundler
    1. Run `bundle config set --local path 'vendor/bundle'`
    1. Run `bundle install` to install any dependencies required

## Testing the Site

To serve the site call `bundle exec jekyll serve`. A webserver will start and host the site (usually http://127.0.0.1:4000/workfloplus-docs/). From here, navigate to your browser.

## Contributions

Contributions are welcome. Feel free to fork the repository, make changes and submit a PR.

## More Info

For more information on Intoware or WorkfloPlus visit www.intoware.com.

Intoware and WorkfloPlus are registered trademarks of Intoware Limited, a company registered in England and Wales. All rights reserved.