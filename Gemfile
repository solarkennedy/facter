if gem_source = ENV['GEM_SOURCE']
  source gem_source
else
  source "https://rubygems.org"
end

group :development do
  gem 'pry'
  gem 'watchr'
end

group :development, :test do
  gem 'rake'
  gem 'facter', ">= 1.0.0", :path => File.expand_path("..", __FILE__)
  gem 'rspec', "~> 2.11.0"
  gem 'mocha', "~> 0.10.5"
  gem 'json', "~> 1.7"
  gem 'puppetlabs_spec_helper'
end

platform :mswin, :mingw do
  gem "win32-api", "~> 1.4.8"
  gem "win32-dir", "~> 0.3.7"
  gem "windows-api", "~> 0.4.1"
  gem "windows-pr", "~> 1.2.1"
end

if File.exists? "#{__FILE__}.local"
  eval(File.read("#{__FILE__}.local"), binding)
end

# vim:ft=ruby
