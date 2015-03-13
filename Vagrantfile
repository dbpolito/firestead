require 'json'
require 'yaml'

VAGRANTFILE_API_VERSION = "2"

firesteadYamlPath = File.expand_path("./firestead/config.yaml")
afterScriptPath = File.expand_path("./firestead/after.sh")
aliasesPath = File.expand_path("./firestead/aliases")

require_relative 'firestead/config.rb'

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
	if File.exists? aliasesPath then
		config.vm.provision "file", source: aliasesPath, destination: "~/.bash_aliases"
	end

	Homestead.configure(config, YAML::load(File.read(firesteadYamlPath)))

	if File.exists? afterScriptPath then
		config.vm.provision "shell", path: afterScriptPath
	end
end
