require 'nanoc3/tasks'

namespace :optimise do
  desc 'Optimise JPEG images in output/images directory using jpegoptim'
  task :jpeg do
    puts `find output/images -name '*.jpg' -exec jpegoptim {} \\;`
  end

  desc 'Optimise PNG images in output/images directory using optipng'
  task :png do
    puts `find output/images -name '*.png' -exec optipng {} \\;`
  end

  desc 'Compress CSS files in output/style directory using YUI Compressor'
  task :css do
    puts `find output/style -name '*.css' -exec java -jar /usr/share/yuicompressor-2.4.2/build/yuicompressor-2.4.2.jar --type css '{}' -o '{}' \\;`
  end

  desc 'Compress JavaScript files in output/script directory using YUI Compressor'
  task :js do
    puts `find output/script -name '*.js' -exec java -jar /usr/share/yuicompressor-2.4.2/build/yuicompressor-2.4.2.jar --type js '{}' -o '{}' \\;`
  end

  desc 'Compress HTML files in output directory using Google HTML Compressor'
  task :html do
    puts `find output -name '*.html' -exec java -jar /usr/share/htmlcompressor-0.9.1/htmlcompressor-0.9.1.jar --type html '{}' -o '{}' \\;`
  end
  
  desc 'Compress XML files in output directory using Google HTML Compressor'
  task :xml do
    puts `find output -name '*.xml' -exec java -jar /usr/share/htmlcompressor-0.9.1/htmlcompressor-0.9.1.jar --type xml '{}' -o '{}' \\;`
  end

  desc 'Optimise all image, CSS, JavaScript, HTML and XML files in the output directory'
  task :all => [:jpeg, :png, :css, :js, :html, :xml]
end
