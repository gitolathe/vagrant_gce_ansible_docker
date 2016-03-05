Vagrant.configure("2") do |config|
  config.vm.box = "gce"
  config.vm.provider :google do |google, override|
    google.google_project_id = "myola100"
    google.google_client_email = "ola.theander@myola.se"
    google.google_json_key_location = "/home/ola_theander/.ssh/myola100-d86b378355bf.json"
    # Define the name of the instance.
    google.name = "docker"
    # Set the zone where the instance will be located. To find out available zones:
    # `gcloud compute zones list`.
    google.zone = "europe-west1-b"
    # Set the machine type to use. To find out available types:
    # `gcloud compute machine-types list --zone asia-east1-c`.
    google.machine_type = "n1-standard-2"
    # Set the machine image to use. To find out available images:
    # `$ gcloud compute images list`.
    #google.image = "ubuntu-1404-trusty-v20150901a"
    google.image = "ubuntu-1510-wily-v20160226"
    override.ssh.username = "olathe"
    override.ssh.private_key_path = "/home/ola_theander/.ssh/id_rsa"
  end
  #
  # Provision using Ansible playbook.
  #
  config.vm.provision "ansible" do |ansible|
    ansible.groups = {
       "docker" => ["default"]
    } 
    ansible.playbook = "provisioning/playbook.yml"
  end 
end
