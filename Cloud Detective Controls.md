# <p align="center"> Amazon GuardDuty

* An useful tool to gather logs from different AWS services and place them together in one place for easy monitoring, with only one click. It doesn’t require installing anything and has no impact on the systems running.
* This service that Amazon provides, uses threat intelligence feeds like malicious IPs and domains, also machine learning to identify malicious or unusual activities within the AWS environment. It recollects and monitor data from many sources like CloudTrail, DNS, EBS, EKS audit and VPC flow logs.
* A really good aspect of this service is that one doesn’t need to enable any of the other services, since GuardDuty will independently collect the logs from them, this will save money and setup time on large organizations.
* One master account can be set, so it can monitor the findings from the whole organization in case there are accounts in different regions.
* The service basically streams the data, does not store it, unless it detects unusual activity in which case it produces security findings to inform the status of the AWS environment. some of these findings can be:
  * Escalation of privileges
  * Communication with malicious IPs
  * Presence of malware
  * Unauthorize infrastructure deployment
  * Unusual API calls, among others

*  This service can be accessed through the browser, it provides software development kits(SDK) that contain libraries and sample codes for different programming languages and platforms. The kit lets you use HTTPS API to create programmatically access to AWS, issuing requests directly to the service.
