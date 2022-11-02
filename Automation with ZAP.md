# <p align="center"> Automated AppSec With ZAP

* Zep Attack Proxy is a free open-source penetration tool specifically designed to test web applications.
* It uses a man in the middle approach, standing between the tester’s browser and the web application to intercept and compromise the interaction. If a corporate network is using a proxy, then ZAP is deployed to connect to it. 
* A great quality of ZAP is that it can be implemented by users ranging from testers new in the field to developers. Its functionality will vary depending on the user and it works on major OSs and Docker.
* Additionally, ZAP is open source so the community can provide improvements and examine the code being used. 

### Install and Configuration
* ZAP needs to be installed and requires Java 11+ to work. Once installed, the persistence option is presented and sessions are always recorded to disk in a HSQLDB database, if persistence is not selected this sessions are deleted once ZAP is exited.

### ZAP Desktop UI
* In the Desktop one can find 
	* Menu Bar: For automated and tools manuals
	* Toolbar: For easy access to commonly used features
	* Tree window: Displays tree and scripts Window
	* Workspace Window: Displays request, responses and scripts, all of them editable
* Information Window: Details of automated and manual tools
* Footer: Summary of alerts and status of main automated tools
### Automated Scan
* The quick scan using ZAP is as simple as going to the tab “Quick Start>Automated Scan> Input URL>Attack”. ZAP will scan each page, then attack each of their functionality and parameters. 
* ZAP crawls the web Application with 2 types of spiders. The traditional one is fast but not always effective when dealing with AJAX web applications that generate links using JavaScript, it reveals links by examining HTML. 
* However, ZAP’s AJAX spider works better in these situations since it invokes  browsers which then follow the links that have been generated. This type is slower and requires to be configured if going in a hadless environment.
* In a regular search ZAP is safe, works passively and in the background. On the other hand, an active scan, attacks targets and can put them at risk. Depending on the investigation and permissions, one should decide the type of scan.

### Results
* As ZAP works its way through, a map of the web application and its resources is constructed. It also records requests and responses sent to each page, creating alerts for possible problems on these requests and responses.
* The examined pages can be found at the “Sites” tab in the tree window, and nodes there are expandable to access the URLs.
* In addition, alerts are categorized by levels under the “Alerts” tab in the information window; these alerts will display the URL and vulnerability detected. 
* There is a “Response” Tab in the Workspace that contains the header, body and part of the response that generates the alert.

### Manual Exploration
* The automated scans mentioned above are great but they should be combined with manual exploration, for greater results and to avoid limitations like access to protected login pages unless the authentication function in ZAP has been configured, or be able to handle errors that may arise.
*  It is fundamental to be thorough with all pages of the web application since hidden pages may go live and security by obscurity is not recommended here.
* By selecting “Manual Scan” instead of the Automated one, ZAP will launch any of the most common browsers being installed in the new profile. Already existing browsers in different profiles need to be added by configuring the browser to proxy via ZAP, and import and trust the ZAP root CA. 
* By default ZAP goes on “Heads Up Display” (unless unselected), allowing pen testers to focus on functionality while providing key security information and functionality.

### Advance features
* Extra features can be found and added for regular use by right clicking on them under the “+” tab.
*  Additionally, new free functionalities can be added through an online marketplace in the “Manage Add-ons” toolbar.
* Automation supports many options like:
	* Docker Packaged Scans
	* Github Actions
	* Automation Framework
	* API and Daemon mode

* Remember that ZAP is a pentesting tool that simulates a real attack, so be careful when using it because it can cause harm. If not sure, it is better to use it in safe mode available in the toolbar.
