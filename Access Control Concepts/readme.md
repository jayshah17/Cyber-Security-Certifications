# Access Control Concepts

## Module 1: Understand Access Control Concepts

Access controls are not just about restricting access to information systems and data, but also about allowing access. It is about granting the appropriate level of access to authorized personnel and processes and denying access to unauthorized functions or individuals.

A technical example of defense in depth, in which multiple layers of technical controls are implemented, is when a username and password are required for logging in to your account, followed by a code sent to your phone to verify your identity. This is a form of multi-factor authentication using methods on two layers, something you have and something you know. The combination of the two layers is much more difficult for an adversary to obtain than either of the authentication codes individually.

- The Principle of Least Privilege is a standard of permitting only minimum access necessary for users or programs to fulfill their function

Privileged Access Management

- Privileged access management provides the first and perhaps most familiar use case

Segregation of Duties 

- A core element of authorization is the principle of segregation of duties (also known as separation of duties).
-  Segregation of duties is based on the security practice that no one person should control an entire high-risk transaction from start to finish. Segregation of duties breaks the transaction into separate parts and requires a different person to execute each part of the transaction.

## Module 2: Understand Physical Access Controls

- Physical access controls are items you can physically touch. They include physical mechanisms deployed to prevent, monitor, or detect direct contact with systems or areas within a facility.
- Examples of physical access controls include security guards, fences, motion detectors, locked doors/gates, sealed windows, lights, cable protection, laptop locks, badges, swipe cards, guard dogs, cameras, mantraps/turnstiles, and alarms.

## Module 3: Understand Logical Access Controls

1. Discretionary Access Control (DAC)

- Discretionary access control (DAC) is a specific type of access control policy that is enforced over all subjects and objects in an information system. In DAC, the policy specifies that a subject who has been granted access to information can do one or more of the following:
    - Pass the information to other subjects or objects
    - Grant its privileges to other subjects
    - Change security attributes on subjects, objects, information systems or system components
    - Choose the security attributes to be associated with newly created or revised objects; and/or
    - Change the rules governing access control; mandatory access controls restrict this capability

 - Most information systems are DAC systems.

2. Mandatory Access Control (MAC)

- A mandatory access control (MAC) policy is one that is uniformly enforced across all subjects and objects within the boundary of an information system.
- In simplest terms, this means that only properly designated security administrators, as trusted subjects, can modify any of the security rules that are established for subjects and objects within the system. 
  - Passing the information to unauthorized subjects or objects
  - Granting its privileges to other subjects
  - Changing one or more security attributes on subjects, objects, the information system or system components
  - Choosing the security attributes to be associated with newly created or modified objects
  - Changing the rules governing access control 
