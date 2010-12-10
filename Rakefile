require 'rake'
require 'rake/testtask'
require 'rake/rdoctask'

desc 'Default: run unit tests.'
task :default => :test

desc 'Test the GeoKit plugin.'
Rake::TestTask.new(:test) do |t|
  t.libs << 'lib'
  t.pattern = 'test/**/*_test.rb'
  t.verbose = true
end

desc 'Generate documentation for the GeoKit plugin.'
Rake::RDocTask.new(:rdoc) do |rdoc|
  rdoc.rdoc_dir = 'rdoc'
  rdoc.title    = 'GeoKit'
  rdoc.options << '--line-numbers' << '--inline-source'
  rdoc.rdoc_files.include('README')
  rdoc.rdoc_files.include('lib/**/*.rb')
end

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name = "geokit-rails"
    gem.summary = %Q{Geo distance calculations, distance calculation query support, geocoding for physical and ip addresses}
    gem.description = %Q{Geo distance calculations, distance calculation query support, geocoding for physical and ip addresses}
    gem.authors = ["Bill Eisenhauer", "Andre Lewis"]
    gem.email = "andre@earthcode.com / bill_eisenhauer@yahoo.com"
    gem.add_dependency "geokit-gem", "~> 1.2.5"
  end
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: gem install jeweler"
end