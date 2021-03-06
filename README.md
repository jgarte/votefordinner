[![Build Status](https://travis-ci.org/octopusinvitro/votefordinner.svg?branch=master)](https://travis-ci.org/octopusinvitro/votefordinner)
[![build status](https://gitlab.com/octopusinvitro/votefordinner/badges/master/build.svg)](https://gitlab.com/octopusinvitro/votefordinner/commits/master)
[![Dependency status](https://badges.depfu.com/badges/c575060ba5bcaf9cd11a77b139616753/overview.svg)](https://depfu.com/github/octopusinvitro/votefordinner?project=Bundler)
[![Code Climate](https://codeclimate.com/github/octopusinvitro/votefordinner/badges/gpa.svg)](https://codeclimate.com/github/octopusinvitro/votefordinner)

# Readme

A project to play with Sinatra. You can visit the app at [https://votefordinner.herokuapp.com/](https://votefordinner.herokuapp.com/).

![Screenshot](screenshot.png)


## How to use this project

This is a Ruby project.
You will need to tell your favourite Ruby version manager to set your local Ruby version to the one specified in the `.ruby-version` file.

For example, if you are using [rbenv](https://cbednarski.com/articles/installing-ruby/):

1. Install the right Ruby version:
```bash
$ rbenv install < VERSION >
$ rbenv rehash
```
1. Move to the root directory of this project and type:
```bash
$ rbenv local < VERSION >
$ ruby -v
```

You will also need to install the `bundler` gem, which will allow you to install the rest of the dependencies listed in the `Gemfile` file of this project.

```bash
$ gem install bundler
$ rbenv rehash
```


### Folder structure

* `bin `: Executables
* `lib `: Sources
* `spec`: Tests


### To initialise the project

```bash
$ bundle install
$ bundle exec rake
```


### To run the tests

```bash
$ bundle exec rspec --color
```


### To run the tests and rubocop

```bash
$ bundle exec rake
```

### To run the app

Make sure that the `bin/app` file has execution permissions:

```bash
$ chmod +x bin/app
```

Then just type:

```bash
$ bin/app
```

Open your browser and go to http://localhost:4567/


### Another way of running it

Update the `config.ru` file, then type

```bash
$ bundle exec rackup
```

Open your browser and go to http://localhost:9292/


## Heroku

Login to your Heroku account:

```bash
$ heroku login
```

Deploy:

```sh
$ heroku create votefordinner # first deploy only
$ git remote add heroku git@heroku.com:votefordinner.git
$ git push heroku master
$ heroku open
```


## Todo

* [ ] Make Sinatra use sass with sprokets (apparently another gem has to be added, `sprockets-sass`, which is stupid, because sass can do sass things! I may drop sprockets)
* [ ] Fix the radio buttons, for some reason the `:after` pseudo-element is not showing.
* [x] Find out why the cast page container is wider than the other pages.
* [ ] Extract the yaml from the main class.
* [ ] Extract the svg's into partials.


## License

[![License](https://img.shields.io/badge/gnu-license-green.svg?style=flat)](https://opensource.org/licenses/GPL-2.0)
GNU License
