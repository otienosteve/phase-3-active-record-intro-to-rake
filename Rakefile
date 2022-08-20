
namespace :greeting do

task :hello do
  puts "hello from Rake!"
end
task :hola do
  puts "hola de Rake!"

end

end

namespace :db do
   
  task :environment do
    require_relative './config/environment'
  end


  desc 'migrate changes to your database'
  task migrate: :environment do
    Student.create_table
  end


  desc 'seed the database with some dummy data'
  task seed: :environment do
    require_relative './db/seeds'
  end
  

end

task console: :environment do
  Pry.start
end

