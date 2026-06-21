**2026-06-21**

# What was the Morris Worm?
- It was the first worm ever registered and released publicly. During november of 1988, Robert Morris released a program capable of self-replication across a network of computers by exploiting vulnerabilities in the UNIX systems.
# Why it happened?
- The initial objective was to use the program to measure how much computers were connected to the network. However, the code had a flaw that caused it to replicate itself more than intended, causing major disruptions across the network due to memory and CPU exhaustion.

# What happened after?
- Morris was the first person convicted under the Computer Fraud and Abuse Act of 1986, charged with a felony.
- This also made the community take computer security more seriously, leading to the creation of CERT (Computer Emergency Response Team), which is an organization that works to protect against cyber threats.

# Technical side
- Exploited BSD OS vulnerabilities
- Used "sendmail" debugging flaw to gain access to other computers and replicate itself.
- Used "fingerd" buffer overflow to execute commands on target machines. This was also one of the first buffer overflow apparitions in the wild.

# Questions
- How does current 2020s worms work?
- How does current security teams detect these kind of malware? What signature do they have?
- Are 'sendmail' and 'fingerd' still used? do they have a modern equivalent?