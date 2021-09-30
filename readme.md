
##  What is?
Ansible playbook that installs on 3 different machines ELK stack, does simple configuration and install grafana and prometheus on machine nr 4.

## Prerequestises
* 4 VMs provisioned and on the same network/able to communicate with one another
* Ansible and module prerequisites

## Usage
* Edit inventory, add VM IPs
* Edit elk.yml and add IP's to set fact
* In elk.yml last task sets password for grafana
* run ansible-playbook -i inv.ini elk.yml

## Manual Steps
* Monitoring
* * Configuration of prom and grafana to be modified as per user requirements by the user in roles directory.

## Needed future Improvements
* elk.yml clean up, adding loops
* Making better use of variables in inventory and elk.yml, primarily remove the need to specify host ip more than once
* Setting up connection between prometheus and grafana, currently the metrics are only found on host:9100 and do not go to grafana without further user configuration
* much more :>


