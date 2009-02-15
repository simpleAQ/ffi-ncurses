# Look in the tasks/setup.rb file for the various options that can be
# configured in this Rakefile. The .rake files in the tasks directory
# are where the options are used.

begin
  require 'bones'
  Bones.setup
rescue LoadError
  begin
    load 'tasks/setup.rb'
  rescue LoadError
    raise RuntimeError, '### please install the "bones" gem ###'
  end
end

ensure_in_path 'lib'
require 'ffi-ncurses'

task :default => 'spec:run'

# see tasks/setup.rb for full list of options

PROJ.name = 'ffi-ncurses'
PROJ.authors = ["Sean O'Halpin"]
PROJ.email = 'sean.ohalpin@gmail.com'
PROJ.url = 'http://github.com/seanohalpin/ffi-ncurses'
PROJ.summary = "FFI wrapper for ncurses"
PROJ.version = "0.3.0"
PROJ.rubyforge.name = 'ffi-ncurses'

# rdoc
PROJ.rdoc.exclude << "^notes"
PROJ.readme_file = 'README.rdoc'

PROJ.rdoc.include << /ffi-.*\.rb/

# spec
PROJ.spec.opts << '--color'

# files
PROJ.exclude = %w(tmp$ bak$ ~$ CVS \.svn ^pkg ^doc \.git)
PROJ.exclude << '^tags$' << "^bug" << "^tools"
PROJ.exclude << File.read('.gitignore').split(/\n/)

# notes
#PROJ.notes.exclude = %w(^README\.txt$ ^data/)
PROJ.notes.extensions << '.org'

# EOF
