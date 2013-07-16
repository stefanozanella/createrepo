require 'rake'

root_dir = File.join(File.dirname(__FILE__))
install_dir = 'dist'

task :install do
  FileUtils.cd(root_dir) do
    system("export DESTDIR=#{File.join(root_dir, install_dir)} && make install")
  end
end

task :clean do
  FileUtils.rm_rf install_dir
end

desc 'Install createrepo in local folder via Vagrant'
task :default => :clean do
  system "vagrant up"
  system "vagrant ssh -c 'sudo gem install rake --no-rdoc --no-ri'"
  system "vagrant ssh -c 'rake -f /vagrant/#{File.basename __FILE__} install'"
end
