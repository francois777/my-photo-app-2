# README

## Recommended guide to arrive at a baseline template for a Rails 7.x application
[Heroku Guide to get started with Rails 7.x on Heroku](https://devcenter.heroku.com/articles/getting-started-with-rails7)

Add x86_64_linux platform:

`bundle lock --add-platform x86_64-linux --add-platform ruby`

Remember to add gems: `net-smtp`, `net-pop`, and `gem net-imap`

Use latest stable version of node before doing:
`rails webpacker:install`.

For this application, node v16.14 was used.

## Github

`https://github.com/francois777/my-photo-app-2`

## Working with Heroku

`https://my-photo-app-2.herokuapp.com`

`heroku create`

`heroku apps:rename <new ap name>`

`git push heroku main`

## Working with Devise

1. Add devise rubygems
2. `rails g devise:install`
3. `rails g devise User`
4. Add devise :confirmable to Users - read devise wiki
  - Uncomment confirmable fields in migration file before `db:migrate`
5. `rails db:migrate`
6. Apply authentication to `ApplicationController`
7. `rails g bootstrap:install static`
8. `rails g bootstrap:layout application`
9. `rails g devise:views:locale en`
10. `rails g devise:views:bootstrap_templates`

Retrieve missing assets from this source:

`wget https://www.python.org/static/apple-touch-icon-144x144-precomposed.png`

## Working with SendGrid in Heroku

After setting up your heroku account,
`heroku addons:create sendgrid:starter`

Response:
`Created sendgrid-symmetrical-83723 as SENDGRID_PASSWORD, SENDGRID_USERNAME`

    heroku config:set SENDGRID_USER_NAME=apikey
    heroku config:set SENDGRID_PASSWORD=<api-key>

To display your settings you can type in:
`heroku config:get SENDGRID_USERNAME`

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
