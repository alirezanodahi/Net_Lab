# Network Configuration with GNS3 and Ubuntu

## Overview

This project is focused on setting up a simulated network environment using GNS3 and Ubuntu. The goal is to configure both DHCP and DNS servers on Ubuntu, connect it to GNS3, and ensure that devices within the network can communicate with each other using proper network configurations.

## Requirements

- **GNS3**: Network simulation software
- **Ubuntu**: Operating system for network services (DHCP, DNS)
- **PuTTY**: SSH and Telnet client
- **VMware** or **VirtualBox**: Virtualization software for running Ubuntu
- Basic understanding of IP addressing, routing, and network services

## Steps

### 1. Set Up a Loopback IP

1. Create a loopback interface on your system.
2. Manually assign it an IP address. In this case, we will use: 192.168.2.10

### 2. Configure GNS3 VM

1. Assign an IP to the GNS3 VM in the same range as the loopback interface.
2. Ensure that the GNS3 VM is up and running (the VM status in GNS3 should turn green).

### 3. Configure Ubuntu

1. Start the Ubuntu virtual machine.
2. Manually assign it an IP address in the same range as the loopback interface:192.168.2.2

3. You should now be able to ping both the GNS3 VM and Ubuntu.

### 4. Install and Configure DHCP and DNS on Ubuntu

1. Install **DHCP** and **DNS** services on Ubuntu.
2. Configure the services according to the project requirements (refer to the project specifications for detailed steps).

### 5. Simulate Network in GNS3

1. Simulate the network environment in GNS3.
2. Run the network configuration on the GNS3 virtual machine.

### 6. Router Configuration

1. Access the router console in GNS3.
2. Assign the router its IP address based on the project requirements.
3. Verify the router's configuration by pinging the router from both the command line (`cmd`) and Ubuntu.

### 7. Set Up Telnet Access to the Router

1. Configure a username and password on the router to allow Telnet access.
2. Use **PuTTY** to Telnet into the router.
3. Once logged in, change the router's hostname to confirm successful access.

### 8. PC Configuration and Pinging

1. Access the console of `PC1` and assign it an IP address.
2. Confirm connectivity by pinging `PC1` from both the command line (`cmd`) and Ubuntu.
3. Ping the router from `PC1` to ensure proper routing.

### 9. DHCP IP Assignment

1. Initially, `PC1` does not have an IP address.
2. It will broadcast for an IP and receive one from the **DHCP** server running on Ubuntu.
3. Once assigned, you can ping all the devices (GNS3 VM, router, loopback, etc.) from `PC1`.

## Results

After completing these steps, you should have:

- Successful communication between all network nodes (GNS3 VM, Ubuntu, Router, PC).
- Functional **DHCP** and **DNS** services on Ubuntu.
- Telnet access to the router using **PuTTY**.
- A fully simulated network environment in GNS3 with routing and IP assignment.

## Troubleshooting

- If you cannot ping a device, verify that the IP addresses are correctly assigned and that the devices are in the same subnet.
- Ensure that the DHCP and DNS services are properly configured and running on Ubuntu.
- If Telnet access fails, double-check the router's username and password configuration.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
