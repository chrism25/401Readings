# <p align="center"> Virtual Private Cloud

* A good subject to know more of since VPC is a great tool that makes sense to implement on every organization.
* A VPC provides enterprises with their own private cloud environments on shared public cloud infrastructure. This logically isolated environment becomes a control, secure place on the public cloud.
* These VPCs are created with virtual network functions and security security features, providing enterprises with full control over them. They provide private cloud benefits while leveraging public cloud resources and savings.

Features:
* Agility: To control the size of the network and deploy resources when needed. These resources can also be scaled in real time.
* Availability: To produce redundancy on resources and highly fault-tolerant availability zone architectures so workloads and applications are highly available.
* Security: Full control over how resources and workloads are accessed and by whom, even isolating them from the cloud’s provider.
* Affordability: It helps save on hardware cost and labor times among others.

Benefits:
* Flexible business growth: Cloud infrastructure can be deployed dynamically, easier to implement changes,
* Satisfied customers: Being already in the cloud speeds the process of receiving and sending data. VPC environments are highly available, making them reliable and increasing trust.
* Reduced risk across the entire data lifecycle: Superior levels of security at the instance and subnet level, providing peace of mind.
* More resources to channel toward business innovation: Savings on cost and fewer demands on the internal IT team, so one can focus on the business.

Architecture:
* Compute: Virtual Servers Instances or VS are presented as vCPU with pre-set parameters.
* Storage: The pre-set amount of storage can be easily upgraded if needed.
* Networking: Networking functions can be virtually deployed to the private cloud to provide or restrict access to its resources. 
> * There are public gateways present so some areas or all can be made public to the internet. 
> * Load balancers that distribute traffic across multiple VSIs to maximize performance and  availability.
> * Routers that direct traffic and allow communication between network segments.
> * Links, either dedicated or direct that enable fast and secure communications among on premises  enterprises IT environments or PC and the VPC resources on the public cloud

 Three-tier architecture in a VPC
* The web or presentation tier takes requests from web browsers and presents the information to the user
* The application tier, where most processing takes place and contains the business logic
* The database tier which contains database servers.
* Each tier must have its own subnet, each layer automatically assigned its own unique ACL

Security
* VPCs are highly secure because they replicate security features from traditional data centers. Customers can define virtual networks in logically isolated parts of the public cloud, controlling the access of IPs to resources.
* Access control lists (ACLs): List of rules to limit who access particular subnets. The ACL mandates who access these subdivisions of the VPC.
* Security group: Groups that act like virtual firewalls controlling the traffic to the virtual servers. Resources can be placed in these groups with rules to design who access them.

VPC and …
* Virtual Private Network: The VPNs  are secure ways to connect using encrypted tunnels, deploying it as a service can establish secure communication within subnets on VPC and between it and your physical location.
* Private Cloud: Is a single cloud environment owned, commonly hosted on premises, while VPC hosts multiple users but all logically separated.
* Public Cloud: Customers create a virtual private cloud inside the public cloud, but VPC provides more security at the price of a public cloud, they are both scalable but one is most cost efficient and secure.

* Among all the providers for VPCs, it is important to take into account the business requirements to select the right one, since the features and offerings may affect the price on some of them. There are some that also have features to ease the integration with one’s existing applications and toolsets.
