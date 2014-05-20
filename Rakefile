require 'rubygems'
require 'bundler/setup'
require 'bundler/gem_tasks'
require 'rspec/core/rake_task'
require 'appraisal'

RSpec::Core::RakeTask.new do |t|
  t.pattern = 'spec/**/*_spec.rb'
  t.rspec_opts = '--color --format progress'
  t.verbose = false
end

if !ENV['APPRAISAL_INITIALIZED'] && !ENV['TRAVIS']
  task :default => :appraisal
else
  task :default => :spec
end