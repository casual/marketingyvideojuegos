source "https://rubygems.org"

gem "jekyll", "~> 4.3.0"
gem "minimal-mistakes-jekyll"

group :jekyll_plugins do
  gem "jekyll-feed"
  gem "jekyll-sitemap"
  gem "jekyll-paginate"
  gem "jekyll-include-cache"
end

# Gemas requeridas para Ruby 3.4+
gem "csv"
gem "base64"
gem "logger"
gem "bigdecimal"
gem "webrick", "~> 1.7"

# Windows timezone
install_if -> { RUBY_PLATFORM =~ %r!mingw|mswin|java! } do
  gem "tzinfo", "~> 1.2"
  gem "tzinfo-data"
end
