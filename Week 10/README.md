
# Weeks 10 & 11: Honeypot
Time spent: 10 hours

A honeypot is a decoy application, server, or other networked resource that intentionally exposes insecure features which, when exploited by an attacker, will reveal information about the methods, tools, and possibly even the identity of that attacker. 


    The setup:
        - Create a google cloud account 
        - Download and install GCP SDK
        - Create MHN in VM, allow http and ports open
        - Install the MHN admin application
        - Install the Honeypot application and deploy it
        
    Which Honeypot(s) were deployed:
     - Dionaea
     - Cowrie
    Any issues you encountered:
    Authentication issues can occur if more than one google cloud console is open. 
    In order to avoid this issue multiple accounts or projects should not be open at the same time.
    
  ![](https://github.com/lcano8/Codepath/blob/master/Week%2010/Honeypot%20.gif)
  
     
    
A summary of the data collected: number of attacks, number of malware samples, etc.
    
Total Attacks: 9,461
   
    - Dionaea: 8,143
    - Cowrie: 941
    
TOP 5 Attacker IPs:

    172.117.74.154 (2,522 attacks)
    111.77.115.34 (560 attacks)
    14.188.58.231 (459 attacks)
    117.102.101.231 (284 attacks)
    122.115.37.12 (204 attacks)
    
    
TOP 5 Attacked ports:

    8088 (1,463 times)
    445 (1,214 times)
    22 (955 times)
    80 (903 times)
    110 (612 times)



