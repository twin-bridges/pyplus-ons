# CSV/Excel Exercise 1

1. Use the juniper_bgp.j2 template:

```
protocols {
    bgp {
        group external-peers {
            type external;
            peer-as {{ peer_as }};
            neighbor {{ neighbor1 }};
            neighbor {{ neighbor2 }};
            neighbor {{ neighbor3 }};
        }
    }
}
```

For this template create a CSV file consisting of five network devices:

```
device_name, peer_as, neighbor1, neighbor2, neighbor3
rtr1, 22, 10.10.10.99, 10.10.10.8, 10.10.10.254
...
```

2. Read the CSV file into your Python program. For each entry in the CSV file, process the CSV data through the Jinja2 template and generate an output string for each device.
