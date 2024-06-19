# Homelabs
A place to show what I'm cooking up in my homelabs!

# 5/29/2024 Update - At this time I'm currently working on building an Elastic Siem following a video by I.T. Security Labs. This lab will serve as a way to monitor my home network while also attacking a VM to see what those logs look like in real time. This lab will be hosted on my server which houses all my virtual machines.


https://www.youtube.com/watch?v=tD5fRwHRygY&ab_channel=I.TSecurityLabs This is the initial setup

Following this series here https://www.youtube.com/watch?v=-tMY9GVvvsM&list=PLyJqGMYm0vnOxMapUGkt9DfU4aTTU2vqU&ab_channel=I.TSecurityLabs


Following this gitlab guide

https://gitlab.com/kalilinux/kali-purple/documentation/-/blob/main/301_kali-purple/installation.txt#L37

https://www.youtube.com/watch?v=Zafi0laDQFk&ab_channel=BitsByteHard 

reference the above link if you need further understanding of this process


When you get to the step about setting up HTTPS make sure you hit enter through all the prompts and key the default names for the ca and keys. After adding those to your kibana.yml you need to restart the kibana service for HTTPS to take effect - fun fact this took me hours of troubleshooting to figure out.

# 6/1/2024 12:24AM Update - Fun times - finally was able to get monitoring setup for the elastic SIEM. I'll upload my progress tomorrow and begin the next step of the guide.

Successfully setting up Https on elastic

![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BIn%20Progress%5D%20Elastic%20SIEM/images/Success.png)

Attempting Reverse Shell

![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BIn%20Progress%5D%20Elastic%20SIEM/images/Attempting_Reverse_Shell.png)

![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BIn%20Progress%5D%20Elastic%20SIEM/images/Hosting_Reverse_Shell.png)

Alerts Firing

![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BIn%20Progress%5D%20Elastic%20SIEM/images/Alerts_Firing.png)



# 6/8/2024 Update - I was able to successfully get my opnSENSE firewall to communicate with my kali purple machine that hosts the elastic SIEM. This proved especially difficult due to the fact that creating a bridge network in esxi client host isn't as simple as toggling bridged network within the network settings when spinning up a new VM. Nonetheless we were able to get them to communicate and move on to the next step.

OPNsense and Kali Purple hosting elastic communicating

![image](https://github.com/Norman-Smith-CSJ/Homelabs/blob/main/%5BIn%20Progress%5D%20Elastic%20SIEM/images/OPNsense_and_kali.png)



# 6/19/2024 Update - Wow what a doozy this was. I'll admit this is mostly due to my own fault but I ran into a few issues when moving onto the suricata IDS portion of the lab. Due to recent updates with filebeat you have to ensure if your using this walkthrough you utilzie filebeat7 and NOT filebeat8. I had to uninstall and remove everything that filebeat8 put on my OPNsense firewall and do a make install with filebeat7. Once this was completed everything worked the way it needed to. I had to restart the OPNsense firewall multiple times for changes to take effect but in the end I was able to do the following: 

# OPNsense firewall installed filebeat / suricata

# Set up downloads / rules on OPNsense and was able to see alerts.

# Conducted an nmap scan against the firewall to determine if my activity was being caught by the firewall.

# Reviewed in the OPNsense web application the alerts coming in from the nmap scan.

# verified the alerts were being forwarded from OPNsense to elastic siem by reviewing the discover tab.

# Viewed the data with a filebeat / suricata dashboard

