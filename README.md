# README

## Recommended guide to arrive at a baseline template for a Rails 7.x application
[Heroku Guide to get started with Rails 7.x on Heroku](https://devcenter.heroku.com/articles/getting-started-with-rails7)

Add x86_64_linux platform:

`bundle lock --add-platform x86_64-linux --add-platform ruby`

Remember to add gems: `net-smtp`, `net-pop`, and `gem net-imap`

Use latest stable version of node before doing:
`rails webpacker:install`.

For this application, node v16.14 was used.

`heroku create`

`heroku apps:rename <new ap name>`

`git push heroku main`

## Miscellaneous
This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
