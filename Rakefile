require 'rubygems'
require 'rake'
require 'yard'
require 'jeweler'
require 'rake/testtask'

require File.join(File.dirname(__FILE__), 'lib', 'joint', 'version')

Jeweler::Tasks.new do |gem|
  gem.name        = "joint"
  gem.summary     = %Q{MongoMapper and GridFS united in file upload love.}
  gem.description = %Q{MongoMapper and GridFS united in file upload love.}
  gem.email       = "nunemaker@gmail.com"
  gem.homepage    = "http://github.com/jnunemaker/joint"
  gem.authors     = ["John Nunemaker"]
  gem.version     = Joint::Version

  gem.add_dependency 'wand', '>= 0.2.1'
  gem.add_dependency 'mime-types'

  gem.add_development_dependency 'jeweler'
end
Jeweler::GemcutterTasks.new


Rake::TestTask.new(:test) do |test|
  test.libs      << 'lib' << 'test'
  test.ruby_opts << '-rubygems'
  test.pattern   = 'test/**/test_*.rb'
  test.verbose   = true
end

task :test    => :check_dependencies
task :default => :test