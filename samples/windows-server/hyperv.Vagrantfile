Vagrant.configure(2) do |config|
  config.vm.guest = :windows
  config.vm.boot_timeout = 600

  config.vm.communicator = 'winrm'
  config.winssh.shell = 'powershell'

  config.vm.provider 'hyperv' do |h|
    h.cpus = 2
    h.memory = 2048
    h.ip_address_timeout = 600
  end
end
