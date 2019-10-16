source 'https://rubygems.org'

RAILS_VERSION = '~> 4.2.11'

send :ruby, ENV['GEMFILE_RUBY_VERSION'] if ENV['GEMFILE_RUBY_VERSION']

gem 'actionmailer', RAILS_VERSION
gem 'actionpack', RAILS_VERSION
gem 'railties', RAILS_VERSION

gem 'actionmailer_inline_css', "~> 1.5"
gem 'decent_exposure', "~> 2.3"
gem 'devise', '~> 3.5'
gem 'dotenv-rails', "~> 2.0"
gem 'draper', "~> 2.1"
gem 'errbit_plugin', "~> 0.6"
gem 'errbit_github_plugin', "~> 0.3"
gem 'font-awesome-rails', "~> 4.2"
gem 'haml', "~> 4.0"
gem 'htmlentities', "~> 4.3"
gem 'kaminari', '~> 0.16'
gem 'mongoid', '~> 5.0'
gem 'mongoid_rails_migrations', "~> 1.0"
gem 'rack-ssl', "~> 1.4", require: 'rack/ssl' # force SSL
gem 'rack-ssl-enforcer', "~> 0.2", require: false
gem 'rails_autolink', "~> 1.1"
gem 'useragent', "~> 0.14"

# Please don't update hoptoad_notifier to airbrake.
# It's for internal use only, and we monkeypatch certain methods
gem 'hoptoad_notifier', "~> 2.4"

# Notification services
# ---------------------------------------
gem 'campy', "~> 1.0"
# Hipchat
gem 'hipchat', "~> 1.5"
# Google Talk
gem 'xmpp4r', "~> 0.5", require: ["xmpp4r", "xmpp4r/muc"]
# Hoiio (SMS)
gem 'hoi', "~> 0.0"
# Pushover (iOS Push notifications)
gem 'rushover', "~> 0.3"
# Hubot
gem 'httparty', "~> 0.13"
# Flowdock
gem 'flowdock', "~> 0.6"

# Authentication
# ---------------------------------------
# GitHub OAuth
gem 'omniauth-github', "~> 1.1"
# Google OAuth
gem 'omniauth-google-oauth2', "~> 0.4"

gem 'ri_cal', "~> 0.8"
gem 'yajl-ruby', '~> 1.4', platform: 'ruby'
gem 'json', '~> 1.8', platform: 'jruby'

group :development, :test do
  gem 'airbrake', '~> 4.3', require: false
  gem 'pry-rails', "~> 0.3"
  gem 'pry-byebug', "~> 3.1", platforms: [:mri]
  gem 'quiet_assets', "~> 1.1"
  gem 'rubocop', "~> 0.34", require: false
end

group :development do
  gem 'capistrano', "~> 3.4",         require: false
  gem 'capistrano-bundler', "~> 1.1", require: false
  gem 'capistrano-rails', "~> 1.1",   require: false
  gem 'capistrano-rbenv', "~> 2.0",   require: false
  gem 'capistrano-rvm', "~> 0.1",     require: false
  gem 'capistrano3-puma', "~> 1.2",   require: false

  # better errors
  gem 'better_errors', "~> 2.1"
  gem 'binding_of_caller', "~> 0.7", platform: 'ruby'
  gem 'meta_request', "~> 0.3"
end

group :test do
  gem 'rspec', '~> 3.3'
  gem 'rspec-rails', '~> 3.3', require: false
  gem 'rspec-activemodel-mocks', "~> 1.0"
  gem 'rspec-its', "~> 1.2"
  gem 'mongoid-rspec', '~> 3.0', require: false
  gem 'fabrication', "~> 2.13"
  gem 'capybara', "~> 2.4"
  gem 'poltergeist', "~> 1.6"
  gem 'phantomjs', "~> 2.1"
  gem 'launchy', "~> 2.4"
  gem 'email_spec', "~> 1.6"
  gem 'timecop', "~> 0.7"
  gem 'coveralls', "~> 0.8", require: false
end

group :heroku, :production do
  gem 'rails_12factor', "~> 0.0", require: ENV.key?("HEROKU")
end

group :no_docker, :test, :development do
 gem 'therubyracer', "~> 0.12", :platform => :ruby # C Ruby (MRI) or Rubinius, but NOT Windows
end

gem 'puma', "~> 3.4"
gem 'sass-rails', "~> 5.0"
gem 'uglifier', "~> 2.7"
# We can't upgrade because not compatible to jquery >= 1.9.
# To do that, we need fix the rails.js
gem 'jquery-rails', '~> 2.1'
gem 'pjax_rails', "~> 0.4"
gem 'underscore-rails', "~> 1.8"

gem 'sucker_punch', "~> 2.0"

ENV['USER_GEMFILE'] ||= './UserGemfile'
eval_gemfile ENV['USER_GEMFILE'] if File.exist?(ENV['USER_GEMFILE'])
