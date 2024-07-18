# Understanding-IDS-and-Snort
</p> This section will cover how intrusion detection systems work and how they are typically deployed. I will also cover Snort IDS/IPS by explaining how Snort works and outlines the structure of a Snort rule </p>
</p> - Intrusion detection is the process of actively discovering threats/attacks/intrusions on a network hosts, services. </p>
</p> - There are two types of intrusion detection solutions, a host based IDS is a setup on an individual host on a network and a network IDS is placed within a network to monitor traffic to and from all parts of a network. </p>
</p> - An IDS is a system/host planted within a network to capture traffic and identify malicious activity based on predefined rules, after which, the malicious activity is logged, and a notification is sent to the relevant parties informing them of an intrusion. </p>
</p> - IDS's are typically coupled with the functionality to also perform intrusion prevention, whereby specific rules are set to drop packets that are malicious or intrusive. </p>
</p> Snort is a free, open sourse IDS/IPS system that is used to perform traffic/protocol analysis, content matching and can be used to detect and prevent various attacks based on predefined rules. It has three operational modes. When snort works as an IPS, you want to place it between the router and the switch. When snort works as an IDS, it is implemented into the switch .   </p>
</p>Packet sniffing: collects and displays network traffic like what Wireshark does.
</p>Packet logging: collects and logs network traffic into a file. 
</p>Network intrusion detection: analyzes packets and matches traffic against signatures. </p> 
</p> When active, Snort captures packetss, reassembles them, analyzes them, and determines whaat needs to be done to the packet based on predefined rules. </p>
</p> Snort rules are very similar to a typical firewall rule, whereby, they are used to match network activity against specific patterns or signatures and consequently make a decision as to whether to send an alert or drop the traffic. Snort has a large amount of rule-sets created by the community that are very useful to begin with. </p>
</p> There are currently two versions of Snort: Snort 2.X: de facto version, most widely implemented, and has extensive support, documention and rule-sets Snort 3.0: latest version that provides improved efficiency, performance, scalability, and usability over Snort 2.0 </p>
</p> Snort has three different types of rule-sets: 
</p> Community rules: free rule sets created by the Snort community
</p> Registered rules: free rule-sets created by Talos. In order to use them, you need to register an account. 
</p> Subscription only rules: these rule sets require an active paid subscription in order to be accessed and used.
</p> OR we can create our own rules based on requirements. 
</p> Snort rule syntax: </p>
<img width="896" alt="Screenshot 2024-07-18 at 4 57 07 PM" src="https://github.com/user-attachments/assets/88186c94-da54-4c55-af5e-d66a4ad490bb">
</p> How snort works: Incoming network traffic is captured by the snort server through sniffing. It then goes through a preprocessor and into the snort plugin and packet decoding. Then it goes through the classification of packets through ML. In the event a signature is matched, the alarm loggin process is implemented where it is either logged, or an alert is sent </p>
<img width="892" alt="Screenshot 2024-07-18 at 5 21 57 PM" src="https://github.com/user-attachments/assets/dc6bd417-bc87-4a67-bd6a-897d48cc454a">
