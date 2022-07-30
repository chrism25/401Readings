# <p align="center"> Public Key Infrastructure

* This is definitely a good topic to know more about since these are main factors that happened behind the curtains but are really important so one can surf the web with some peace of mind.
* This is a kind of technology that allows users and devices to authenticate themselves through a key. Basically anything can be associated with a key, a trusted party has to sign a document so the entity and the key can be linked, the document is called a certificate and the party that signs them, a certificate authority(CA), which also has a key that is used to sign the certificates.
* The basic concept is that each entity has a private key to sign certificates and nobody knows the key, from this key a public key is derived. This public key only verifies signatures, is available to anyone and normally is present on certificates.
* There are numerous CA and devices normally trust them by default. Usually the standard certificate format is called X.509v3 and it is maintained as RFC 3280.
* Public Keys are commonly used on secure socket layers(SSL) certificates, this is a security protocol used when navigating to “https” addresses. However, nowadays most websites use a new version called Transport Layer Security(TLS)
* These certificates ensure a secure connection to prevent someone from sniffing the connection, like a “man in the middle attack” 
* The secure Shell protocol supports certificates to authenticate hosts and users. OpensSSH uses its own certificates and Tectia SSH the standard X.509
* Additionally, certificates are also used to secure emails. Using the X.509 certificate, S/MIME specifies a message format for signed and encrypted messaging.
* Even though certificates seem secured, sadly there may be cases in which CA may be coerced to create certificates to vouch for parties. Also, intelligence agencies may use fraudulent certificates in many ways, so one should be careful when trusting public CA. In addition, some organizations have their own PKI and CA so no other CA will check on them.
*  SSHs have been playing a big role on PKIs, writing documents for protocols, selling SSH certifier, working on X.509 and proposing a simple public key infrastructure(SPKI) to address some of its trust issues. It also used customizable policy rules for choosing CA, brought support for CAs and registration authorities.
