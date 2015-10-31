require 'rake/clean'

format_name = 'dbp'
tex_file = "#{format_name}.tex"
fmt_file = "#{format_name}.fmt"
log_file = "#{format_name}.log"
install_dir = '/usr/local/texlive/texmf-local/web2c/pdftex'


file fmt_file => tex_file do |t|
  `pdftex -ini -enc #{tex_file}`
end

desc 'Build the format file'
task build: fmt_file

desc 'Install the format file'
task install: fmt_file do
  `mv #{fmt_file} #{install_dir}`
end

CLEAN << fmt_file
CLEAN << log_file
