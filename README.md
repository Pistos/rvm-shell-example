This repository demonstrates a failure to use RVM correctly when shelling out
in Ruby.

## Setup

    cd app1
    bundle install
    cd ../app2
    bundle install

## Test

    cd app2
    ./build-site.sh
    # Observe nanoc help output show successfully.

    cd ../app1
    bundle exec ruby shell-and-build-site.rb
    # Observe error:
    #   nanoc is not part of the bundle. Add it to Gemfile. (Gem::LoadError)
