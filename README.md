# Website

## Requirements:
* Ruby `5.1` or higher
* MySQL installation
* *Windows Only* Ruby [DevKit `x.x.x`](http://rubyinstaller.org/downloads) (required by nokogiri)

## Bulding API Java Classes
* Set `api-out` in `avicus.yml` to where you want the classes to go.
* Run `rake graphql:generate` to generate the classes.
* When the classes are loaded into the IDE, there will be a lot of unneeded imports, simply run Code -> Reformat Code to fix all errors

## Installation (Linux)
### Clone & Preperation
 * Install git, curl if it is not present on the System already `sudo apt install git curl`
 * Clone a local copy by running `git clone https://github.com/Avicus/Website`
### Installing Ruby
 * Install RVM Ruby Version Manager `gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 \ 7D2BAF1CF37B13E2069D6956105BD0E739499BDB`
  * Download the RVM installer script and install the RVM `curl -sSL https://get.rvm.io | bash -s stable --ruby`
  * Once all installation is completed, load the RVM `source /usr/local/rvm/scripts/rvm` *replace `local` with your home username*
  * Update RVM to latest stable `rvm get stable --autolibs=enable`
  * Install Ruby `rvm install ruby-2.7.1`
  * Make the Ruby 2.7.1 as the default Ruby version on your system `rvm --default use ruby-2.7.1`
  * Update RubyGem to latest version `gem update --system`
### Installing Packages & Gems
  * Install NodeJS `sudo apt install nodejs redis libmysqlclient-dev`
  * Install Ruby on Rails and other needed gems `gem install rails mysql2 nokogiri`
  * Update bundler `bundle update --bundler`
### Configure database.yml
  * In `config/database.yml` configure the host, database, username and password for MySQL.
  * In `config/avicus.yml` configure the host, port and password for redis.
  * Run `rake db:setup` to populate the database.
  * Use `rails s`to boot the Website application, default address is `localhost:3000`
  
