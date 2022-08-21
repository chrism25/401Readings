# <p align="center"> Cloud Identity and Access Management (IAM) with AWS

* Now days that everything is going remote it is important to understand the shared responsibility and all the preparation that this involve in order to prevent catastrophes 
* Capital one suffered a catastrophic breach that affected millions of customers but could have been prevented by a single product or set of professional services. 
* The problem was a misconfiguration at the application layer of the firewall, which was exacerbated by unintended broader permissions. 
* The actor “Erratic” discovered a misconfigured WAF which allowed him to access the instance, using server-side request forgery(SSRF). He used a command to return a role to obtain temporary security credentials for elevated role access. Once there he listed all S3 buckets using an IAM role and proceeded to download the files that the elevated credentials gave him access to.
* The problem here was the flawn design that exposed the S3 buckets to anyone with an IAM role. The poorly configured WAF wasn’t a challenge for an EC2 with an excessive IAM role. It is important to follow governance practices like:
> * Review all access path and permission (human o not) to data storage. Use Cloud Infrastructure Entitlement Management solutions to automate the detection of over-privileged identities and over-exposed data.
> * Automate policies, providing security and compliance views across all AWS (version 1 and 2)
> * Use CloudTrail, CloudWatch, and/or AWS lambda services to review and automate specific actions taken on S3 resources.
> * Ensure each application, EC2 instance, or autoscaling group has its own IAM role, unrelated applications should not share roles.
> * Ensure roles only have permissions to enable access just to required AWS resources. This wasn’t the case in this incident.
> * Include a “Condition” statement inside the IAM role to investiagte the access to known IPs or VPC endpoints.
> * Instances should not have IAM roles that permit attaching or replacing role policies in any
production environment.
> * Get rid of unused cloud resources from prior production debugging efforts.

* AWS also has configurations that can prevent these attacks:
> *  AWS IAM: Enforce least privileged IAM controls and make sure IAM policies are attached only to groups or roles
> * AWS S3: Ensure AWS S3 buckets don’t allow public READ, READ_ACP, WRITE_ACP  access, nor FULL_CONTROL access to AWS authenticated users via S3 ACLs. These buckets must have limited access only to specific IPs, must have policies to require server-side and in transit encryption for all objects stored and users authenticated through S3 ACL must not have READ access, FULL_CONTROL.
> * AWS Networking: Ensure no security groups allow ingress from 0.0.0.0/0 to port 22, port 22 (SSH), port 3389 (RDP) and that Application Load Balancer with administrative service (SSH-TCP:22) is not exposed to the public internet. 
> * AWS - Audit and Logging: Make sure S3 bucket access logging is enabled on the CloudTrail S3 bucket, buckets used to store CloudTrail logs are not publicly accessible. CloudTrail should be enabled in all regions, integrated with CloudWatch Logs and there must be a log metric filter and alarm for CloudTrail configuration changes.

* Ideally these configurations should be part of a IaC automation within DevOps pipelines. This way misconfigurations won’t get into production and a management solution could validate their security posture in pre-production and production environments continuously. Additionally, an integrated policy-driven framework that auto-remediate resources that deviate from the defined security policies would remediate misconfigured resources and IAM permissions.

* With the massive shift to remote workers, it is important to take a moment to understand the shared responsibility model, and be prepared to carefully adjust the cloud environments, implement adequate cloud security, IAM controls and compliance assurance.
