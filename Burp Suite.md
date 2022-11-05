# <p align="center"> Burp Suite


* Burp suite is a suite of tools that complements penetration testing on web applications over HTTP(S). It’s based on a proxy designed to allow the analysis and editing of web traffic, this proxy can intercept web requests/responses and read/edit them before they reach their destination.
* Most of the tools in this suite work along with the main proxy and the suite is available for MacOS, Windows and Linux. Among some of the other tools in the suite we have:
	* Intruder: Which imports requests to configure arrange of payloads to attempt and can then run through them automatically.
  * Repeater: It imports web requests to modify them and see the response side by side in order to allow adjustments to attempt exploits and corroborate exploits.
  * Sequencer: Analyzes the randomness of data, like session IDs, CSRF tokens and password reset tokens. A pool of 100 samples is required for the analysis, identifying weaknesses in how supposedly random values are being generated.
  * Decoder: Allows decodification of strings and encodes them again.
  * Comparer: Compares 2 strings to check for differences
  * There is also an issue tracker that comes at a premium, listing identified issues but that need to be checked for false positives.

* The suite also presents free community-written extensions although some use features of the premium version. A paid version runs at $399 while an enterprise edition has a yearly subscription of $3999, plus $399 per scanning agent that can only be added in batches of 10.

It was very interesting working with ZAP, definitely a great tool that let us analyze many aspects of the WebApplications and their vulnerabilities. The challenge was also interesting since we saw how we were able to grab some headers and even cookies with just a few lines in a python script.
