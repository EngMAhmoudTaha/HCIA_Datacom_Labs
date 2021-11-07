# HCIA_Datacom_Labs
impalement all labs  of chapters and the steps for every topic

---
> [Huawei Tools Download link](https://mega.nz/folder/WkUDmQjK#jUw9HnMms1lHpdvhagCc9g) 

  ## CH4 IPv4 Basic Configurations

  1. **Login to Router (local or Remote)**
      - **Local login:** using console cable & Putty App
      - **Remote login:** using Putty App & (SSH  or telnet)
  2. **Enter to system view to begin set your configurations** 
      - **<Huawei>** system-veiw  #to enter to system view
  3. **Enter to the interface view** 
      - **[Huawei]** interface [interface type] [interface-number]
  4. **Configure the ip address for the interface**
      - **[Huawei-[interface-type-[interface-number]]]** ip address ip-address {musk | Musk-length}
  5. **Back to system view** 
      - **[Huawei-[interface-type-[interface-number]]]** quit
  6. **Back to user view**
      - **[Huawei]** quit
  7. **Save changes**
      - **<Huawei>** save
______________________________________________________________________________________________________________________________________________________________________________  
  
  ## CH5 Static Route IP Address Configuration commands
  
  ### Static Route IPv4 Configuration Steps:
  1. **Login to Router (local or Remote)**
      - **Local login:** using console cable & Putty App
      - **Remote login:** using Putty App & (SSH  or telnet)
  2. **Enter to system view to begin set your configurations** 
      - **<Huawei>** system-veiw  to enter to system view
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
      - **<Huawei>** system-veiw  __to enter to system view__
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
      - **<Huawei>** system-veiw  #to enter to system view
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
      - **<Huawei>** system-veiw  #to enter to system view
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
      - **<Huawei>** display ospf peer brief 
  3. **Check the OSPF LSDB Table**
      - **<Huawei>** display ospf lsdb 
      - **<Huawei>** display ospf routing
  4. **Check the ip routing table**
      - **<Huawei>** display ip routing-table

