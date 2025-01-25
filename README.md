
# Cisco Packet Tracer CLI Commands

## 1. Basic Router and Switch Configuration
- **Entering Privileged EXEC Mode:**  
  ```
  enable  // Short: en
  ```
  *Purpose:* Access high-level administrative commands.
  
- **Entering Global Configuration Mode:**  
  ```
  configure terminal  // Short: conf t
  ```
  *Purpose:* Configure router or switch settings.

- **Setting the Hostname:**  
  ```
  hostname <name>
  ```
  *Purpose:* Assign a name to the device for identification.

- **Setting a Password for Privileged EXEC Mode:**  
  ```
  enable password <password>
  ```
  *Purpose:* Protect privileged EXEC mode with a password.

- **Setting a Secret Password (Encrypted):**  
  ```
  enable secret <password>
  ```
  *Purpose:* Encrypt and secure privileged EXEC mode access.

- **Setting Console Password:**  
  ```
  line console 0
  password <password>
  login
  ```
  *Purpose:* Set a password for console access.

- **Setting VTY Password (for Telnet/SSH):**  
  ```
  line vty 0 4
  password <password>
  login
  ```
  *Purpose:* Secure remote access via Telnet or SSH.

- **Configuring a Banner:**  
  ```
  banner motd #<message>#
  ```
  *Purpose:* Display a message upon login.

## 2. Interface Configuration
- **Accessing an Interface:**  
  ```
  interface <type> <number>  // Short: int <type> <number>
  ```
  *Purpose:* Configure specific network interfaces.

- **Assigning an IP Address to an Interface:**  
  ```
  ip address <IP> <Subnet_Mask>
  no shutdown  // Short: no shut
  ```
  *Purpose:* Enable and configure interface with IP settings.

- **Enabling/Disabling an Interface:**  
  ```
  no shutdown       // Enable
  shutdown          // Disable
  ```
  *Purpose:* Turn an interface on or off.

## 3. VLAN Configuration (on Switches)
- **Creating a VLAN:**  
  ```
  vlan <VLAN_ID>
  name <VLAN_Name>
  ```
  *Purpose:* Define a new VLAN and assign a name.

- **Assigning VLAN to an Interface:**  
  ```
  interface <type> <number>  // Short: int <type> <number>
  switchport mode access     // Short: sw mo ac
  switchport access vlan <VLAN_ID>  // Short: sw ac vl <VLAN_ID>
  ```
  *Purpose:* Bind an interface to a specific VLAN.

- **Configuring Trunk Ports:**  
  ```
  interface <type> <number>  // Short: int <type> <number>
  switchport mode trunk      // Short: sw mo tr
  switchport trunk allowed vlan <VLAN_IDs>  // Short: sw tr al vl <VLAN_IDs>
  ```
  *Purpose:* Allow multiple VLAN traffic on a trunk link.

## 4. Routing
- **Enabling a Routing Protocol (e.g., RIP):**  
  ```
  router rip
  version 2
  network <network_address>
  ```
  *Purpose:* Enable dynamic routing for specific networks.

- **Configuring Static Routes:**  
  ```
  ip route <destination_network> <subnet_mask> <next_hop_IP>
  ```
  *Purpose:* Manually define a route to a network.

- **Default Route (Gateway of Last Resort):**  
  ```
  ip route 0.0.0.0 0.0.0.0 <next_hop_IP>
  ```
  *Purpose:* Configure a fallback route for unknown networks.

## 5. Access Control Lists (ACLs)
- **Standard ACL:**  
  ```
  access-list <ACL_Number> permit/deny <source_IP> <wildcard_mask>  // Short: acc-l <ACL_Number>
  ```
  *Purpose:* Control access to resources using IP rules.

- **Applying ACL to an Interface:**  
  ```
  interface <type> <number>  // Short: int <type> <number>
  ip access-group <ACL_Number> in/out
  ```
  *Purpose:* Apply ACL rules to an interface for inbound/outbound traffic.

## 6. Saving and Verifying Configuration
- **Save Configuration:**  
  ```
  copy running-config startup-config  // Short: wr
  ```
  *Purpose:* Save current settings to persistent memory.

- **Show Running Configuration:**  
  ```
  show running-config  // Short: sh run
  ```
  *Purpose:* Display current configurations.

- **Show Startup Configuration:**  
  ```
  show startup-config  // Short: sh start
  ```
  *Purpose:* View saved configurations in memory.

## 7. Troubleshooting and Monitoring
- **Ping a Host/Network:**  
  ```
  ping <IP_address>
  ```
  *Purpose:* Test connectivity to a specific host.

- **Trace Route:**  
  ```
  traceroute <IP_address>  // Short: trace <IP_address>
  ```
  *Purpose:* Identify the path packets take to a destination.

- **Display Routing Table:**  
  ```
  show ip route  // Short: sh ip ro
  ```
  *Purpose:* Display routing information.

- **Display Interface Status:**  
  ```
  show ip interface brief  // Short: sh ip int br
  ```
  *Purpose:* View interface IP and status summary.

- **View MAC Address Table (Switch):**  
  ```
  show mac address-table  // Short: sh mac ad
  ```
  *Purpose:* Display MAC address table on a switch.

## PC Command Prompt Commands
- **Ping a Host:**  
  ```
  ping <IP_address>
  ```
  *Purpose:* Verify connectivity to a specific device.

- **Check Network Configuration:**  
  ```
  ipconfig
  ```
  *Purpose:* Display basic IP settings.

  For detailed information:  
  ```
  ipconfig /all
  ```

- **Clear ARP Cache:**  
  ```
  arp -d
  ```
  *Purpose:* Clear cached ARP entries.

- **Display ARP Table:**  
  ```
  arp -a
  ```
  *Purpose:* View current ARP entries.

- **Trace Route:**  
  ```
  tracert <IP_address>
  ```
  *Purpose:* Identify the network path to a host.

- **Check Connectivity to a Specific Port:**  
  ```
  telnet <IP_address> <port_number>
  ```
  *Purpose:* Test connectivity to a device on a specific port.

- **Test DNS Resolution:**  
  ```
  nslookup <domain_name>
  ```
  *Purpose:* Resolve domain names to IP addresses.

- **Release and Renew IP Address:**  
  ```
  ipconfig /release
  ipconfig /renew
  ```
  *Purpose:* Reset and renew the device's IP configuration.

