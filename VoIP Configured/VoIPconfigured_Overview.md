# Goal
THe goal for this project was to configure IP phones correctly and have a separate vlan than the end devices such as PC.

# Network Topology
One router, one swtich and three different IP phones and PCs were used.<br>
![Screenshot 2023-09-28 091448](https://github.com/Kendra0004/CiscoNetwork_Lab/assets/142570738/740b310e-6a5d-4cfd-87bf-ef229bed70f1)

# Router Configuration
VLAN 10 is DATA which is for PCs, VLAN 20 is VOICE which is for IP phones and VLAN 50 is NATIVE.<br>
![Screenshot 2023-09-28 091619](https://github.com/Kendra0004/CiscoNetwork_Lab/assets/142570738/81184cb1-310e-4c03-a31a-4d408913e3fc)<br>

DHCP pool are created for IP phones and PCs so, ip addresses are automatically configured.<br>
![Screenshot 2023-09-28 091630](https://github.com/Kendra0004/CiscoNetwork_Lab/assets/142570738/a4be098a-9416-44e3-97d7-97acc0a16904)

Telephony service is configured to allow maximum of three phones along with source ip address and port number for its uses.
Three different IP phones numbers configured with unique buttons each.<br>
![Screenshot 2023-09-28 091606](https://github.com/Kendra0004/CiscoNetwork_Lab/assets/142570738/66c6098e-dba9-416e-a98a-5c28027adc44)
![Screenshot 2023-09-28 091612](https://github.com/Kendra0004/CiscoNetwork_Lab/assets/142570738/dc86df55-09f1-4861-901b-4a4e2185d0d7)

# Switch Configuration
Different VLAN was created and allowed in the specific ports according to the connected IP phones, PCs and more.<br>
1. VLAN 10 --> DATA<br>
2. VLAN 20 --> VOICE<br>
3. VLAN 30 --> MGT<br>
4. VLAN 40 --> MISC<br>
5. VALN 50 --> NATIVE<br>
![Screenshot 2023-09-28 091700](https://github.com/Kendra0004/CiscoNetwork_Lab/assets/142570738/39c971f4-afa1-42d3-8298-b8fd5bb262a8)

Only used ports are actived allowed VLAN 10 and 20 while shutting down the unused ports.<br>
![Screenshot 2023-09-28 093332](https://github.com/Kendra0004/CiscoNetwork_Lab/assets/142570738/cda446d0-7397-418b-84ce-0701cd178201)<br>
![Screenshot 2023-09-28 091726](https://github.com/Kendra0004/CiscoNetwork_Lab/assets/142570738/2ead9ae3-ca6a-4464-98a5-2db37bbff097)<br>

# IP Phones
Ip phones are connected to switch ports and tested if the call goes through from one phone to another.<br>
![Screenshot 2023-09-28 093820](https://github.com/Kendra0004/CiscoNetwork_Lab/assets/142570738/dc250faf-6c3f-4099-94f2-04a2bffa5135)

# PCs
PCs have automatically assigned Ip address due to DHCP pool created in router.<br>
![Screenshot 2023-09-28 093459](https://github.com/Kendra0004/CiscoNetwork_Lab/assets/142570738/a26cd27f-f062-42e1-8f31-abb36a6b0f57)




