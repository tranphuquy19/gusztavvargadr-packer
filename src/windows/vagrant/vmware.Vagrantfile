Vagrant.configure(2) do |config|
  config.vm.guest = :windows
  config.vm.boot_timeout = 600

  config.vm.communicator = 'winrm'
  config.winssh.shell = 'powershell'

  config.vm.provider 'vmware_desktop' do |vw|
    vw.cpus = ${options.cpus}
    vw.memory = ${options.memory}
  end

%{ for port in options.ports ~}
  config.vm.network :forwarded_port, guest: ${port}, host: ${50000 + port}, auto_correct: true
%{ endfor ~}
end