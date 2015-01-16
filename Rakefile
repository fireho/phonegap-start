# gem install haml sass
# npm -g install coffee
require 'rake'
START = Time.now

def get_sources(ext)
  source_files = Rake::FileList.new("app/**/*.#{ext}") do |fl|
    fl.exclude("~*")
    fl.exclude(/^scratch\//)
    # fl.exclude { |f| `git ls-files #{f}`.empty? } # Only commited
  end
end

task default: ['compile:all']

namespace :compile do

  desc 'Compiles all resources'
  task :all => [:js, :css, :html] do |t|
    puts "DONE #{format("%.2f", Time.now - START)}s #{t}"
  end

  task :js => get_sources(:coffee).ext('.js')
  task :css => get_sources(:sass).ext('.css')
  task :html => get_sources(:haml).ext('.html')

  rule '.js' => '.coffee' do |t|
    output = File.dirname(t.source).gsub(/app\//, 'www/')
    print "CoffeeScript | " # #{t.source} -> #{output}"
    sh "coffee --no-header -b -o #{output} #{t.source}"
  end

  rule '.css' => '.sass' do |t|
    print "SASS | #{t.source} -> #{t.name} | "
    sh "sass #{t.source} #{t.name.gsub(/app\//, 'www/')}"
  end

  rule '.html' => '.haml' do |t|
    print "HAML | #{t.source} -> #{t.name} | "
    sh "haml #{t.source} #{t.name.gsub(/app\/html/, 'www')}"
  end
end
