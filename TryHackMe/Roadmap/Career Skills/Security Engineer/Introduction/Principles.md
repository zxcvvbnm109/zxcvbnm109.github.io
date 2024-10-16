###### Task 2

```
Q: Click on "View Site" and answer the five questions. What is the flag that you obtained at the end?

A: THM{CIA_TRIAD}
```

Going beyond the CIA triad we have:
- authenticity - Not fraudulent. Ensures that the data is from the claimed source.
- nonrepudiation- Repudiation means refusing to recognize the validity of something. Nonrepudiation ensures, that the original source cannot deny they are the source of data.

###### Task 3

The opposite of CIA triad is DAD:
- disclosure - opposite of confidentiality
- alteration- opposite of integrity
- destruction / denial - opposite of availability

```
Q: The attacker managed to gain access to customer records and dumped them online. What is this attack?

A: Disclosure
```

```
Q: A group of attackers were able to locate both the main and the backup power supply systems and switch them off. As a result, the whole network was shut down. What is this attack?

A: Destruction / Denial
```

###### Task 4

You could implement these security functions by using security models such as:
- Bell-LaPadula Model
- The Biba Integrity Model
- The Clark-Wilson Model

1. **Bell-LaPadula Model**
Aims to achieve confidentiality with these 3 rules:
- Simple Security Property - aka "no read up" - a subject at lower security level cannot read at higher levels. This prevents access to sensitive information above the authorized level.
- Star Security Property - aka "no write down" - subject at higher security level cannot write at lower levels. This prevents disclosure of sensitive data to a lower security level.
- Discretionary-Security Property - uses an access matrix to allow read / write operations, such as the one below:

| Subject   | Object A     | Object B  |
| --------- | ------------ | --------- |
| Subject 1 | Write        | No access |
| Subject 2 | Read / Write | Read      |

First 2 rules may be summarized as "write up, read down". You can share information with higher levels, but only read from lower levels. This model may not work for file-sharing.

2. **The Biba Model**
Aims to achieve integrity by specifying these rules:
- Simple Integrity Property - aka "no read down" - higher integrity subject should not read from lower integrity object 
- Start Integrity Property - aka "no write up" - lower integrity subject should not write to higher integrity object

These 2 can be summarized as "read up, write down". This model does not handle internal (insider) threats.

3. The Clark-Wilson Model
This one aims to achieve integrity by using following concepts:
- Constrained Data Item (CDI) - refers to the data type whose integrity we want to improve
- Unconstrained Data Item (UDI) - refers to all data types beyond CDI, such as user system input
- Transformation Procedures (TPs) - these procedures are programmed operations, such as read / write, and should maintain integrity of CDIs
- Integrity Verification Procedures (IVPs) - check and ensure validity of CDIs

More models:
- Brewer and Nash Model
- Goguen-Meseguer Mode
- Sutherland Model
- Graham-Denning Mode
- Harrison-Ruzzo-Ullman Model


```
Q: Click on "View Site" and answer the four questions. What is the flag that you obtained at the end?

A: THM{SECURITY_MODELS}
```

###### Task 6

ISO/IEC 19249 lists 5 architectural principles:
- Domain Separation - every set of components is grouped as single entity, each entity will have its own domain with attributes
- Layering - structured system allows to impose security policies
- Encapsulation - prevent direct manipulation with API
- Redundancy - if one power supply fails, the other take the charge
- Virtualization - sharing single set of hardware among multiple systems as well as secure detonation and observance of malicious programs

and teaches 5 design principles:
- Least Privilege - dont assign permissions they dont need to carry out their tasks
- Attack Surface Minimisation - during hardening, disable services you dont need
- Centralized Parameter Validation - invalid inputs can be used to exploit or disrupt systems
- Centralized General Security Services - centralize all security services, e.g. authentication
- Preparing for Error and Exception Handling - if firewall crashes, block all traffic; error messages should not leak sensitive information


```
Q: Which principle are you applying when you turn off an insecure server that is not critical to the business?

A: Attack Surface Minimisation
```

```
Q: Your company hired a new sales representative. Which principle are they applying when they tell you to give them access only to the company products and prices?

A: Least Privilege
```

```
Q: While reading the code of an ATM, you noticed a huge chunk of code to handle unexpected situations such as network disconnection and power failure. Which principle are they applying?

A: Preparing for Error and Exception Handling
```

###### Task 8

Trust principles:
- Trust but Verify - always verify, even when we trust an entity and its behaviour
- Zero Trust - treat trust as vulnerability - "never trust, always verify"

Three terms related to security weaknesses are: 
- Vulnerability - vulnerable means susceptible to attack or damage.
- Threat - potential danger associated with weakness / vulnerability
- Risk - likelihood of threat actor exploiting a vulnerability, and the impact on the business

