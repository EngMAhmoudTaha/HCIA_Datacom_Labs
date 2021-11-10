# HCIA_Datacom_Labs
impalement all labs  of chapters and the steps for every topic

---
> [Huawei Tools Download link](https://mega.nz/folder/WkUDmQjK#jUw9HnMms1lHpdvhagCc9g) 

  ## CH4 IPv4 Basic Configurations

  1. **Login to Router (local or Remote)**
      - **Local login:** using console cable & Putty App
      - **Remote login:** using Putty App & (SSH  or telnet)
  2. **Enter to system view to begin set your configurations** 
      - **\<Huawei\>** system-veiw  #to enter to system view
  3. **Enter to the interface view** 
      - **[Huawei]** interface [interface type] [interface-number]
  4. **Configure the ip address for the interface**
      - **[Huawei-[interface-type-[interface-number]]]** ip address ip-address {musk | Musk-length}
  5. **Back to system view** 
      - **[Huawei-[interface-type-[interface-number]]]** quit
  6. **Back to user view**
      - **[Huawei]** quit
  7. **Save changes**
      - **\<Huawei\>** save
______________________________________________________________________________________________________________________________________________________________________________  
  
  ## CH5 Static Route IP Address Configuration commands
  
  ### Static Route IPv4 Configuration Steps:
  1. **Login to Router (local or Remote)**
      - **Local login:** using console cable & Putty App
      - **Remote login:** using Putty App & (SSH  or telnet)
  2. **Enter to system view to begin set your configurations** 
      - **\<Huawei\>** system-veiw  to enter to system view
  3. **Specify the next hop IP address for static route**
      - **[Huawei]** ip route-static network-address {mask | mask length} next-hop_ip_address
  4. **Specify an outbound interface for static route**
      - **[Huawei]** ip route-static network-address {mask | mask length} interface-type interface-number
  5. **Specify an outbound interface and next-hop address for static route**
      - **[Huawei]** ip route-static network-address {mask | mask length}  interface-type interface-number [next-hop address]
     
  ### Static Route IPV6 Address Configuration Steps:
  1. **Login to Router (local or Remote)**
      - **Local login:** using console cable & Putty App
      - **Remote login:** using Putty App & (SSH  or telnet)
  2. **Enter to system view to begin set your configurations** 
      - **\<Huawei\>** system-veiw  __to enter to system view__
  3. **Enable IPv6**
      - **[Huawei]** ipv6
  4. **Specify the next hop IP address for static route**
      - **[Huawei]** ipv6 route-static network-address prefix next-hop_ip_address
  5. **Specify an outbound interface for static route**
      - **[Huawei]** ipv6 route-static network-address prefix interface-type interface-number
  6. **Specify bout an outbound interface and next-hop address for static route**
      - **[Huawei]** ipv6 route-static network-address prefix  interface-type interface-number [next-hop address]
  ___________________________________________________________________________________________________________________________________________________________________________
  
  ## CH6 OSPF Basics
  ### Primary Configurations
  1. **Login to Router (local or Remote)**
      - **Local login:** using console cable & Putty App
      - **Remote login:** using Putty App & (SSH  or telnet)
  2. **Enter to system view to begin set your configurations** 
      - **\<Huawei\>** system-veiw  #to enter to system view
  3.  **Create and run an OSPF process and enter the OSPF view**
      - **[Huawei]** ospf [process-id | router-id router-id]
  4. **Create an OSPF area and enter the OSPF area view**
      - **[Huawei-ospf-process-id]** area area-id
  5. **Set an ospf bandwidth reference value *(optional)* **
      - **[Huawei-[interface-type-[interface-number]]]** bandwidth-reference value
  6. **Specify the interfaces that are belong to the OSPF area**
      - **[Huawei-ospf-[process-id]-area-[area-num]]** network network-address wildcard
  
  
  ### Advanced Configuration
  1. **Login to Router (local or Remote)**
      - **Local login:** using console cable & Putty App
      - **Remote login:** using Putty App & (SSH  or telnet)
  2. **Enter to system view to begin set your configurations** 
      - **\<Huawei\>** system-veiw  #to enter to system view
  3. **Enter to the interface view** 
      - **[Huawei]** interface [interface type] [interface-number]
  4. **Set an OSPF interface cost**
      - **[Huawei-[interface-type-[interface-number]]]** ospf cost cost
  5. **Set the priority of an interface for an DR election**
      - **[Huawei-[interface-type-[interface-number]]]** ospf dr-priority priority

  
  
  ### Troubleshooting & validate Configuration
  1. **Login to Router (local or Remote)**
      - **Local login:** using console cable & Putty App
      - **Remote login:** using Putty App & (SSH  or telnet)
  2. **Check the OSPF neighbor Table**
      - **\<Huawei\>** display ospf peer brief 
  3. **Check the OSPF LSDB Table**
      - **\<Huawei\>** display ospf lsdb 
      - **\<Huawei\>** display ospf routing
  4. **Check the ip routing table**
      - **\<Huawei\>** display ip routing-table
  ---
  ## CH7&8 Ethernet switching and VLAN Basics
  ### Basic Interface-VLAN Configuration commands
  1. **Login to Router (local or Remote)**
      - **Local login:** using console cable & Putty App
      - **Remote login:** using Putty App & (SSH  or telnet)
  2. **Enter to system view to begin set your configurations** 
      - **\<Huawei\>** system-veiw  #to enter to system view
  3. **Create one or more VLANs**
      - **If create one vlan**
          - **[Huawei]** vlan vlanid
      - **If more vlans**
          - **[Huawei]** vlan batch {vlan_id1 to vlan_id2}
  4. **Enter to the interface view** 
      - **[Huawei]** interface [interface type] \[interface-number\]
  5. **Set the link type of an interface**
      - **[Huawei-[interface-type-[interface-number]]]** port link-type {access | trunk | hybrid } 
  6. **Configure a default VLAN for** 
      - **The access interface**
          - **[Huawei-[interface-type-[interface-number]]]** port default vlan vlan-id
      - **The trunk interface**
          - **[Huawei-[interface-type-[interface-number]]]** port trunk pvid vlan  vlan-id
      - **The hybrid interface**
          - **[Huawei-[interface-type-[interface-number]]]** port hybrid pvid vlan vlan-id
  7. **Allow the VLANs that are passed from this trunk interface** 
      - **[Huawei-[interface-type-[interface-number]]]** port trunk allow-pass vlan {[vlan-id1 to {vlan_id2}] | all }
  8. **Specify the VLANs that  act untagged and VLANs that act tagged** 
      - **[Huawei-[interface-type-[interface-number]]]** port hybrid untagged vlan {[vlan-id1 to {vlan_id2}]
      - **[Huawei-[interface-type-[interface-number]]]** port hybrid tagged vlan {[vlan-id1 to {vlan_id2}]
  9. **Verify the configuration**
      - **\<Huawei\>** display vlan
  
  ### Basic MAC-VLAN Configuration commands
  1. **Login to Router (local or Remote)**
      - **Local login:** using console cable & Putty App
      - **Remote login:** using Putty App & (SSH  or telnet)
  2. **Enter to system view to begin set your configurations** 
      - **\<Huawei\>** system-veiw  #to enter to system view
  3. **Create one or more VLANs**
      - **If create one vlan**
          - **[Huawei] vlan vlanid**
      - **If more vlans**
          - **[Huawei]** vlan batch {vlan_id1 to vlan_id2}
  4. **Enter to vlan vlan-id view**
      - **[Huawei]** vlan vlan-id
  5. **Associate a Mac address with a VLAN**
      - **[Huawei-vlan-[vlan-id]]** mac-vlan mac-address mac-address[mask | mask-length]
  6. **Enter to the interface view** 
      - **[Huawei]** interface [interface type] [interface-number]
  7. **Enable mac-address based VLAN assignment on an interface**
      - **[Huawei-[interface-type-[interface-number]]]** mac-vlan enable

  ---
  ## CH9 Spanning Tree Protocol (STP)
  1. **Login to Router (local or Remote)**
      - **Local login:** using console cable & Putty App
      - **Remote login:** using Putty App & (SSH  or telnet)
  2. **Enter to system view to begin set your configurations** 
      - **\<Huawei\>** system-veiw  #to enter to system view
  3. **Configure a working mode**
      - **[Huawei]** stp mode { stp | rstp | mstp }
  4. **Configure a root bridge *(optional)***
      - **[Huawei]** stp root primary 
  5. **Configure a secondary root bridge *(optional)***
      - **[Huawei]** stp root secondary 
  6. **Configure a STP priority of a switch *(optional)***
      - **[Huawei]** stp priority priority 
  7. **Configure a path cost for a port *(optional)***
      - **[Huawei]** stp pathcost-standared {dot1d-1998 | dot1t | legacy }
      - **[Huawei-[interface-type-[interface-number]]]** stp cost cost
  8. **Configure a priority for a port**
      - **[Huawei-[interface-type-[interface-number]]]** stp priority priority
  9. **Enable STP, RSTP, MSTP**
      - **[Huawei]** stp enable
  10. **Validate the STP**
      - **\<Huawei\>** display stp brief

---

  ## CH11 Eth-Trunk 
  
  1. **Login to Router (local or Remote)**
      - **Local login:** using console cable & Putty App
      - **Remote login:** using Putty App & (SSH  or telnet)
  2. **Enter to system view to begin set your configurations** 
      - **\<Huawei\>** system-veiw  #to enter to system view
  3. **Create an ether trunk**
      - **[Huawei]** interface eth_trunk trunk_id
  4. **Configure a link aggregation mode**
      - **IF you want LACP mode**
          - **[Huawei-Eth-Trunk-Trunk_ID]** mode lacp
      - **If you want manual mode**
          - **[Huawei-Eth-Trunk-Trunk_ID]** mode manual load-balance
   5. **Add an interface to Eth-Trunk**
      - **From Interface View** 
          - **[Huawei]** interface \[interface type\] \[interface-number\]
          - **[Huawei-[interface-type-[interface-number]]]** eth-trunk trunk_id
      - **From Eth-Trunk view**
          - **[Huawei-Eth-Trunk-Trunk_ID]** trunkport \[interface type\] \[interface-number\]
  6. **Enable the interfaces of different rate are added to the Eth-Trunk**
      - **[Huawei-Eth-Trunk-Trunk_ID]** mixed-rate link enable
  7. Configure the LACP system priority
      -	**[Huawei-Eth-Trunk-Trunk_ID]** lacp priority pariority
  8. Configure The max. number of active interfaces
      - **[Huawei-Eth-Trunk-Trunk_ID]** max link-activenumber number
  9. Configure The min. number of active interfaces
      - **[Huawei-Eth-Trunk-Trunk_ID]** least link-activenumber number
  10. Configure the LACP interface priority
      - **[Huawei-[interface-type-[interface-number]]]** lacp priority priority
---
  ## CH19 IPv6 Basic
  ### Basic IPV6 Address Configuration commands
  1.  **Login to Router (local or Remote)**
      - **Local login:** using console cable & Putty App
      - **Remote login:** using Putty App & (SSH  or telnet)
  2. **Enter to system view to begin set your configurations** 
      - **\<Huawei\>** system-veiw  #to enter to system view
  3. **Enable IPv6**
      - **From system view:**
          - **[Huawei]** ipv6
      - **From Interface View:**
          - **[Huawei]** interface \[interface type\] \[interface-number\]
          - **[Huawei-[interface-type-[interface-number]]]** ipv6 enable
  4. **Enter to interface view**
      - **[Huawei]** interface \[interface type]\ \[interface-number\]
  5. **Configure LLA for the interface**
      - **If you want manual configuration**
          - **[Huawei-[interface-type-[interface-number]]]** ipv6 address ip-address link-local
      - **If you want auto configuration**
           - **[Huawei-[interface-type-[interface-number]]]** ipv6 address auto link-local
  6. Configure GUA for the interface
      - **If you want manual configuration**
           - **[Huawei-[interface-type-[interface-number]]]** ipv6 address {ip-address prefix-length | ip-address/prefix-length}
      - **If you want statfull auto configuration (use DHCP)**
           - **[Huawei-[interface-type-[interface-number]]]** ipv6 address auto dhcp
      - **If you want statless auto configuration**
           - **[Huawei-[interface-type-[interface-number]]]** ipv6 address auto global
  7. Enable the interface send RA message
      - **\[Huawei-\[interface-type-\[interface-number\]\]\]** undo ipv6 nd ra halt
  
  ### Troubleshoot Configuration steps:
  1. **Login to Router (local or Remote)**
        - **Local login:** using console cable & Putty App
        - **Remote login:** using Putty App & (SSH  or telnet)
  2. **Enter to system view to begin set your configurations** 
        - **\<Huawei\>** system-veiw  #to enter to system view
  3. **Display IPv6 information on an interface**
        - **\[Huawei\]** display ipv6 interface {brief | \[interface-type\]-\[interface-number\]}
  4. **Display neighbor entry information**
        - **\[Huawei\]** display ipv6 neighbors


