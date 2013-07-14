require 'rubygems'

version = '1.5.0146.1'

directory 'pkg'

task :gem => 'pkg' do
  spec = Gem::Specification.new do |s|
    s.name = 'bouncy-castle-java'
    s.version = version
    s.author = 'Hiroshi Nakamura'
    s.email = 'nahi@ruby-lang.org'
    s.rubyforge_project = "jruby-extras"
    s.homepage = 'http://github.com/nahi/bouncy-castle-java/'
    s.summary = 'Gem redistribution of Bouncy Castle jars'
    s.description = 'Gem redistribution of "Legion of the Bouncy Castle Java cryptography APIs" jars at http://www.bouncycastle.org/java.html'
    s.platform = Gem::Platform::CURRENT
    s.require_path = 'lib'
    s.files = ['README', 'LICENSE.html'] + Dir.glob("lib/**/*")
  end
  filename = Gem::Builder.new(spec).build
  mv filename, "pkg/#{filename}"
end

task :default => :gem
