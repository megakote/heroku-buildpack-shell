heroku-buildpack-shell
========================

A [heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for bash script. It looks like this `/bin/bash /app/.sh`.

## Usage
    echo -e "echo 'Hello from dokku'" > .sh
    git add .sh; git commit -m 'Added heroku-buildpack-shell';
    git push dokku master;

## Use with ddollar/heroku-buildpack-multi
    echo -e "EXPORT=BUILDPACK_URL=https://github.com/ddollar/heroku-buildpack-multi" > .env
    echo -e "https://github.com/heroku/heroku-buildpack-ruby\nhttps://github.com/gtank/heroku-buildpack-shell" > .buildpacks
