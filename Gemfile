source "https://rubygems.org"

gemspec

group :test do
  gem "pry-rails"
  if ENV['RSPEC2']
    gem "rspec-rails", "~> 2.14.1"
  else
    gem "rspec-rails"
  end
  gem "weak_parameters"
  gem "protected_attributes"
  gem "rack-test"
end
