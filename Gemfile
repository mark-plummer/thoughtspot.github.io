source 'https://rubygems.org'

require 'json'
require 'open-uri'
versions = JSON.parse(open('https://pages.github.com/versions.json').read)

# gem 'github-pages', versions['github-pages']
gem 'github-pages', group: :jekyll_plugins
gem 'jekyll-sitemap'
gem 'jekyll-seo-tag'
gem 'jekyll-redirect-from'

# Gemfile

group :jekyll_plugins do
  gem 'jekyll-algolia', '~> 1.0'
end
