# Prometheus with Grafana using Ansible

In this project, we are configurating prometheus, node_exporter, alertmanager and Grafana. We setup Grafana dashboard which can use source as Prometheus.

## Getting Started

Step 1: Update ip address of instances in inventory file.

Step 2: Run ansible command to setup prometheus, node_exporter, alertmanager and Grafana services

Ansible command to install prometheus : ansible-playbook -i inventory.yml playbook.yml --tags prometheus -kK

                                        prometheus should then be available at machine_ip:9090 for example http://192.168.43.148:9090/status

Ansible command to install alertmanager : ansible-playbook -i inventory.yml playbook.yml --tags alertmanager -kK

                                          alertmanager should then be available at machine_ip:9093 for example http://192.168.43.148:9093/#/alerts

Ansible command to install grafana: ansible-playbook -i inventory.yml playbook.yml --tags grafana -kK

                                    grafana should then be available at machine_ip:3000 for example http://192.168.43.148:3000


Ansible command to install node_exporter : ansible-playbook -i inventory.yml playbook.yml --tags prometheus_node_exporter -kK