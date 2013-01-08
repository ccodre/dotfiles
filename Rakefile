require 'fileutils'

task :default => 'sync_files'

task :sync_files do
	make_dir 'zsh'
	copy_the_file 'zshrc', 'zsh'
end

def make_dir(dir)
	if ! File.directory? dir
		FileUtils.mkdir dir
		puts 'created %s' % dir
	end
end

def copy_the_file(file, dest_dir)
	FileUtils.cp "/home/ccodre/.#{file}" , "#{dest_dir}/#{file}"
	puts 'copied %s to %s/%s' % [file, dest_dir, file]
end