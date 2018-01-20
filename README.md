# [superset](https://github.com/apache/incubator-superset) on [Heroku](http://heroku.com)

Superset is a data exploration platform designed to be visual, intuitive, and interactive. Visit the project's website at <http://airbnb.io/superset>

## Deploying on Heroku

To get your own Superset App running on Heroku, click the button below:

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/fourniem/superset-on-heroku)

Fill out the form, and later you should be performing analytics at the speed of thought.

### Things you should know
##### After deployment

- Superset will be accessible at `YOURAPPNAME.herokuapp.com`.

- To make changes to your app like creating admin user, clone your app locally using the [Heroku Toolbelt](https://toolbelt.heroku.com/):

```sh
heroku git:clone --app YOURAPPNAME
```

- Attach the postgres DB to the app


- Create an Admin user by using

```sh
heroku run bash --app YOURAPPNAME
fabmanager create-admin --app superset
superset db upgrade
superset init
```

- Check Papertrail logs for debugging any errors.

### How this works

This repository is essentially a minimal web application that specifies [Superset as a dependency](https://github.com/apache/incubator-superset), and makes a deploy button available.

## Problems?

If you have problems using your instance of Superset, you should check the [official documentation](https://superset.incubator.apache.org/installation.html) or open an issue on [issue tracker](https://github.com/apache/incubator-superset/issues). If you discover an issue with the deployment process provided by *this repository*, then [open an issue here](https://github.com/dugjason/superset-on-heroku/issues).
