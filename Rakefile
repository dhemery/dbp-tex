require 'rake/clean'

format_name = 'dbp'
tex_file = "#{format_name}.tex"
fmt_file = "#{format_name}.fmt"
log_file = "#{format_name}.log"
install_dir = '/usr/local/texlive/texmf-local/web2c/pdftex'
installed_fmt_file = "#{install_dir}/#{fmt_file}"

task default: [:clobber, :install]

directory install_dir do |t|
  mkdir_p install_dir
end

file fmt_file

file installed_fmt_file

desc 'Build the format file'
task :build do
 `pdftex -interaction=batchmode -etex -enc -ini #{tex_file}`
end

desc 'Install the format file'
task install: [:build, install_dir] do
  cp fmt_file, installed_fmt_file
end

desc 'Show the log file'
task :log do
  print `cat #{log_file}`
end

CLEAN << fmt_file
CLEAN << log_file
CLOBBER << install_dir
