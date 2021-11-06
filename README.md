# HCIA_Datacom_Labs
impalement all labs  of chapters and the steps for every topic
---
[Huawei Tools Download link](https://mega.nz/folder/WkUDmQjK#jUw9HnMms1lHpdvhagCc9g) 
---
  ## CH4 IPv4 Basic Configurations
  ---
  ![Lab_Topology](/CH4/Basic_Conf.jpg)

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
  ---
  >![Static_route_Topology](/CH5/STATIC_Route.jpg)
  
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
