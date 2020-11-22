source "https://rubygems.org"

alchemy_branch = ENV.fetch("ALCHEMY_BRANCH", "master")
gem "alchemy_cms", github: "AlchemyCMS/alchemy_cms", branch: alchemy_branch

# Specify your gem's dependencies in alchemy-solidus.gemspec
gemspec

group :test do
  gem "sqlite3" if ENV["DB"].nil? || ENV["DB"] == "sqlite"
  gem "mysql2" if ENV["DB"] == "mysql"
  gem "pg", "~> 1.0" if ENV["DB"] == "postgresql"
  if ENV["TRAVIS"]
    gem "codeclimate-test-reporter", "~> 1.0", require: false
  end
end

gem "github_fast_changelog", require: false
