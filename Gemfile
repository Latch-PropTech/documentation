source "https://rubygems.org"

# Use GitHub Pages gem for compatibility
gem "github-pages", group: :jekyll_plugins

# Windows and JRuby compatibility
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Performance-booster for watching directories
gem "wdm", "~> 0.1", :platforms => [:mingw, :x64_mingw, :mswin]

# Lock `http_parser.rb` gem to `v0.6.0` on JRuby builds
gem "http_parser.rb", "~> 0.6.0", :platforms => [:jruby]

# WebRick for Ruby 3+
gem "webrick"
