# Security In OSI

Security architecture In OSI divided into three main parts:

1. `Security Attack`: Any action that compromises the security of information owned by an organization.
2. `Security Services`: A processing or communication service that enhances the security of the data processing systems and the information transfers of an organization. The services are intended to counter security attacks, and they make use of one or more security mechanisms to provide the service.
3. `Security Mechanism`: A process ( or a device incorporating such a process) that is designed to detect, prevent, or recover from a security attack
 
## Security Mechanism

Divide to:

1. Specific Security Mechanism:
incorporated into the appropriate protocol layer to provide some of OSI Security Services :

- `Encipherment`: it is ciphering technique (if we have `plane text` converted to `ciphering text` before sending it cross the internet to prevent the attacker to know what the data is and that makes the data more in this way to achieve from Security Services data or Security confidentiality.) 

some architecture that generates ciphering text :
(تعددي بعض من الخوارزميات التشفير الي اخذتوها اذا بدك)

- `Data Integrity`: checking the sender and receiver parts before and after data is received, in this way they always check that the right data reach the right destination.

- `Authentication exchange`: this mechanism to check from the sender and the reserve by exchanging pieces of data like `two-way handshaking mechanism` to check that still the authorized node.

- `Digital Signature`: having a Signature (a piece of code that insert into the message) to prove the identity of the sender, in the way to achieve from Security Services the authentication and data integrity.

- `Access control`: given access right to resource depend on user privilege )(all users have their own access right to part of resource).

- `traffic padding`: having dummy data to confuse the third part but this data haven't any impact on the receiver.
- `Routing control`: when users send data in the network they also specify the route that should take in order to reach the destination.
- `notarization`: deploy a trusted third party that gives us the above to reach the destination. 
Example: SSL layer HTTP`s`)in secure servers. 



2. pervasive Security Mechanism:
this is Security Mechanism that is not related to Specific layer, it is a general Mechanism :

- `Trusted Functionality`: process perceived to be correct with respect to some criteria 
// like: established by a security policy.
- `Security Label`: marking of a Security attribute to a resource to identify that we go on the right process. 
- `Event Detection`: when every action is created in the system event is created to check the process.
- `Security Audit Trail`: review the system record and activity that is carried out in order to ensure that the activity is accepted or suspicious or attacked. 
- `Security Recovery`: to Recovery the system after the attack damage is done. 

## resources

- [Security In OSI (Youtube)](https://www.youtube.com/watch?v=MnQ0EmDj68A)
- [generale information OSI Reference Model (youtube)](https://www.youtube.com/watch?v=9zqHMl9_s5k)
// - [generale information OSI Reference Model (youtube)](https://www.youtube.com/watch?v=H5ifNVeDXkg)
- [Specific Security Mechanism (geeksforgeeks)](https://www.geeksforgeeks.org/types-of-security-mechanism/)
- [prevasive Security Mechanism (tutorialspoint)](https://www.tutorialspoint.com/what-are-the-pervasive-security-mechanisms-in-information-security)


