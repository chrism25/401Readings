# <p align="center"> Threat Hunting

* This is an active/proactive activity, in which threat hunters look into the internal systems for indicators of compromise, like a command and control channel with some external system. One doesn’t wait for alerts to be triggered but analyze the behavior.
* In order to give a report with certainty that the network is in a current safe state, threat hunters constantly go and scan for abnormal behavior and threat indicators.
* Current tools either help us protect our system(protection based) or expel actors from our network(response based), the issue is realizing the defenses have failed and that it is time to go into the response state. 
* The typical approach is to analyze the logs in order to detect the breach. Sadly, the average response time to detect a breach this way is more than 6 months, and most of the times these breaches are even caught by 3rd parties like fraud detection, making relying on log analysis obsolete.
* Because of these reasons Threat Hunters use tools to analyze the networks. AC-Hunter for example is a tool that analyzes the network and reports on abnormal behavior and threats, some of these alerts might be mild or not important but they add up to a score and let the user see an abnormal change is the score that can indicate an intruder trying to access the network.
* The tool also gives us all details about communications with our system, IPs, DNS. An important aspect is analysis on DNS, because DNS is normally open and subdomains are used to communicate outside. An actor will create several subdomains to create control over DNS take out and this is one just of the many tools that are out there and provide a better approach than simply analyzing the logs.

  ![Screenshot (27)](https://user-images.githubusercontent.com/97658998/196516197-dee07271-f88f-4a99-bf99-387d81c646d9.png)
