# A sample Guardfile
# More info at https://github.com/guard/guard#readme

## Uncomment and set this to only include directories you want to watch
# directories %w(app lib config test spec feature)

## Uncomment to clear the screen before every task
# clearing :on

coffeescript_options = {
  bare: true,
  input: 'app/js',
  output: 'www/js',
  patterns: [%r{^app/js/(.+\.(?:coffee|coffee\.md|litcoffee))$}]
}

guard 'coffeescript', coffeescript_options do
  coffeescript_options[:patterns].each { |pattern| watch(pattern) }
end

guard :haml, :input => 'app/html', :output => 'www'

# guard :haml, :input => 'app/html', :output => 'www' do
#   watch(/^.+(\.html\.haml)$/)
# end

guard :sass, :input => 'app/css', :output => 'www/css'
