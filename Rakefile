namespace :greeting do
desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end
desc 'output hola'
task :hola do 
  puts 'hola de Rake!'
end
end

desc 'drop into pry console'
task :console => :environment do 
  Pry.start
end

task :environment do
  require_relative './config/environment'
end

namespace :db do 
  desc 'migrate'
  task :migrate => :environment do 
    Student.create_table
  end

  desc 'seed'
  task :seed do 
    require_relative './db/seeds.rb'
  end
  
end

