
# Cisco Packet Tracer CLI Commands

## 1. Basic Router and Switch Configuration
- **Entering Privileged EXEC Mode:**  
  ```
  enable
  ```
- **Entering Global Configuration Mode:**  
  ```
  configure terminal
  ```
- **Setting the Hostname:**  
  ```
  hostname <name>
  ```
- **Setting a Password for Privileged EXEC Mode:**  
  ```
  enable password <password>
  ```
- **Setting a Secret Password (Encrypted):**  
  ```
  enable secret <password>
  ```
- **Setting Console Password:**  
  ```
  line console 0
  password <password>
  login
  ```
- **Setting VTY Password (for Telnet/SSH):**  
  ```
  line vty 0 4
  password <password>
  login
  ```
- **Configuring a Banner:**  
  ```
  banner motd #<message>#
  ```

## 2. Interface Configuration
- **Accessing an Interface:**  
  ```
  interface <type> <number>
  ```
  Example: `interface gigabitEthernet 0/0`
- **Assigning an IP Address to an Interface:**  
  ```
  ip address <IP> <Subnet_Mask>
  no shutdown
  ```
- **Enabling/Disabling an Interface:**  
  ```
  no shutdown       // Enable
  shutdown          // Disable
  ```

## 3. VLAN Configuration (on Switches)
- **Creating a VLAN:**  
  ```
  vlan <VLAN_ID>
  name <VLAN_Name>
  ```
- **Assigning VLAN to an Interface:**  
  ```
  interface <type> <number>
  switchport mode access
  switchport access vlan <VLAN_ID>
  ```
- **Configuring Trunk Ports:**  
  ```
  interface <type> <number>
  switchport mode trunk
  switchport trunk allowed vlan <VLAN_IDs>
  ```

## 4. Routing
- **Enabling a Routing Protocol (e.g., RIP):**  
  ```
  router rip
  version 2
  network <network_address>
  ```
- **Configuring Static Routes:**  
  ```
  ip route <destination_network> <subnet_mask> <next_hop_IP>
  ```
- **Default Route (Gateway of Last Resort):**  
  ```
  ip route 0.0.0.0 0.0.0.0 <next_hop_IP>
  ```

## 5. Access Control Lists (ACLs)
- **Standard ACL:**  
  ```
  access-list <ACL_Number> permit/deny <source_IP> <wildcard_mask>
  ```
  Example: `access-list 1 permit 192.168.1.0 0.0.0.255`
- **Applying ACL to an Interface:**  
  ```
  interface <type> <number>
  ip access-group <ACL_Number> in/out
  ```

## 6. Saving and Verifying Configuration
- **Save Configuration:**  
  ```
  copy running-config startup-config
  ```
- **Show Running Configuration:**  
  ```
  show running-config
  ```
- **Show Startup Configuration:**  
  ```
  show startup-config
  ```

## 7. Troubleshooting and Monitoring
- **Ping a Host/Network:**  
  ```
  ping <IP_address>
  ```
- **Trace Route:**  
  ```
  traceroute <IP_address>
  ```
- **Display Routing Table:**  
  ```
  show ip route
  ```
- **Display Interface Status:**  
  ```
  show ip interface brief
  ```
- **View MAC Address Table (Switch):**  
  ```
  show mac address-table
  ```

## PC Command Prompt Commands

- **Ping a Host:**  
  ```
  ping <IP_address>
  ```
  Example: `ping 192.168.1.1`
- **Check Network Configuration:**  
  ```
  ipconfig
  ```
  For detailed information:  
  ```
  ipconfig /all
  ```
- **Clear ARP Cache:**  
  ```
  arp -d
  ```
- **Display ARP Table:**  
  ```
  arp -a
  ```
- **Trace Route:**  
  ```
  tracert <IP_address>
  ```
- **Check Connectivity to a Specific Port:**  
  ```
  telnet <IP_address> <port_number>
  ```
  Example: `telnet 192.168.1.1 80`
- **Test DNS Resolution:**  
  ```
  nslookup <domain_name>
  ```
- **Release and Renew IP Address:**  
  ```
  ipconfig /release
  ipconfig /renew
  ```
