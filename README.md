
# README

## Fuzzy-Q-Learning

A source code implementation of Fuzzy Q-Learning in OpenStack (IaaS cloud infrastructure)
It divide into main part : 1) HEAT template files for creating your own stack in OpenStack and 2) source code implementation of FQL in Python which will be run and executed inside of control VM created by HEAT files

# To create your stack from HEAT file :

```
heat stack-create -f autoscaling.yaml -P "network=$(neutron net-show private -F id -f value);subnet_id=$(neutron subnet-show private-subnet -F id -f value);external_network_id=$(neutron net-show public -F id -f value);OS_AUTH_URL=$OS_AUTH_URL;desired_capacity=1" asg
```
also, you can modify any input parameters in HEAT template file (autoscaling.yaml) by passing your prefered value in 'heat stack-create' command

# Contact

If you notice a bug, want to request a feature, or have a question or feedback, please send an email to hamid.arabnejad@gmail.com

