# EXERCISE 6: networking

### Listing network

1. To list networks

![image](https://github.com/user-attachments/assets/77d194b3-c09b-43a0-9355-e395a8ce6ed4)

### The default bridge network

1. inspect the bridge network by running docker network inspect bridge:

![image](https://github.com/user-attachments/assets/85481c0b-8bbf-49c6-a284-ded468b76bfc)

```
[
    {
        "Name": "bridge",
        "Id": "b658ef06f2f66aa71d2902e83193324c29e9f66d0e102c27e4d180162a771c4f",
        "Created": "2024-11-14T20:37:35.33877Z",
        "Scope": "local",
        "Driver": "bridge",
        "EnableIPv6": false,
        "IPAM": {
            "Driver": "default",
            "Options": null,
            "Config": [
                {
                    "Subnet": "172.17.0.0/16",
                    "Gateway": "172.17.0.1"
                }
            ]
        },
        "Internal": false,
        "Attachable": false,
        "Ingress": false,
        "ConfigFrom": {
            "Network": ""
        },
        "ConfigOnly": false,
        "Containers": {
            "684a7734c614008964e9dde675a595cc44f1e3d31e4548569db8f6654cf0b695": {
                "Name": "apache",
                "EndpointID": "56faf10329203c6379fe3b9605ea98f1bd7c59094d820a8c3a18aafe7e48d71a",
                "MacAddress": "02:42:ac:11:00:02",
                "IPv4Address": "172.17.0.2/16",
                "IPv6Address": ""
            }
        },
        "Options": {
            "com.docker.network.bridge.default_bridge": "true",
            "com.docker.network.bridge.enable_icc": "true",
            "com.docker.network.bridge.enable_ip_masquerade": "true",
            "com.docker.network.bridge.host_binding_ipv4": "0.0.0.0",
            "com.docker.network.bridge.name": "docker0",
            "com.docker.network.driver.mtu": "1500"
        },
        "Labels": {}
    }
]
```

2. Let's start a ping container, and inspect this again:

![image](https://github.com/user-attachments/assets/ca59b6f3-ff05-4aab-8bdd-841f5f4c9b09)

```
[
    {
        "Name": "bridge",
        "Id": "b658ef06f2f66aa71d2902e83193324c29e9f66d0e102c27e4d180162a771c4f",
        "Created": "2024-11-14T20:37:35.33877Z",
        "Scope": "local",
        "Driver": "bridge",
        "EnableIPv6": false,
        "IPAM": {
            "Driver": "default",
            "Options": null,
            "Config": [
                {
                    "Subnet": "172.17.0.0/16",
                    "Gateway": "172.17.0.1"
                }
            ]
        },
        "Internal": false,
        "Attachable": false,
        "Ingress": false,
        "ConfigFrom": {
            "Network": ""
        },
        "ConfigOnly": false,
        "Containers": {
            "684a7734c614008964e9dde675a595cc44f1e3d31e4548569db8f6654cf0b695": {
                "Name": "apache",
                "EndpointID": "56faf10329203c6379fe3b9605ea98f1bd7c59094d820a8c3a18aafe7e48d71a",
                "MacAddress": "02:42:ac:11:00:02",
                "IPv4Address": "172.17.0.2/16",
                "IPv6Address": ""
            },
            "f710705a27858685d6312c6cafbf7f2fc36c8f3d63f78aec78de4f02a63007c4": {
                "Name": "dummy",
                "EndpointID": "f11dadc0a7883ec76db3033c83743d38125b5c480c0d3a1307f388e27fb8b69f",
                "MacAddress": "02:42:ac:11:00:03",
                "IPv4Address": "172.17.0.3/16",
                "IPv6Address": ""
            }
        },
        "Options": {
            "com.docker.network.bridge.default_bridge": "true",
            "com.docker.network.bridge.enable_icc": "true",
            "com.docker.network.bridge.enable_ip_masquerade": "true",
            "com.docker.network.bridge.host_binding_ipv4": "0.0.0.0",
            "com.docker.network.bridge.name": "docker0",
            "com.docker.network.driver.mtu": "1500"
        },
        "Labels": {}
    }
]
```

3. Now let's add another ping container, and set it to ping our first.

![image](https://github.com/user-attachments/assets/c5b4c2ed-c7c4-45da-8080-4d0cf1628617)

4. 
