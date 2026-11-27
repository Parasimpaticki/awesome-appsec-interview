# Awesome AppSec Interview [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of resources, practice questions, and study materials to help you prepare for **Application Security Engineer** interviews, organized by interview type.


## Contents

- [Interview Overview](#interview-overview)
- [Secure Code Review](#secure-code-review)
- [Threat Modeling](#threat-modeling)
- [Coding & Scripting](#coding--scripting)
- [Scenario-Based Interviews](#scenario-based-interviews)
- [Technical Knowledge](#technical-knowledge)
- [System Design](#system-design)
- [Behavioral Interviews (STAR)](#behavioral-interviews-star)
- [Related Resources](#related-resources)
- [Contributing](#contributing)
- [License](#license)

## Interview Overview

### What to Expect
Most AppSec interview loops include a mix of:

- Secure Code Review
- Threat Modeling
- Coding or Scripting
- Scenario-Based Questions
- Technical Knowledge
- System Design (Senior+)
- Behavioral Interview

### General Interview Tips
- **Ask clarifying questions** - Questions are intentionally vague to see how you think 
- **Think out loud** - Verbalize your reasoning process 
- **Write down notes** - Track requirements and constraints 
- **Show your approach** - Process often matters more than perfect answers 
- **Don't rush to solutions** - Explore the problem space first 
- **It's okay to not know everything** - Show how you'd find the answer


## Secure Code Review

### What You’re Tested On
- Identifying vulnerabilities from code
- Following data flow (sources → sinks)
- Understanding exploitability
- Recommending pragmatic mitigations

### Core Concepts
- OWASP Top 10 vulnerabilities and mitigations 
- Language-specific vulnerability patterns 
- Taint analysis and data flow 
- Understanding the code

### Learning Resources
- **[Code Review Lab](https://www.codereviewlab.com/)** - Interview style secure code review challenges 
- [OWASP WebGoat](https://owasp.org/www-project-webgoat/) - Deliberately insecure application 
- [OWASP Code Review Guide](https://owasp.org/www-project-code-review-guide/)
- [OWASP Cheat Sheet Series](https://cheatsheetseries.owasp.org/)
- [PortSwigger Web Security Academy](https://portswigger.net/web-security)
- [Security Labs (The Work Gym)](https://theworkgym.com/security-labs/) - Break a feature, fix the code and prove the fix holds, in Java, Python and TypeScript labs mapped to the OWASP Top 10 and CWE.

### Common Interview Questions
- Walk through this code and identify issues
- Why is this vulnerable (or not)?
- How would you exploit this?
- How would you fix it?


## Threat Modeling

### What You’re Tested On
- Structured thinking
- Identifying threats early
- Prioritization and trade-offs
- Communication with engineers

### Core Concepts
- **STRIDE** - Spoofing, Tampering, Repudiation, Information Disclosure, DoS, Elevation of Privilege 
- 4 Questions framework
- Data Flow Diagrams (DFDs) 
- Attack trees 
- Trust boundaries 
- Asset identification and threat prioritization 
- Always cover **the basics** (_eg using TLS for data in transit_)

### Learning Resources
**Videos**
- [World’s Shortest Threat Modeling Course](https://www.youtube.com/playlist?list=PLCVhBqLDKoOOZqKt74QI4pbDUnXSQo0nf)
- [STRIDE in 20 Minutes](https://www.youtube.com/watch?v=rEnJYNkUde0)

**Reading**
- [Threat Modeling Beginner’s Guide](https://shostack.org/resources/threat-modeling)
- [Threat Modeling Modern Applications](https://behradtaher.dev/2022/05/27/Threat-Modeling-Modern-Applications/)
- [OWASP Threat Modeling](https://owasp.org/www-project-threat-model/)

**Books**
- *Threat Modeling: Designing for Security* – Adam Shostack

### Common Interview Questions
- Threat model a login flow / payment system / API
- How do you prioritize threats?
- Explain STRIDE
- Difference between threat modeling and pentesting? 
- What are trust boundaries?

## Coding & Scripting

### Coding (Algorithms & DSA)

#### What You’re Tested On
- Problem-solving
- Data Structures

#### Core Concepts
- Arrays, hash maps, stacks, queues
- Trees and graphs (basic)
- Big-O reasoning
- Common patterns (two pointers, BFS/DFS)

#### Learning Resources
- **[LeetCode Interview Crash Course](https://leetcode.com/explore/interview/card/leetcodes-interview-crash-course-data-structures-and-algorithms/)** - Structured curriculum 
- Practice Easy/Medium on [LeetCode](https://leetcode.com/) 
- Focus on patterns: [LeetCode Patterns](https://seanprashad.com/leetcode-patterns/) 
- [NeetCode Roadmap](https://neetcode.io/roadmap) - 150 essential problems
- [NeetCode](https://www.youtube.com/@NeetCode) - Excellent explanations 
- [NeetCode YouTube Playlists](https://www.youtube.com/@NeetCode/playlists)
- [Cracking the Coding Interview](https://www.amazon.co.uk/Cracking-Coding-Interview-6th-Programming/dp/0984782850) 
- [Grokking Algorithms](https://www.manning.com/books/grokking-algorithms)


#### Recommended Problem Count
- **Minimum:** 50-75 Easy/Medium problems 
- **Comfortable:** 100-150 problems covering all patterns 
- **Well-prepared:** 200+ problems

### Scripting & Automation

#### What You’re Tested On
- Practical automation
- Log and data parsing
- Security tooling familiarity

#### Core Concepts
- **Log parsing** - Extract IPs, domains, timestamps, user agents 
- **API interaction** - Query security APIs, submit data 
- **Data transformation** - JSON/XML/CSV parsing and manipulation 
- **Pattern matching** - Regex for security indicators 
- **File operations** - Read, parse, and process security data

#### Learning Resources
- [Automate the Boring Stuff](https://automatetheboringstuff.com/) - Python fundamentals 
- [HackerRank Python Track](https://www.hackerrank.com/domains/python) - Practice Python basics 
- [HackerRank Regex Track](https://www.hackerrank.com/domains/regex) - Pattern matching 
- [ExplainShell](https://explainshell.com/) - Understand bash commands

### Common Interview Questions
- Parse web server logs for suspicious activity 
- Find patterns indicating scanning/enumeration 
- Parse Nmap XML output and generate reports 
- Aggregate results from multiple security tools 
- Find all URLs/IPs/email addresses in text 
- Basic port scanner 
- HTTP header security checker 
- Simple vulnerability scanner

## Scenario-Based Interviews

### What You’re Tested On
- Security judgment
- Communication
- Risk assessment
- Incident handling

### Core Concepts
- Vulnerability triage
- CVSS and severity
- Incident response lifecycle
- Root cause analysis

#### Learning Resources
- Public Bug Bounty Write Ups 
- Public post-mortem blog posts

### Common Interview Questions
- Walk through a vulnerability you found
- How would you triage this report?
- Explain a recent CVE
- How does SSTI / XSS / SSRF work?


## Technical Knowledge

### What You’re Tested On
- Overall security knowledge
- Usually conducted by senior security engineer
- Will go into depth in one of these areas based on the role

### Core Concepts
- Cryptography
  - Symmetric vs Asymmetric (When to use each) 
  - Hashing 
  - TLS/SSL (Handshake process) 
  - PKI 
  - Difference between encryption, encoding, hashing?
- Authentication & Authorization
  - MFA 
  - Protocols (OAuth 2.0, SAML, JWT) 
  - Session Management and attacks 
  - Authorization Models (RBAC, ABAC, ACLs)
- Web Security
  - Core Vulnerabilities (OWASP Top 25) 
  - Mitigation and mitigating factors for each one 
  - HTTP Headers 
  - CORS 
  - Same-origin policy
- Cloud & Container Security
  - IAM best practices 
  - Shared responsibility model 
  - Container Security 
  - Security implications of serverless
- Secure Architecture Principles
  - Defense in depth 
  - Zero trust architecture 
  - Least privilege 
  - Fail securely 
  - Security by default 
  - Secure SDLC integration

### Learning Resources
- [Crypto101](https://www.crypto101.io/) 
- [OWASP Cryptographic Storage](https://cheatsheetseries.owasp.org/cheatsheets/Cryptographic_Storage_Cheat_Sheet.html) 
- [OAuth 2.0 Simplified](https://www.oauth.com/) 
- [JWT.io](https://jwt.io/) 
- [OWASP Authentication Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html) 
- [AWS Security Best Practices](https://aws.amazon.com/security/best-practices/) 
- [Cloud Security Alliance](https://cloudsecurityalliance.org/) 
- [PortSwigger Web Security Academy](https://portswigger.net/web-security) 
- [OWASP Top 10](https://owasp.org/www-project-top-ten/) 
- [OWASP Testing Guide](https://owasp.org/www-project-web-security-testing-guide/) 
- **[Secure by Design](https://www.manning.com/books/secure-by-design)** 
- [Security Engineering - Ross Anderson](https://www.cl.cam.ac.uk/~rja14/book.html) - Free 
- [OWASP SAMM](https://owaspsamm.org/) 
- [NIST Cybersecurity Framework](https://www.nist.gov/cyberframework)


## System Design

### What You’re Tested On
- Secure-by-design thinking
- Scalability + security trade-offs
- Real-world constraints

### Core Concepts
- Auth at scale
- Rate limiting & abuse prevention
- Secrets management
- Audit logging
- Defense in depth

### Learning Resources
- **[Grokking the System Design Interview](https://www.designgurus.io/course/grokking-the-system-design-interview)** 
- [Grokking Modern System Design](https://www.educative.io/courses/grokking-modern-system-design-interview-for-engineers-managers)
- **[ByteByteGo - Algorithms for System Design](https://www.youtube.com/playlist?list=PLCRMIe5FDPsdSsAdVfub8OCVeFi-5m06O)** - Start here 
- [ByteByteGo - System Design Interviews](https://www.youtube.com/playlist?list=PLCRMIe5FDPseVvwzRiCQBmNOVUIZSSkP8) 
- [NeetCode - System Design](https://www.youtube.com/playlist?list=PLot-Xpze53le35rQuIbRET3YwEtrcJfdt)
- [System Design Interview Vol 1 & 2](https://www.amazon.com/System-Design-Interview-insiders-Second/dp/B08CMF2CQF) 
- [Hacking the System Design Interview](https://www.amazon.co.uk/Hacking-System-Design-Interview-depth/dp/B0B7QHRK5Q)


## Behavioral Interviews (STAR)

### What You’re Tested On
- Ownership
- Influence
- Conflict handling
- Learning mindset

### Core Concepts
- STAR Framework
  - **S**ituation - Context and background 
  - **T**ask - Your specific responsibility 
  - **A**ction - What YOU did (be specific) 
  - **R**esult - Outcomes and lessons learned
- Prepare 5–7 stories
- Quantify impact
- Focus on **your** actions
- Show growth

### Learning Resources
- [Understanding the STAR interview format](https://uk.indeed.com/hire/c/info/understanding-the-star-interview-format)
- [Tech Interview Handbook – Behavioral](https://www.techinterviewhandbook.org/behavioral-interview/)


## Related Resources

### Interview Prep
- [Tech Interview Handbook](https://www.techinterviewhandbook.org/)
- [Grace Nolan’s Notes](https://github.com/gracenolan/Notes/blob/master/interview-study-notes-for-security-engineering.md)

### Awesome Lists
- [awesome-security](https://github.com/sbilly/awesome-security)
- [awesome-appsec](https://github.com/paragonie/awesome-appsec)


## Contributing

Contributions are welcome! Just submit a PR!

**Guidelines**
- Add resources relevant to AppSec interviews
- Follow existing section structure
- Ensure links are stable and reputable
