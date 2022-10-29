# <p align="center"> XSS
Cross-site scripting (XSS) is a vulnerability that allows the actor to masquerade as the user, so it can have access to the user’s data and can interact with the vulnerable application, which can end up giving the actor full control over the application.

### Functionality
* In the presence of a vulnerable server, an actor manipulates the server so it returns a malicious JavaScript to users. Once the code is executed inside the user’s browser, the interaction between the user and the app gets compromised.

### XSS proof of concept
* A way to recognize a vulnerable application is by injecting a payload in the browser and see if it executes some arbitrary Javascript.
* The “alert()” function it’s commonly used for this purpose since it is easy to spot and not really harmful. However, chrome doesn’t allow it anymore since it is highly used, instead “print()” can be used and a “PoC” payload might be better suited.

### Types of XSS attacks
* Reflected XSS: This is the simplest type in which the malicious script is sent in an HTTP request and the data gets included in the immediate response in an unsafe way. Once a user visits the URL constructed by the attacker, the script gets executed in the browser, it can carry out any action and retrieve any data that the user has access to.
* Stored XSS: This is a second order XSS or persistence type, the application receives the data and includes that data in later HTTP responses in an unsafe way. The difference is that the data submitted can be through HTTP requests, emails over SMTP, marketing applications or network monitoring applications among others.
* DOM-based XSS: Also known as DOM XSS, in this type the application contains some client-side JavaScript that processes data in an unsafe way, usually writing it back to the DOM. 

### Uses
* Carry out actions impersonating the user.
* Capture the user’s login credentials.
* Impersonate the user .
* Read data that the user has access to.
* Virtual defacement of the website.
* Trojan functionality injection into the website.

### Impact
* If it is a brochure application with anonymous users and public information, normally the impact will be minimal.
* If the application has sensitive private data, the impact will be high.
* If the compromised user has elevated privileges within the application, the impact will be critical since the actor has full control of the app.

### How to find and test for XSS vulnerabilities
* Manually testing requires submitting a simple unique input into every entry point in the application, identifying where the input is returned in HTTP responses and testing each location to see if suitable crafted input can be used to execute arbitrary JavaScript. This will reveal the XSS context to determine the suitable payload.
* However, to test for DOM-based XSS, one places a simple unique input in the parameter using the browser’s developer tools to search the DOM for this input and testing the locations to see if they are exploitable. This works for most cases but some DOM XSS are harder to detect, non-URL-based inputs and non-HTML-based sinks, required to review the JavaScript code.
* Luckily, there are tools like Burp Suite’s Web Vulnerability Scanner that are reliable and quick to find vulnerabilities, combining dynamic and static analysis of Javascript.
----
* Content Security Policy(CSP): Is a browser mechanism that prevents the exploitation of vulnerabilities based on behavior analysis. CSP can be circumvented to enable exploitation of underlying vulnerabilities.
* Dangling Markup Injection: Is a technique that captures data cross-domain when a full cross-site scripting is not possible due to input filters or other defenses.

### How to prevent XSS attacks
Most likely this can be achieve by combining some of the following methods
* Filter Input on arrival: Filters for the input received by the user should be very strict based on valid and expected input.
* Encode data on output: Output in HTTP responses should be encoded, this might require HTML, URL, Javascript and CSS encoding.
* Appropriate response headers: Content-Type and X-Content-Type-Options headers should be used to ensure browsers present responses in the way they are intended.
* Content Security Policy: This will work as the last resource to reduce the severity of vulnerabilities that might still happen.
--------
* This is an important subject since XSS vulnerabilities are very common.
* CSFR and SQL are similar vulnerabilities but CSFR induces the victim to perform unwanted actions while SQL is server-side and targets the database.
* Whitelists helps to filter for allowed characters, and Htmlentities, Ent_quotes, Google Guava and JavaScript Unicode escapes help with the output.
