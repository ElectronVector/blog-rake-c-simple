source_files = Rake::FileList["*.c"]
object_files = source_files.ext(".o")

task :binary => object_files do
    sh "gcc #{object_files} -o app.exe"
end

task 'main.o' do
    sh "gcc -c main.c"
end 

task :default => :binary