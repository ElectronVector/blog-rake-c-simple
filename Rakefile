require 'rake/clean'

CLEAN.include('*.o')
CLOBBER.include('*.exe')

source_files = Rake::FileList["*.c"]
object_files = source_files.ext(".o")

desc "Build the binary executable"
task :binary => object_files do
    sh "gcc #{object_files} -o app.exe"
end

rule '.o' => '.c' do |task|
    sh "gcc -c #{task.source}"
end

desc "rake binary"
task :default => :binary