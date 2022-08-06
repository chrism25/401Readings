# <p align="center"> Cloud Security Principles and Frameworks
* Service providers can offer different features and services depending on the customer needs and these features vary depending on the level of abstraction. 
* The same way providers have the responsibility to give a service and support, users have the duty to know how to use these services and do the parts that the provider doesn’t cover. Some providers give the option for extra features to make the user’s life easier at a premium and even give support to users so they can succeed and keep using the services.
* AWS for example offers lightsails, EC2s  and containers, while lightsai is a new version that takes care of almost everything, EC2 is the 1st abstraction that manages hardware and hypervisor. On the other hand, containers are self-contained environments that provide the user with everything needed to run different applications with different software dependencies.
* These containers are divided into the control panel (API and interfaces) and the data plane (CPU, network, memory, storage). However, new versions have been released like EKS, which liberates the user from having to manage the control panel and Lambda, which basically takes care of everything, the user only has to run the desired function. 
* Additionally, AWS has been gracious enough to listen and provides additional options for different users like Bare metal that has almost no abstraction, giving the user more responsibilities but also flexibility at the same time and Fargate, which will heavily put the responsibility on the provider since it also has to manage the data plane.

![Abstraction8-1024x575](https://user-images.githubusercontent.com/97658998/177693205-f17323e2-75ad-44f0-a30e-cf83d891e49b.png)
***
Definitely a good read to better understand the abstraction of services and the responsibilities that lie on providers and users when entering into an agreement. 
