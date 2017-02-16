# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "ubuntu/xenial64"

  config.vm.hostname = "blazegraph"

  config.vm.provider "virtualbox" do |v|
    # Blazegraph debian package has a default memory requirement of 8G, see:
    # https://github.com/blazegraph/database/blob/BLAZEGRAPH_RELEASE_2_1_4/blazegraph-deb/src/deb/conf/blazegraph#L19
    v.memory = 8192
    v.name = "blazegraph"
  end

  config.vm.network :forwarded_port, guest: 9999, host: 9999 # Blazegraph

  # packages
  shared_dir = "/vagrant"
  packages = [
    'scripts/bootstrap.sh',
    'scripts/packages/vim.sh',
    'scripts/packages/git.sh',
    'scripts/packages/java.sh',
    'scripts/packages/java7.sh',
    'scripts/packages/maven.sh',
    'scripts/packages/blazegraph.sh',
    'scripts/cleanup.sh',
  ]
  packages.each {|p| config.vm.provision "shell", path: p, args: shared_dir }

end

