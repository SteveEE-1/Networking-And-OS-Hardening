# Networking

## Protocols


### DNS

**Domain name System**, When a domain name example `google.com` it goes to the DNS server and fetches the appropriate ip address of that particular domain. 
**Recursive resolution** = DNS server does all the work of resolving the name.

The **+** in your tcpdump shows the **"Recursion Desired"** flag is set — so you're asking the `DNS server to resolve everything and return just the IP`.

### UDP

**User Datagram Protocol** ,It directly does transmission of data without any connection to that server or system. Connectionless protocol.

### TCP

**Transmission control protocol**, `Transport Layer`.Connects with the particular system or server and check if they system acknowledges the particular request. It follows a `Three way handshake`


### HTTPS

**Hyper Text Transfer Protocol** , Its a more secure way connection via web servers and client. It encrypts the data using `TLS/SSL` encryption menthods. So if an attacker cant view the data during the transmission.
`Application Layer`. This is a security protocol.


### Simple Network Management Protocol (SNMP)

Is a network protocol used for monitoring and managing devices on a network. SNMP can reset a password on a network device or change its baseline configuration. Can be used for reporting how much bandwidth is being used 


### nternet Control Message Protocol (ICMP)  

Its used for checking data transmission errors across the the network.
Used to troubleshoot the network and latency by pinging. 


### Secure File Transfer Protocol (SFTP)

Mainly used in file transfer uses SSH protocol for file transfer. It encrypts using **AES(Advanced encryption standard)** so it cant be intercepted and read.



### DHCP (Dynamic Host Configuration Protocol)

It assigns a devices its IP address and other configuration on a network.

### ARP (Address Resolution Protocol)

It translates the IP address in the data packets into **MAC** addresses so that the devices can be found in the local network. Does not have port number since its layer 2 protocol.


### Telnet

Used to remotely connect with devices over network. Sends information via clear text.

### SSH (Secure Shell)

Securily connect to a remote system. Serves authentication and encryptions.

### IMAP (Internet Message Access Protocol)

IMAP is used for incoming email. Donwloads headers of emails and message content. Once the mail is downloaded it doesnt get deleted from the server and can be accessed again from multiple devices.

# PORTS

| **Protocol/Service**      | **Port Number** | **Transport** | **Encryption**            |
| ------------------------- | --------------- | ------------- | ------------------------- |
| **DHCP (Server)**         | 67              | UDP           | ❌                         |
| **DHCP (Client)**         | 68              | UDP           | ❌                         |
| **Telnet**                | 23              | TCP           | ❌                         |
| **SSH**                   | 22              | TCP           | ✅ (Encrypted)             |
| **SFTP**                  | 22              | TCP           | ✅ (via SSH)               |
| **POP3**                  | 110             | TCP/UDP       | ❌                         |
| **POP3S (POP3 over SSL)** | 995             | TCP/UDP       | ✅ (SSL/TLS)               |
| **IMAP**                  | 143             | TCP           | ❌                         |
| **IMAPS (IMAP over SSL)** | 993             | TCP           | ✅ (SSL/TLS)               |
| **SMTP**                  | 25              | TCP/UDP       | ❌                         |
| **SMTPS (SMTP with TLS)** | 587             | TCP/UDP       | ✅ (TLS)                   |
| **HTTP**                  | 80              | TCP           | ❌                         |
| **HTTPS**                 | 443             | TCP           | ✅ (SSL/TLS)               |
| **DNS**                   | 53              | TCP/UDP       | ❌ (typically unencrypted) |




# Security Zones

Security Technique that divides the network into segments. Each segment has its own security measures and permissions, Secuity Zone controls who can access certain segments. Barrier to internal networks to keep corporates and there info same from the internet.


Example : `A hotel that offers free public Wi-Fi.The unsecured guest network is kept separate fromanother encrypted network used by the hotel staff. `


## Types of Security Zones

### Controlled

Subent that protects the internal network from the internet or **Uncontrolled Zone**
Several types inside the controlled zone. 

Outer layer contains **DMZ (Demilitarized Zone)** which acts as a buffer between the and the organizations data. It allows users to access the services of website but the user wont be able to all the services as there are authentication and permissions needed to get certain access or services.


### Firwalls

**Statless** : It has predefined rules and does not keep track of data packets being receieved.

**Statful** : It practively keeps in track of the packets being received.
Only requires in one direction cause it uses a `State table` to track connections so it can match return traffic to an existing session


### DMZ

DMZ is placed between 2 firewalls where each firewall is equipped with certain access control policies which the security analyst sets. There firewall regulate the incoming traffic and restricts certain **ports and IP's**

### Uncontrolled Zone

Any Network outside the organizations control


# Subnetting

Method in which a network gets divided into smaller networks and this can be more efficient and fast. These smaller networks function as their own networks. Different subnets can communicate with each other via a **router**. If they want to communicate in the same network they use a **switch**

## CIDR (Classless Inter-Domain Routing notation for subnetting) 

Assign subnet masks to ip addresses to create a subnet.

`IPV4 192,168.0.0/24` Here the `24` means the range of the ip addresses.
ranges from `192.168.0.0`  to `192.168.0.255`.



# Proxy servers

They fullfill the clients request and forwards them onto another server. They basically act like a man in the middle but the secure edition. Proxies check whether a connection request is safe or not. Proxies have public ip address which keep the private ip address hidden from malicious users.

Proxies have a temporary memory to store data which are regularly requested by the external servers. 



## Types of Proxies

| Type              | Who it protects/represents | Main Job                        | Who uses it?   |
| ----------------- | -------------------------- | ------------------------------- | -------------- |
| **Forward Proxy** | **Client (you)**           | Hides clients from the internet | Users          |
| **Reverse Proxy** | **Server**                 | Hides servers from the internet | Website owners |

### Reverse Proxy 

Shields the client server from the incoming traffic. It validates each requests and sees if its fit to pass through.

### Forward Proxy 

Shields the users in the internal servers from the uncontrolled zone. 


 
##
# TCPDUMP LOGS


**Network protocol analyzer** is basically a packet sniffer or packet analyzer. Used to capture and analyze the packet or data traffic within a network.


**PICTURE OF TCP DUMP**

![TCP Dump](images/tcpdump.png)





## PACKET SPOOFING

A network attack performed when an attacker changes the source IP of a data packet to impersonate an authorized system and gain access to a network

Packet contains a header, Where the Ip address is stored and a body where valuable information is stored.


### Active packet sniffing : 

When a person modifies the packet to redirect to a different port or inject malicious code into so that it can harm your system or server once its been reached is called Active Packet Sniffing

### Passive packet sniffing:

When a person just views the value inside the packet but doesnt modify it or inject it.

# Types of attacks

### Smurf attack: 
`A network attack performed when an attacker sniffs an authorized user’s IP address and floods it with ICMP packets`


### Replay attack:
`A network attack performed when a malicious actor intercepts a data packet in transit and delays it or repeats it at another time`


