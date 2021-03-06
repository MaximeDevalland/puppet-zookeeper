source 'https://rubygems.org'

group :tests do
  puppetversion = ENV.key?('PUPPET_VERSION') ? "#{ENV['PUPPET_VERSION']}" : ['>= 2.7.0', '< 6.0']
  gem 'puppet', puppetversion
  gem 'rake'
  gem 'puppet-lint'
  gem 'puppetlabs_spec_helper'
  gem 'librarian-puppet', '>= 2.0'
  gem 'highline'
  gem 'simplecov'
  gem 'simplecov-console'
  gem 'rspec-puppet-facts'
  gem 'rspec', '>= 3.0.0'
  gem 'rspec-puppet', '>= 2.3.0'
  if RUBY_VERSION < "2.0.0"
    gem 'json', '< 2.0' # newer versions requires at least ruby 2.0
    gem 'json_pure', '< 2.0.0'
    gem 'fog-google', '< 0.1.1'
    gem 'google-api-client', '< 0.9'
    gem 'public_suffix', '< 1.5.0'
    gem 'parallel_tests', '< 2.10'
    gem 'metadata-json-lint', '< 1.2.0', require: false
  else
    gem 'metadata-json-lint', require: false
  end
end

group :development do
  gem 'rubocop', '>= 0.49.0'
  gem 'puppet-blacksmith', '< 4.0.0'
end

group :system_tests do
  # beaker-rspec will require beaker gem
  if RUBY_VERSION >= '2.2.5'
    gem 'beaker'
  else
    gem 'beaker', '< 3'
  end
  gem 'beaker-rspec'
  gem 'serverspec'
  gem 'beaker-hostgenerator'
  gem 'beaker-puppet_install_helper'
  gem 'master_manipulator'
end
