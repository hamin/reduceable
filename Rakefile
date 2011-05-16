require 'bundler'
Bundler::GemHelper.install_tasks

require "rspec/core/rake_task"

RSpec::Core::RakeTask.new(:core) do |spec|
  spec.pattern = 'spec/**/*_spec.rb'
  spec.rspec_opts = %w(-fs --color)
end

Dir["tasks/*.rake"].each do |rake_file|
  load rake_file
end

task :default => [:core]
