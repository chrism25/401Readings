# <p align="center"> AWS CloudWatch

* Nowadays the cloud is being used massively and not just for resources but also to handle entire companies. So it is imperative to have some knowledge about the subject, since as time progresses, these services are simply going to expand and most businesses will migrate at least up to some degree.
* CloudWatch is a wonderful tool that constantly monitors all AWS resources in addition to on-prem resources, creates logs, sets alarms and it helps with automation. Some of these metrics are:
> * Instance Metrics
> * CPU Credit Metrics
> * Amazon EBS Metrics for Nitro-based Instances
> * Status Check Metrics
> * Amazon EC2 Metric Dimensions
> * Amazon EC2 Usage Metrics
  
* Any of these metrics can be used to create dashboards, even custom metrics.
* CloudWatch can collect near real-time streams of events that can trigger alarms like SMS or services like Step function, Lambda. Some of these events can be the status of an EC2, auto-scale, and by creating custom rules AWS services can be automated.
 * The events are represented in a JSON script. These events can be generated when AWS resources change their state; API calls and console sign-ins; when the code generates application-level events and publish them; and can be issued on a scheduled basis.
* The rules match incoming events and route to 1 or more targets for processing.
* The targets process events and are specified within the rules.
* CloudWatch Agent can send custom metrics to CloudWatch from different OS like Linux, windows, debian, among others. This agent can also be installed on-premises, specifying the credentials of the IAM user created for CloudWatch.
* A CloudWatch alarm can be triggered by the metrics or the result of a math expression based on the metrics, executing the action(s) based on the set conditions. These actions can be services or alarms.
*  The CloudWatch Logs centralized all logs from all systems for easy access and is scalable. These near real time logs can be filtered for specific values or phrases, facilitating the troubleshooting of systems and applications; these logs can also be delivered to other services with a subscription. These logs can also trigger alarms and be stored in S3 buckets so 3rd parties can review if needed, like for audits and analysis.
* By enabling Anomaly Detection, CloudWatch will use matching learning algorithms that will determine normal baselines and surface inconsistencies with minimal user involvement. Once the expected behavior is learned, an anomaly detection band is generated based on an upper and lower band model. Values out of this predicted band are considered anomalies  and will trigger an alarm once it is set up.
