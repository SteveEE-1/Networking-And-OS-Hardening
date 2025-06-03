# OS Hardening

## VMS  (Virtual Machines)

Like physical systems but they can run code in an isolated environment, Which prevents damage of your host system. Used to investigate infected machines and to test out malware. Help you to screenshot (basically like save your system at its current time) incase if anything goes wrong, you can revert back to default.

## SandBoxes 

A sandbox is a type of testing environment that allows you to execute software or programs separate from your network.They are commonly used for testing patches, identifying and addressing bugs, or detecting cybersecurity vulnerabilities. Sandboxes can also be used to evaluate suspicious software, evaluate files containing malicious code, and simulate attack scenarios. 


## Prevention Measures

### Salting and Hashing:

    Hashing Converts the data into a unique value which works in a one way direction. Meaning once its encrypted its impossible to decrypt it. Salting just adds extra set of letters in the middle to increase the word length and make it more secure.


### MFA and 2FA:
     It provides an additonal layer of security. If the infiltrator suppose brute forces his way through the password. It will ask the for additional security requirements to eventually get full access. This can be getting a OTP via your phone number or having Facial recognition.

### CAPTCHA and reCAPTHC

    CAPTCHA stands for Completely Automated Public Turing test to tell Computers and Humans Apart. It asks users to complete a simple test that proves they are human. This helps prevent software from trying to brute force a password. reCAPTCHA is a free CAPTCHA service from Google that helps protect websites from bots and malicious software.



## TCP Flag codes

### TCP Flag codes include:

##### Flags [S]  - Connection Start 

##### Flags [F]  - Connection Finish

##### Flags [P]  - Data Push

##### Flags [R]  - Connection Reset

##### Flags [.]  - Acknowledgment
#
# Network security Hardening Tools


## IDS (Intrusion Detection System)

    It helps monitor system activity and alerts on possible intrusion.

    Its already configured to detect known attacks.

    It also looks out for anomalies.

    Its placed after the firewall because the firewall restricts certain ports. So traffic coming in through those ports are rejected and the allowed ones go through the IDS.

## Intrusion Prevention System 

    It helps to monitor intrsuive activity and helps stop it.

    Better than IDS since it stops the intrusive activity ones detected. 

    Limitation it has false positives(legitmate users are blocked) and if the inline(connection between the private network and internet) breaks.

## Security Information and event management Tool

    To analyze log data and to monitor incoming traffic. It gets the log from IPS, IDS, DNS logs, firewalls, VPNS and proxies.


## Topology of a network architecture


| Layer / Order        | **Firewall Only** | **With IDS**                                  | **With IPS**                   |
| -------------------- | ----------------- | --------------------------------------------- | ------------------------------ |
| 1. Hosts             | Hosts             | Hosts                                         | Hosts                          |
| 2. LAN               | → LAN             | → LAN                                         | → LAN                          |
| 3. Next Component    | → Router          | → Switch                                      | → **IPS**                      |
| 4. Monitoring Device | *(none)*          | IDS (connected to Switch via port mirror/tap) | *(IPS is inline, not passive)* |
| 5. Next Hop          | → Firewall        | → Router                                      | → Router                       |
| 6. Firewall          | → Firewall        | → Firewall                                    | → Firewall                     |
| 7. Modem             | → Modem           | → Modem                                       | → Modem                        |
| 8. Internet          | → Web Service     | → Web Service                                 | → Web Service                  |



## Cloud security

### IAM (Identity and Access Management)

    IAM is a set of processes, policies, and technologies used to manage and control digital identities and user access within an organization’s environment—especially in cloud computing.

### Attack Surface

    Every service of the CSP has certain flaws which increase the attack surface. Increasing of the attack surface means the security measures also should increase.
    Many of the services also creates entry points. These entry points can be used to inject malware.

### 
