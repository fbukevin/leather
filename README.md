# Leather

Adds some useful setup for Rails apps that use Devise and Bootstrap 3. Creates a UI Kit page that makes it easy to define Bootstrap styles before starting the design process. Adds a nice-looking set of Devise views that use Bootstrap markup. Provides some useful partials for common Bootstrap components like modals, allowing you to skip the trip to getbootstrap.com to copy the markup.

## Installation

Add this line to your application's Gemfile:

    gem 'leather'

Then execute:

    $ bundle
    
This will install leather, along with devise and bootstrap-sass as dependencies. 

You will need to install devise. The basic steps are to run:

    $ rails g devise:install
    $ rails g devise User

and make sure you have:

* Flash messages displayed in your application layout
* A root route set
* Default URL options for the Devise mailer configured for each environment. An example for `config/environments/development.rb` is:

    config.action_mailer.default_url_options = { host: 'localhost', port: 3000 }

## Usage

### Installing Devise Views

Run this command to install a set of views for devise that work nicely with Bootstrap 3:

    $ rails g leather:install
    
You'll also want to add the styles (which include bootstrap) to your application.css.scss by including:

    @import 'devise';
    
And modify your `<body>` tag:

    <body class="<%= params[:controller].split("/").join("_") %> <%= params[:action] %>">

You'll get fully-customizable views that look good by default:

![Screenshot](https://raw.githubusercontent.com/dvanderbeek/leather/master/login.png)

### Adding a UI Kit


## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
