# OpenVPN and HTTP Proxy
This repository consists of Ansible playbooks realizing these openvpn scenarios:
1. Setup OpenVPN server
2. Setup HTTP Proxy and forward traffic to an OpenVPN server

# Configure inventory (hosts)

# Use Sandbox
```sh
cd inventories/sandbox
docker-compose up -d
cd ../../
ansible-playbook -i inventories/sandbox.yml install.yml
```

# Run Playbooks
```sh
ansible-playbook install.yml
```

# TODO
1. Documentation

# License
This software is [licensed](LICENSE) under the [GPL v3 License][gpl]. © 2019 [Janstun][janstun]

[gpl]: https://www.gnu.org/licenses/gpl-3.0.en.html
[janstun]: http://www.janstun.com
