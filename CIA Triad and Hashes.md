The CIA triad are the 3 principles that establish a secure system

#### Confidentiality
* The restricted access of information to not authorize parties. Sadly the internet is as useful as it is risky since there are always actors lurking around, hacking a server or a man-in-the-middle- attack are common ways to obtain certain information. Many times this data is precious, for example:
  * A company has vital pieces of information that the competition shouldn’t know, like customers, salaries, etc.
  * A law firm wants to preserve attorney-client privileges.
  * A healthcare organization wants to secure ePHI for HIPAA requirements.
* In order to achieve confidentiality one of the most obvious solutions is encryption, and there are 2 types of encryptions. Data-at-rest encryption and data-in-transit encryption, both are called end-to-end encryption.
* However, both are necessary to ensure its confidentiality since the data can be in danger when in transit or at the servers as well. 
* For data in transit a good approach will be SSL or SSH, for data at rest OpenPGP or a file-level encryption should do the job. 
* Two factor Authentication would be another way to acquire confidentiality, since this will restrict access to unauthorized people. Regular authentication would also be useful, but multifactor authentication would do a better job.

#### Integrity
* It is similar to Confidentiality, but in this case the goal lies in preserving the data intact. Many times altering data in a certain way can be more dangerous than simply taking it away, tampering with data like financial figures whether intentionally or unintentionally may end in catastrophes. 
* Without proper precautions this data can also be affected by hacking a server or a man-in-the- middle-attack.
*  Data needs to travel from one point to another and this is probably when it is at its most vulnerable. Therefore, to preserve its integrity hash functions and digital signatures can be implemented, these are security elements that are already available on transfer protocols.
* It is important to remark that these solutions are not preventive but they will help determine if the integrity of the data has been compromised.

#### Availability
* This principle is as important as the others since the data can be impeccably safeguarded but if it is not available when needed, this becomes a big problem. This precious data can even be rendered obsolete in some cases when data is time sensitive or if it is part of a supply chain. 
This data can become unavailable by factors like network disruptions, DDoS attacks, or natural disasters among others.
* Data is nothing if it can’t be used, so in order to ensure its availability a High Availability Cluster is recommended, and there are 2 ways to achieve this set up.
* An active-passive high availability configuration would be setting up at least one failover server that will immediately take over for the main server.
* An active-active high availability configuration on the other hand will have 2 or more servers working together all the time so the workload is shared and the chances of 1 going down are significantly reduced.

#### CIA Triad in One
* Now the desired goal would be to come up with a way to implement all the aspects of the CIA triad, normally this would require 3 different solutions that we could put to work together, but this is not an easy task since it requires time and deep knowledge.
* Luckily, there are file transfer managers that incorporate all 3 aspects in one solution, JSCAPE MFT Server for example. This implements end-to-end encryption, 2-factor authentication, data integrity, high availability configurations and data loss prevention(DLP).
-----------------------------------------------
 * Hashes are strings that are present on downloads and help verify the data is not corrupted or tampered with. They are produced by cryptographic algorithms and always have the same size despite the size of the data.
* A good way to confirm a file is not corrupted is to run a hash function(SHA-256 is recommended) against the file and compare them with the one the creator has for the file, since even a small change will drastically affect the hash value.
* Using these elements is fairly easy and the tools are already in the system.

Windows
* Open Powershell and run “Get-FileHash C:\path\to\file.iso” replacing the path for the one for the file. By default it will use SHA-256 but a different hashing element can be specified if desired. At this point all that is left is to compare it to the original hash.

MAC
* Go to “Finder>applications>utilities>terminal” just as before we run the command “shasum -a 256 /path/to/file” changing the path and a different hash can be selected as well. 

Linux
* Here we also go to the terminal and run “sha256sum /path/to/file” same concept as the others.

* These should give you a piece of mind but to go a step further we can imagine that the creator website was hacked modifying the hashes, or a man in the middle attack was deployed modifying the website in transit.
* For this case Linux came with the solution to cryptographically sign the hashes, so one just has to look for the signature to ensure the file wasn’t tampered with.
