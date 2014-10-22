# Conditional Heroku deployment step (fork)
[![wercker status](https://app.wercker.com/status/b266b100aa5ba105be6936a379aff064/m "wercker status")](https://app.wercker.com/project/bykey/b266b100aa5ba105be6936a379aff064)

This is a fork of the official `heroku-deploy` step, but with added ability to skip via environment vars.

### For Complete Documentation See [step-heroku-deploy](https://app.wercker.com/#applications/51c829e73179be4478002157/tab/details)




## Using conditional (Feature Fork)

By using environment variables we can conditionally skip the heroku deploy

set environment vars; name: HEROKU_DEPLOY; value: true

set environment vars; name: HEROKU_DEPLOY; value: false

** the rest of the readme is verbatim **

# Configuration

everything is the same but use `conditional-heroku-deploy` instead of `heroku-deploy`

- In the `conditional-heroku-deploy` step in your `wercker.yml` add the config option name property with the value:

``` yaml
deploy:
    steps:
        - conditional-heroku-deploy:
            config-name: CONFIG_VALUE
```

In the above example the `CONFIG_VALUE` should match the environment variable name you used in wercker.

For full options see [see original readme](https://app.wercker.com/project/bykey/b266b100aa5ba105be6936a379aff064)

# What's new

- added rough implementation using $HEROKU_DEPLOY=true/false


# License

The MIT License (MIT)
