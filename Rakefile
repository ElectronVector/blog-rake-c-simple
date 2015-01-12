task :binary => 'main.o' do
    sh "gcc main.o -o app.exe"
end

task 'main.o' do
    sh "gcc -c main.c"
end 

task :default => :binary