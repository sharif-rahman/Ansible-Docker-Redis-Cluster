# Ansible-Docker-Redis-Cluster

## Before Run the Playbook Please follow this steps

# Add the redis Nodes Ip in  /etc/hosts file

``` 
192.*.*.10 redis1
192.*.*.10 redis2
192.*.*.10 redis3 
```

# Add the redis Nodes Ip in  /group_vars/global/vars.yml file

```
master:
      node1:                       # Redis-node1 IP
      node2:                       # Redis-node2 IP
      node3:                       # Redis-node3 IP
```



# Run the Playbook 

ansible-playbook /etc/ansible/playbooks/deploy/redis.yml


OutPut 

Node1

```
CONTAINER ID        IMAGE                         COMMAND                  CREATED             STATUS              PORTS
858be3369c99        redis:5.0.0                   "docker-entrypoint..."   12 days ago         Up 55 minutes       0.0.0.0:7003->7003/tcp, 6379/tcp, 0.0.0.0:17003->17003/tcp   redis-SM3
2028174ad03d        redis:5.0.0                   "docker-entrypoint..."   12 days ago         Up 55 minutes       0.0.0.0:7001->7001/tcp, 6379/tcp, 0.0.0.0:17001->17001/tcp   redis-M1
```
