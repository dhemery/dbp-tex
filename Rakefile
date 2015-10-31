require 'rake/clean'

format_name = 'dbp'
tex_file = "#{format_name}.tex"
fmt_file = "#{format_name}.fmt"
log_file = "#{format_name}.log"
install_dir = '/usr/local/texlive/texmf-local/web2c/pdftex'
installed_fmt_file = "#{install_dir}/#{fmt_file}"

task default: :install

directory install_dir do |t|
  mkdir_p install_dir
end

file fmt_file => tex_file do |t|
  `pdftex -ini -enc #{tex_file}`
end

file installed_fmt_file => [fmt_file, install_dir] do
  cp fmt_file, installed_fmt_file
end

desc 'Build the format file'
task build: fmt_file

desc 'Install the format file'
task install: installed_fmt_file

CLEAN << fmt_file
CLEAN << log_file
CLOBBER << install_dir
