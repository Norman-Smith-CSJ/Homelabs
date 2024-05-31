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