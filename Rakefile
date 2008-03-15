require 'rake'
require 'rake/testtask'
require 'rubygems'
require 'hoe'
require './lib/simplerdb.rb'

  
task :default => [:test]

Hoe.new('simplerdb', SimplerDB::VERSION) do |p|
  p.rubyforge_name = 'simplerdb'
  p.author = 'Gary Elliott'
  p.email = 'gary@tourb.us'
  p.summary = "An in-memory implementation of Amazon's SimpleDB REST API "
  p.description = p.summary
  p.url = p.paragraphs_of('README.txt', 0).first.split(/\n/)[1..-1]
  p.remote_rdoc_dir = '' # Release to root
  p.version = SimplerDB::VERSION
  p.extra_deps << ['dhaka', '>= 2.2.1']
  p.extra_deps << ['builder', '>= 2.0']
end


Rake::TestTask.new do |t|
  t.libs << "lib"
  t.test_files = FileList['test/*test.rb']
  t.verbose = true
end