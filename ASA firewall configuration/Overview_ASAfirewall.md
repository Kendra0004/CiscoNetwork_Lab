# Configuration of ASA firewall
# Scope
The scope of the project are mentioned below:<br>
1. Configure routers in OSPF to connect.<br>
2. Configure Adaptive Security Appliance basic Settings and fire wall.<br>
3. Configure basic ASA setting and interface security levels.<br>
4. Configure routing, address translation and inspection policy.<br>
5. Configure DHCP, AAA and SSH.<br>
6. Configure a DMZ, Static NAT and ACLs.<br>
7. Verify connectivity from inside and outside ASA.<br>

# Network Topology
![Screenshot 2023-09-06 021128](https://github.com/Kendra0004/CiscoNetwork_Lab/assets/142570738/1bd32ffa-7a06-4a9e-bc27-cea7b103892c)

# OSPF configuration in routers
Routers were connected in serial interface and was connected using OSPF.<br>
The O represent the OSPF connection.<br>
router1<br>
![Screenshot 2023-09-06 024207](https://github.com/Kendra0004/CiscoNetwork_Lab/assets/142570738/dc0d426d-08a8-4b50-800a-3fff0deff274)<br>

router2<br>
![Screenshot 2023-09-06 024221](https://github.com/Kendra0004/CiscoNetwork_Lab/assets/142570738/f25b5ae1-3ed6-44f5-8146-32fb4c50f864)<br>

router3<br>
![Screenshot 2023-09-06 024233](https://github.com/Kendra0004/CiscoNetwork_Lab/assets/142570738/7dff64cc-f56f-42fe-b07e-3944ca8ed4da)<br>

# ASA configuration
Configured hostname, domain name and password to enable mode for security.

## Vlan configuration
Different vlans for inside, outside and dmz zones along with different security levels.<br>
VLAN 1 - inside<br>
VLAN 2 - outside<br>
VLAN 3 - DMZ<br>
![Screenshot 2023-09-06 021920](https://github.com/Kendra0004/CiscoNetwork_Lab/assets/142570738/2a63ec9b-bb2c-4c0d-bf82-6a9396c2f17b)<br>

## Configure routing, address translation and inspection policy
Default Static Route
Configured default static route on ASA outside.<br>
![a](https://github.com/Kendra0004/CiscoNetwork_Lab/assets/142570738/95bd15d5-bcee-4a48-8b18-828bf4279460)

Address translation using PAT
![Screenshot 2023-09-06 023051](https://github.com/Kendra0004/CiscoNetwork_Lab/assets/142570738/f463f34e-cded-4a35-851d-2c0ae6556c24)

Modify the MPF application inspection global service policy 
The packet tracer ASA does not have a default MPF policy mapped in it.<br>
![MPF app inspection global service policy](https://github.com/Kendra0004/CiscoNetwork_Lab/assets/142570738/2884866a-8c91-4a5e-ba24-9c947a1b8d9b)

## Configure DHCP, AAA and SSH
Configured DHCP pool in the ASA
![Screenshot 2023-09-06 023535](https://github.com/Kendra0004/CiscoNetwork_Lab/assets/142570738/0b42ce48-be28-457c-9ea6-f8bf86ca0f72)<br>

The inside end device PC-0 has dhcp provided ip address in place.<br>
![Screenshot 2023-09-05 100331](https://github.com/Kendra0004/CiscoNetwork_Lab/assets/142570738/abcddcf9-caec-4737-801e-8776a566bfad)<br>

Configured AAA for local database authentication and configure ssh for remote access to the ASA
![Screenshot 2023-09-06 023816](https://github.com/Kendra0004/CiscoNetwork_Lab/assets/142570738/10fab9fb-8a77-45ca-8d8d-9fa1898b8138)<br>
![Screenshot 2023-09-06 023754](https://github.com/Kendra0004/CiscoNetwork_Lab/assets/142570738/bdc29570-eb57-4f5e-9576-e78828f79b73)<br>

# Confiure DMZ, static NAT and access list
Configured network object named dmz-server, assigned it static IP address of DMZ server and using NAT to translate ip address to public ip address for ouside.<br>

Network object and NAT<br>
![Screenshot 2023-09-06 025520](https://github.com/Kendra0004/CiscoNetwork_Lab/assets/142570738/9cc36e97-2664-439a-b5d9-120082458081)<br>

Access List to permit TCP, ICMP  protocols from outside ip address to internal ip address of DMZ server.<br>
![Screenshot 2023-09-06 025536](https://github.com/Kendra0004/CiscoNetwork_Lab/assets/142570738/300d9082-e072-437a-8bb7-d2aeca883647)<br>

# Check connectivity from inside and outside
## SSH connection to ASA
Establishing ssh connection from inside end device PC-0.<br>
![Screenshot 2023-09-06 025247](https://github.com/Kendra0004/CiscoNetwork_Lab/assets/142570738/fb0974d3-d466-4760-94d6-ba410ffb3d90)

Establishing ssh connection from outside end device PC-1.<br>
![Screenshot 2023-09-06 025318](https://github.com/Kendra0004/CiscoNetwork_Lab/assets/142570738/ffb6e1d9-a777-4419-8106-a5aab69e736f)

## Connecting to DMZ server
Testing dmz outside access from outside end device PC-1 to public ip address 209.165.200.227.<br>
![Screenshot 2023-09-06 030206](https://github.com/Kendra0004/CiscoNetwork_Lab/assets/142570738/6b750dd9-0a53-40d4-a512-bbcc5dc924e5)<br>
![Screenshot 2023-09-06 030229](https://github.com/Kendra0004/CiscoNetwork_Lab/assets/142570738/b8b1cf8e-10c4-430e-a4d9-c6a54e86e11f)












