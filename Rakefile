require 'fileutils'

task :clean do
  FileUtils.rm_rf('slides')
end

task :build do
  `bundle exec reveal-ck generate`
end

task :serve do
  begin
    `bundle exec reveal-ck serve`
  rescue Exception => e
    # probably ctrl+c'ed
  end
end

task :default => [:clean, :build]
