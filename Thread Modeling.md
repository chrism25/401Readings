# <p align="center"> Modeling a Web Application
 
Threat modeling is the structured representation of all the information that affects the security of an application.
* Threat modeling applies to many things from software to networks, and it typically includes:
	* Model description
	* Possible future threats
	* Potential system threats
	* Actions to mitigate threats
	* Verification of model, threats and success

* All the information is analyzed, a model is produced and a list of security improvements is created to aid in the design of an application. The steps needed are also contained in the Threat Modeling Manifesto
* Threat modeling aims to improve security by identifying threats and vulnerabilities to implement countermeasures.
* It is best to apply threat modeling through the development of a project, like an ongoing process that gets refined through the lifecycle. Everytime a new technology is chosen, the risk that its implementation can produce, has to be analyzed. This is also recommended after security incidents occur, new features are released and after architectural or infrastructure changes.
* There are 4 questions that are always important to take into account for threat modeling:
	* What are we working on?
	* What can go wrong?
	* What are we going to do about it?
	* Did we do a good job?

* There is a diversity of techniques used to answer these questions and structures models help make the process more efficient. Instead of  focusing on all possible threats, one needs to refine the search to be more efficient, using the last 4 questions can narrow the search. 
* If done right, rational decisions about security can be taken since this provides a clear line of sight. With a clear view, an assurance argument can be made and sustained with evidence and claims.
* A pretty useful modeling approach is the STRIDE framework
	* Spoofing: There are always people or bots trying to impersonate you, every request needs to be authenticated. For example, single Key grants access indefinitely and many APIs use it, tokens are similar but last for a short period, signatures on the other hand uses encryption and requires private keys that use shared secrets. It is always to be careful how you communicate and with whom, also make sure your system is secure against spoofing attacks.
	* Tampering: Authentication is important but can you be sure the data has not been tampered with? Firewalls and partitioned storage are some techniques to protect your data, log files may detect the tampering and the tampering can simply be a distraction to hide someone’s tracks.
	* Repudiation: Attacks will never stop, so implementing auditing correctly can trace these attacks to the vulnerability so it can be resolved. That's why non-repudiation mechanisms need to be implemented, these work sometimes with logs or spoofed accounts to track back to the user. 
	* Information Disclosure: Servers  and systems guarding sensitive data have to be constantly maintained so information doesn’t get leaked accidentally. There are always people looking for chances to overflown buffers or a buggy code that can give them the chance that they were waiting for.
  * Denial of Service:  Actors may overload a system with incoming requests so users can’t connect and these attacks can also be combined giving the actor access to additional resources. It is important to check which areas are susceptible to denial of service like storage or processing.
  * Elevation of Privilege: This area could be the most dangerous since the actor doesn't just get into the system but also expands its access to different resources, and if it gets the highest privileges the actor can tamper with anything in the system. 

