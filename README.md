Heroku buildpack: AWS-CLI
=======================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) of [AWS-CLI](https://aws.amazon.com/cli/) is intended for use after the regular [python-buildpack](https://github.com/heroku/heroku-buildpack-python).

Usage
-----

Example usage:

```shell
$ heroku create --stack cedar --buildpack https://github.com/GovSciences/heroku-buildpack-aws-cli.git

# or if your app is already created:
$ heroku buildpacks:add https://github.com/GovSciences/heroku-buildpack-aws-cli

$ git push heroku master
```

Configure
---------

Environment variables override configuration and credential files and can be useful for scripting or temporarily setting a named profile as the default.
Set the `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY`:

```shell
heroku config:set AWS_ACCESS_KEY_ID='my-aws-access-key-id' AWS_SECRET_ACCESS_KEY='my-aws-secret-access-key'
```
