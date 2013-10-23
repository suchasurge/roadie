# encoding: utf-8
require 'bundler/setup'

Bundler::GemHelper.install_tasks

begin
  require 'rspec'
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end

require 'rspec/core/rake_task'

desc "Run specs"
RSpec::Core::RakeTask.new('spec') do |t|
  t.pattern = 'spec/**/*_spec.rb'
  t.rspec_opts = ["-c"]
end

desc "Default: Run specs"
task :default => :spec
