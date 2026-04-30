deploy:
	clab dep -t lab1.yml --reconfigure
destroy:
	clab des -t lab1.yml --cleanup
help:
	@echo "\033[1;32m===== Untagging the eth1 at Host1 =====\033[0m"
	@echo " ip addr del 10.10.10.2/24 dev eth1.100"
	@echo " ip link set eth1.100 down"
	@echo " ip link delete link eth1 name eth1.100 type vlan id 100"

test:
	docker exec -ti clab-lab1-host1 ping 10.0.0.3 -c 2
	docker exec -ti clab-lab1-host1 ping 10.0.1.2 -c 2
	docker exec -ti clab-lab1-host1 ping 10.0.1.3 -c 2


show:
	docker exec -ti clab-lab1-leaf1 sr_cli -c "show network-instance default protocols bgp neighbor"
	
leaf1:
	docker exec -ti clab-lab1-leaf1 sr_cli

host1:
	docker exec -ti clab-lab1-host1 bash
