source "https://rubygems.org"

# `github-pages` bundles the exact Jekyll + plugin versions GitHub Pages
# itself runs, so a build via Actions behaves the same as a native Pages
# build. Version is intentionally unpinned here; ruby/setup-ruby's
# bundler-cache in the workflow will resolve and lock it on first run.
gem "github-pages", group: :jekyll_plugins

group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.12"
end

# Windows and JRuby don't ship zoneinfo data by default.
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Performance booster for file watching on Windows.
gem "wdm", "~> 0.1", :platforms => [:mingw, :x64_mingw, :mswin]

# Lock `http_parser.rb` to 0.6.x on JRuby -- newer versions have no Java build.
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]
