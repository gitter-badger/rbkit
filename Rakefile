require "bundler/gem_tasks"
require "rspec/core/rake_task"
require 'rake/extensiontask'

Rake::ExtensionTask.new('rbkit_tracer') do |ext|
  ext.ext_dir = 'ext'
end

Rake::ExtensionTask.new('rbkit_test_helper') do |ext|
  ext.config_script = 'extconf_for_test.rb'
  ext.ext_dir = 'ext'
end

RSpec::Core::RakeTask.new

task :default => [:compile, :spec]
