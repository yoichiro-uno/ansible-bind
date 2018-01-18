allow_access_v4: "port 53 { 127.0.0.1; any; }"
allow_access_v6: "{ none; }"
domain_name:
  - example.com.
allow_query_from: "172.xx.0.0/16; 192.xx.0.0/16;"
name_server: "{{ inventory_hostname }}"
recursion: yes
servers:
  - { hostname: nameserver01, ip: 172.xx.xx.xxx }
  - { hostname: ns, ip: 172.xx.xx.xxx }
  - { hostname: clientname01, ip: 172.xx.xx.xxx }
  - { hostname: clientname02, ip: 192.xx.xx.xxx }

    name_server: "{{ inventory_hostname }}"
    recursion: yes
    servers:



container_name: nameserver01
container_image: centos
container_ports:
  - "53:53"
