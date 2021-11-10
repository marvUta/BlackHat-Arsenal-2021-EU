# BlackHat-Arsenal-2021-EU
Repo-Links to BlackHat Arsenal 2021 EU(Links are in the detail area)

Notify me if I miss some repo to a presentation or you find some, thanks.

## Tools-Presentations with Repo-Links

<details>
  <summary>WhoC: Peeking Under the Hood of CaaS Offerings</summary>
  
Running your business-critical applications on the public cloud involves trust. You trust your cloud provider to separate your workloads from other customers' workloads. You trust your cloud provider to patch and update their software and hardware stack. For those of us with trust issues, blindly running our applications in the public cloud can be tough. Fortunately, trust can be earned through visibility, and that's where WhoC can help. WhoC provides a bit of visibility into how Container-as-a-Service (CaaS) offerings run our containers.

WhoC (Who Contains) is a container image that upon execution extracts the underlying container runtime. It doesn't try to identify the underlying runtime based on the container's cgroup configuration, the existence of a '.dockerenv' file or any other known trick. WhoC exfiltrates the actual container runtime binary from the underlying host.

In this talk Yuval will walk you through how WhoC works and show a demo in a popular CaaS offering. You'll learn a surprising truth: Linux containers can actually access one host file - the container runtime. 
  
  [https://github.com/twistlock/whoc](WhoC)

</details>

<details>
  <summary>Slips: A Machine-Learning Based, Free-Software, Network Intrusion Prevention System</summary>
  
Slips is a behavioral-based intrusion prevention system, and the first free software to use machine learning to detect attacks in the network. It is a modular system that profiles the behavior of IP addresses and performs detections in time windows. Slips' modules detect a range of attacks both to and from the protected device. Slips connects to other Slips using P2P, and exports alerts to other systems.

Slips works in several directionality modes. The concept of home network is not used to choose which detection to apply, but to choose which profile to analyze. The user can choose to detect attacks coming *to* or going *from* these profiles. This makes it easy to protect your network but also to focus on infected computers inside your network.

Among its modules, Slips includes the download/manage of external Threat Intelligence feed (including our laboratory's own TI feed), whois/asn/geocountry enrichment, a LSTM neural net for malicious behavior detection, port scanning detection (vertical and horizontal) on flows, long connection detection, etc. The decisions to block profiles or not are based on ensembling
algorithms. The P2P module connects to other Slips to share detection alerts.

Slips can read packets from the network, pcap, Suricata, Zeek, Argus and Nfdump, and can output alerts files and summaries. Having Zeek as a base tool, Slips can correctly build a sorted timeline of flows combining all Zeek logs. Slips can send alerts using the STIX/TAXII protocol.

More importantly, the Kalipso Node.js interface allows the analysts to see the profiles' behaviors and detections performed by Slips modules directly in the console. Kalipso displays the flows of each profile and time window and compares those connections in charts/bars. It also summarizes the whois/asn/geocountry information for each IP that communicates with a protected device.

  
  [https://github.com/stratosphereips/StratosphereLinuxIPS](Slips)

</details>

<details>
  <summary>RIoTPot: A Modular Hybrid-Interaction IoT/OT Honeypot</summary>
  
  With attacks against Internet of Things (IoT) and Operational Technology (OT) protocols increasing, we need proper defensive tools as well as methods for studying adversarial techniques. RIoTPot is a novel IoT/OT honeypot that is written in Go and moves beyond the traditional binary world of low vs. high interaction level. It achieves this via a modular architecture that allows for hybrid deployment of low-interaction along with high-interaction components (based on containerization techniques) as per users' preferences. RIoTPot emulates a multitude of common IoT and OT protocols such as CoAP, MQTT, Modbus, Telnet, AMQP, SSH, HTTP and UPnP.
  
  [https://github.com/aau-network-security/riotpot](RIoTPot)

</details>

<details>
  <summary>Dependency Combobulator</summary>
  The Dependency Combobulator is a modular and extensible framework to detect and prevent dependency confusion leakage and potential attacks. This facilitates a holistic approach for ensure secure application releases that can be evaluated against different sources (e.g., GitHub, Artifactory) and many package management schemes (e.g., ndm, pip, maven).

The framework can be used by security auditors, pentesters and even baked into an enterprise's application security program and release cycle in an automated fashion.
 
  https://pythonrepo.com/repo/apiiro-combobulator-python-security

</details>

<details>
  <summary>Wireshark Forensics Toolkit</summary>
  
  Wireshark is the most widely used network traffic analyzer. It is an important tool for both live traffic analysis & forensic analysis for forensic/malware analysts. Even though Wireshark provides incredibly powerful functionalities for protocol parsing & filtering, it does not provide any contextual information about network endpoints. For a typical analyst, who has to comb through GBs of PCAP files to identify malicious activity, it's like finding a needle in a haystack.

Wireshark Forensics Toolkit is a cross-platform Wireshark plugin that correlates network traffic data with threat intelligence, asset categorization & vulnerability data to speed up network forensic analysis. It does it by extending Wireshark native search filter functionality to allow filtering based on these additional contextual attributes. It works with both PCAP files and real-time traffic captures.

This toolkit provides the following functionality
- Loads malicious Indicators CSV exported from Threat Intelligence Platforms like MISP and associates it with each source/destination IP from network traffic
- Loads asset classification information based on IP-Range to Asset Type mapping which enables filtering incoming/outgoing traffic from a specific type of assets (e.g. filter for 'Database Server', 'Employee Laptop' etc)
- Loads exported vulnerability scan information exported from Qualys/Nessus map IP to CVEs.
- Extends native Wireshark filter functionality to allow filtering based severity, source, asset type & CVE information for each source or destination IP address in network logs

[https://github.com/rjbhide/wireshark-forensics-plugin](wireshark-forensics-plugin)
</details>


<details>
  <summary>AADInternals: The Swiss Army Knife for Azure AD & M365</summary>
  
AADInternals is a popular attacking and administration toolkit for Azure Active Directory and Microsoft 365, used by red and blue teamers worldwide. The toolkit is written in PowerShell, making it easy to install and use by anyone familiar with the Microsoft ecosystem.

With AADInternals, one can create backdoors, perform elevation of privilege and denial-of-service attacks, extract information, and even bypass multi-factor authentication (MFA).

Join this session to see in action the research results conducted during the past two years, including a new technique to extract AD FS signing certificates remotely.
  
https://github.com/Gerenios/AADInternals

</details>

<details>
  <summary>The Vulnerability Complete Definition Library</summary>
  
More and more security researchers treat source code as a database and use code patterns to search or query potential vulnerabilities. At the Black Hat 2021 USA conference, the 360 ​​Alpha Lab team disclosed how to use code patterns to find 11 CVEs on Chrome, and developed a 0day exploit based on this. The code pattern is essentially a set of conditions for the code, and the code that satisfies certain conditions is very likely to have vulnerabilities. However, the industry does not seem to have a publicly available tool that can accurately describe or define the necessary and sufficient conditions for a specific vulnerability. Although CodeQL (https://securitylab.github.com/tools/codeql/) is already trying to convert the vulnerability described in natural language in Common Weakness Enumeration (https://cwe.mitre.org/) into query sentences , But most of its query conditions are sufficient and non-essential conditions to form a specific vulnerability, that is, it does not include all the circumstances that form this vulnerability. These query sentences avoid the conditions that CodeQL is difficult to process or describe to improve the success rate of the query. And I personally think that the grammatical rules of SQL often cannot intuitively describe the constraints of the code and the code running process, and a large number of built-in query processes also make the learning cost higher.

Therefore, I have developed a complete definition library for vulnerabilities and believe that this library has two main advantages. First, this library can describe constraints with syntax, design ideas, and keywords similar to the code used by developers, which makes this tool have a lower learning cost. Second, this library is designed to describe the necessary and sufficient conditions for the formation of vulnerabilities. The necessary and sufficient conditions here is used to describe all possible situations that form the vulnerabilities. We should not artificially modify the search conditions to make it easier for the algorithm of the search program to search for results, but should let the search algorithm determine by itself how to search can speed up the display of results.

This library is developed based on LLVM's AST (Abstract Syntax Tree) and the constraint solver STP (Simple Theorem Prover), and supports the description of constraints on objects such as control flow, data flow, value size, variable relations, variable types, variable names, etc. The library will also contain a batch of vulnerability definitions I wrote and a simple search algorithm. I will use a simple example to demonstrate how the algorithm finds a vulnerability in a specific situation based on the vulnerability definition. All source code will be hosted on github, you can download and study by yourself.  
  
 https://github.com/antgroup-arclab/TheVulnerabilityCompleteDefinitionLibrary 

</details>


<details>
  <summary>AppsecStudy: Open-Source eLearning Management System for Information Security
</summary>
Because preventing vulnerability is less costly than redeveloping the complete application, infosec education and training become more and more actual. As a result, developers can greatly reduce the risk and expense from cyber attacks in the future by creating secure code. In addition, training the team based on the security assessment results to correct actual errors provides ongoing protection for existing and future products.

Since studying is impossible without a practical part, providing hands-on lab training for developing teams is a necessary step.
AppsecStudy - an open-source platform for seminars, training, and organizing courses for practical information security for developers and IT specialists. This tool has all the built-in basic requirements needed for organizing normal and productive training.
  
https://appsec.study
  
https://github.com/zzzteph/appsec.study
  
</details>

<details>
  <summary>UART Brute Forcing</summary>
  
With the growth of embedded systems the ability to exploit UART has become a key component of a Hardware Vulnerability Assessment. This tool focuses on Bute Forcing UART connections on embedded devices. It allow uses to define a brute forcing process for a wide variety of embedded systems

https://github.com/Merimetso-Code/UART-Hacking
</details>

<details>
  <summary>Kubestriker: A Blazing Fast Security Auditing Tool</summary>
  
Kubestriker performs numerous in depth checks on kubernetes infrastructure to identify any misconfigurations which make organisations an easy target for attackers and safeguards against potential attacks on Kubernetes clusters.

https://github.com/vchinnipilli/kubestriker
  
</details>

<details>
  <summary>crawlergo: A Powerful Browser Crawler for Web Vulnerability Scanners</summary>
  
crawlergo is a browser crawler that uses chrome headless mode for URL collection. It dynamically finds all URL requests contained in a web page through powerful automated intelligent analysis and de-duplication, providing comprehensive and high quality input for subsequent web vulnerability scanning.
  
  https://github.com/Qianlitp/crawlergo
  
</details>

<details>
  <summary>Adhrit: Android Security Suite</summary>
  
Adhrit is an open-source Android application security analysis suite. The tool is an effort to find an efficient solution to all the needs of mobile security testing and automation. Adhrit has been built with a focus on flexibility and modularization. It currently uses the Ghera benchmarks to identify vulnerable code patterns in the bytecode. Apart from bytecode scanning, Adhrit can also identify hardcoded secrets within Android applications. The tool also comes with a built-in integration to popular softwares like Jira and Slack which can be configured to automate and streamline the Android application review process. Adhrit has been presented at conferences like Black Hat Asia, OWASP Seasides and Cysinfo.
</details>

https://github.com/abhi-r3v0/Adhrit

<details>
  <summary>DNSStager: A Tool to Hide Your Payload in DNS</summary>
  
  DNSStager is an open-source project based on Python used to hide and transfer your payload using DNS.

DNSStager will create a malicious DNS server that handles DNS requests to your domain and return your payload as a response to specific record requests such as AAAA or TXT records after splitting it into chunks and encoding the payload using different algorithms.

DNSStager can generate a custom agent written in C or GoLang that will resolve a sequence of domains, retrieve the payload, decode it and finally inject it into the memory based on any technique you want.

You can edit the code of the DNSStager agent as you wish, and build it using your own custom execution techniques.

The main goal of using DNSStager is to help red teamers/pentesters to deliver their payloads in a stealthy channel using DNS.

  
  https://github.com/mhaskar/DNSStager
</details>

<details>
  <summary>Siembol: An Open-Source Real-Time SIEM Tool Based on Big Data Technologies
</summary>
  Siembol is an in-house developed security data processing application, forming the core of an internal Security Data Platform.

Following the experience of using Splunk, and as early adopters of Apache Metron, the team needed a highly efficient, real-time event processing engine with fewer limitations and more enhanced features. With Metron now retired, Siembol hopes to give the community an evolved alternative.

Siembol improvements over Metron:
- Components for real-time alert escalation: CSIRT teams can easily create a rule-based alert from a single data source, or they can create advanced correlation rules that combine various data sources. Moreover, Siembol UI supports importing a Sigma rule into Siembol alerting.
- Ability to integrate with other systems using dedicated components and plugin architecture for easy integration with incident response tools
- Advanced parsing framework for building fault-tolerant parsers
- Enhanced enrichment component allowing for defining rules and joining enrichment tables
- Configurations and rules are defined by a modern Angular web application, with a git-based approval process
- Supports OAuth2/OIDC for authentication and authorization in Siembol UI
- Easy installation for use with prepared docker images, helm charts and quick start guide

Siembol Use Cases:
- SIEM log collection using open-source technologies
- Detection tool for discovery of leaks and attacks on infrastructure
- Real-time stream Sigma rule evaluation without need to index logs

 https://github.com/G-Research/siembol 
</details>

<details>
  <summary>Pentest Collaboration Framework</summary>
  
Pentest Collaboration Framework - An opensource, cross-platform and portable toolkit that allows you to exchange information on the penetration testing process. It also contains a model of differentiation of rights for use by several teams or independent researchers.

One of latest major updates from previous Black Hat conference is a new feature - issue templates library which allow pentesters to create issues much more faster!
  
  https://gitlab.com/invuls/pentest-projects/pcf
</details>

<details>
  <summary>In0ri</summary>
  
Have you ever wondered how many ways there are to detect a defacement attack?

- Based on hash
- Based on signature
- Differential comparison
- Machine learning

Well, quite a lot. Nowadays, machine learning have really developed, with increasing agility and accuracy, this is
a new approach in Cyber Security in general which can adapt to new attack techniques.

In this talk, we will be presenting In0ri - a defacement detection system utilizing image-classification convolutional neural network.
There's two ways to deploy and use In0ri:
- Running off crontab by periodically visiting the URL.
- Internal agent running off the web server

With the first method, we can directly check if a path has been defaced or not.
As a system administrator, we can use the second method to check a local website with an internal Agent.

In0ri the first source machine learning project to detect defacement attacks, we will show the process of installing, training and running In0ri. After that, we will show how it succeeds to get high quality of detecting the deface attacks by using deep learning.

  
  https://github.com/J4FSec/In0ri
  
</details>


<details>
  <summary>CQPenetrationTesting Toolkit: Powerful Toolset That All Pentesters Want to Have
</summary>
  CQ Penetration Testing Toolkit supports you in performing complex penetration tests as well as shows the ways to use them, and the situations in which they apply. It guides you through the process of gathering intel about network, workstations, and servers. Common technics for antimalware avoidance and bypass, lateral movement, and credential harvesting. The toolkit allows also for decrypting RSA keys and EFS protected files as well as blobs and objects protected by DPAPI and DPAPI-NG. This powerful toolkit is useful for those who are interested in penetration testing and professionals engaged in pen-testing working in the areas of database, system, network, or application administration. Among published presented tools are CQARPSpoofer, CQCat, CQDPAPIBlobDecrypter, CQMasterKeyDecrypt, CQReverseShellGen, and many more.

https://github.com/BlackDiverX/cqtools
  
</details>

<details>
  <summary>Mobile Malware Mimicking Framework</summary>
  
Emulating malware is a great way to gain insight into the behaviour of threat actors, and to fetch the newest malware samples and modules from the source. Emulating Android malware using virtual machines is a resource intensive task that does not scale well. To resolve this, I wrote the open-source Mobile Malware Mimicking framework, or m3 in short. The framework is built to easily and scalable emulate Android malware whilst using very few resources. Currently, the renowned Anubis and Cerberus families are supported within the framework.

m3's architecture focuses on three main points: simplicity, security, and scalability. To simplify the implementation of new families, the framework is written in Java, which allows the usage of decompiled code snippets. Additionally, the framework provides internal APIs to simplify the workflow. Each bot contains a phone object, which contains many commonly used Android features in plain Java, optimised for emulation purposes. This way, decompiled code only needs minor tweaks before it is executable within the framework. The framework is secure, as unknown commands are logged and furthermore ignored. Due to its open-source nature, anyone can audit and improve the project. Due to the plain Java implementation of the bots, the framework requires very little memory, compared to the virtual machines that would otherwise be required. Adding more bots barely increases the memory usage, allowing a single machine to handle dozens of bots at once.

To use m3, one must first create one or more bots and provide all required details, after which the bots can be emulated. Logging of activities is done per bot, in both the standard output, and a log file per bot. This provides analysts with a detailed overview of the activities that occurred over time.
  
  https://maxkersten.nl/projects/m3-framework/
  
  https://github.com/ThisIsLibra/m3
</details>

<details>
  <summary>RPC-FireWall</summary>
  
In Windows based environments, RPC is the main underlying protocol required for remote administration and for Active Directory services. As such, it is often used by IT admins, but also by ransomware and advanced attackers to spread by creating remote services, scheduled tasks, DCOM objects, etc. It is also a major component in the persistency phase of attacks such as active directory DCSync, and even DC vulnerabilities such as Zerologon.

The RPC-FireWall is a simple tool to operate, which can be used by security researchers and SOC teams. It places strategically located hooks in the Windows RPC runtime, which enables the operator to audit and control every RPC call. Security researchers can use it to trace and understand how various RPC based lateral movement techniques work. SOC teams can consume the audit information, which is stored to the Event logs, into their SIEM / XDR and use it to create numerous detection rules. The RPC-FireWall also acts as a - well, firewall - which allows defenders granular control over which RPC protocols and methods are allowed, from where, by whom, etc. while potentially malicious RPC calls could be blocked. 
  
https://github.com/zeronetworks/rpcfirewall
</details>

<details>
  <summary></summary>
  
</details>


## Webinars/Sessions/Talks

<details>
  <summary>Disrupting OT and IoT by Exploiting TCP/IP Stacks</summary>
  
We will demonstrate an attacker’s journey to disrupt a model smart building - which could be a residence, an office, or any critical facility like a hospital - using only TCP/IP stack vulnerabilities, which are known to affect large numbers of devices at a time.

Attendees will interact with a tool to identify the TCP/IP stack running on a target device (using techniques such as banner grabbing, ICMP querying and TCP fingerprinting), a static analysis tool to find DNS-based vulnerabilities on TCP/IP stacks, and finally an exploit scenario involving a DNS-based RCE on a development board, an FTP-based DoS on a PLC and a TCP-based DoS on the switch connecting them.

The physical effects on the model building include switching on or off lighting and ventilation systems. We will also discuss how a similar exploit scenario can lead to other types of physical effects in critical infrastructure.
 
  https://www.forescout.com/resources/amnesia33-how-tcp-ip-stacks-breed-critical-vulnerabilities-in-iot-ot-and-it-devices/
  
  !!!404 at the Webinar Link at the bottom of the pages!!! Maybe you got more luck

</details>

<details>
  <summary>Implement DMARC the Right Way to Keep Phishing Attacks Out of Your Inbox</summary>
  
DMARC, SPF, and DKIM are global anti-domain-spoofing standards, which can significantly decrease phishing attacks. Implemented correctly they allow you to monitor email traffic, quarantine suspicious emails and reject unauthorized emails. But less than 30% of organizations are actually using them. And even fewer are using them correctly.

In this session, Roger Grimes, KnowBe4’s Data-Driven Defense Evangelist, will teach you how to enable DMARC, SPF, DKIM the right way. You’ll learn:

    How to best configure DMARC and other defenses to prevent phishing attacks
    What common configuration mistakes organizations make
    Why a strong human firewall is your best last line of defense
  
https://blog.knowbe4.com/implement-dmarc-the-right-way-to-keep-phishing-attacks-out-of-your-inbox
</details>


<details>
  <summary>What Do You Do First, Next, and How Do You Future-Proof Your Organization From Another Such Attack?</summary>
  
You have just learned that your organization has been hit with a new variant of REvil ransomware
Every minute counts. What you do first, next, and how you future-proof your organization from another such attack is critical in the first 24 hours of a breach.
Join us for “Race Against Time,” a simulation event where Cortex, by Palo Alto Networks, provides the critical steps Security Operations teams need to do in the first 24 hours to investigate and respond to an attack.  
  
</details>


<details>
  <summary>From Asset Management to Asset Intelligence: Crossing the CAASM</summary>
  
As the sprawl of devices, device types, and solutions continues to skyrocket, environments only grow more complex.
But there's good news: asset management has evolved. Today’s “asset intelligence” moves from a spreadsheet approach to an API-driven, always up-to-date view into all assets via integrations of existing tools, data correlation at scale, and querying capabilities to find and respond to gaps. Join this session to learn how asset intelligence and the emerging Cyber Asset Attack Surface Management (CAASM) category improves security hygiene, reduces manual work, and remediate gaps.
  
https://store.isaca.org/s/community-event?id=a334w000004SGuCAAW
</details>

<details>
  <summary>Moving Beyond Threat Detection - A Look at The Future of Cybersecurity with Zero Trust</summary>
  
Join ThreatLocker CEO, Danny Jenkins as he discusses the state of cybersecurity and how to protect against ransomware with a zero trust architecture.
</details>

<details>
  <summary>Unlock Your SOC With Limitless Analysis</summary>
  
Imagine if you never again had to discard data, performing machine learning, threat intelligence lookups, proactive hunting, and more — at cloud scale, with no interruptions to your workflows.
Join this talk to explore the possibilities unlocked by the power to analyze all of your security-relevant data. Tackle any conceivable SecOps use case by exploring data from across your entire stack of technologies and applications. Uncover long-dwelling threats and markers of newly discovered exploits by examining years of data. And do it all with Elastic Security, the world’s only free and open SIEM and XDR solution.
  
https://www.elastic.co/de/webinars/unlock-your-soc-stop-threats-with-limitless-xdr  
</details>


<details>
  <summary>Active Directory Security: The Heart of the "Nuclear Reactor" in Identity Management</summary>
  
In all the recent breaches, attackers had one goal: to gain access to privileged accounts and roam freely through the network. They can then target sensitive assets and make Ransomware or data exfiltration breach attacks effective.

Behind identity thefts, there is always an insecure Active Directory (AD) deployment. AD is the Heart of the "Nuclear Reactor" of identity management. It has become a prime target for attackers to elevate privileges and facilitate lateral movement. 

In this session, we'll cover the main attack paths on AD, and how identity management programs need to evolve from a semi-annual audit stage to near-real-time prevention and detection capability around Active Directory.
  
  https://www.tenable.com/events/black-hat-europe-2021
</details>

<details>
  <summary>It's Time to Improve Your Release Fitness with Prisma Cloud DevSecOps</summary>
  
It's time to align security to the app lifecycle, improve the developer experience, and ensure we are releasing apps that are safe the first time, every time. With Prisma Cloud, customers don’t need to wait until the application is running to identify security risks. Prisma Cloud eliminates the necessity to review lots of security alerts and iterate your apps once again, adding overhead on developers and affecting your release fitness. We help you improve release velocity and the reliability of your apps as well as support your overall agility as a business.
  
  https://www.paloaltonetworks.com/prisma/cloud/devsecops
  
</details>

<details>
  <summary>Attacks on Critical Infrastructures: It, OT and AD : The 3 Pillars of the Attacks Surface</summary>
  
Attacking critical infrastructures is not just a matter of cybercrime. Its impact extends far beyond. When a hospital is down for days or a water supplier is compromised, these attacks have profound human consequences.

IT, OT and Active Directory are the 3 pillars of the attack surface in critical infrastructure systems. New paradigms, like remote work and cloud adoption, are increasing the risk to systems newly exposed to the Internet.

In this session, we will focus on an example in the Healthcare industry to show how to mitigate this risk by having a continuous, unified approach to risk-based vulnerability that embraces IT and OT assets and Active Directory.

https://www.tenable.com/events/black-hat-europe-2021
</details>

<details>
  <summary>One Simple Missed Vulnerability, One Big Headache</summary>

Developers are often regarded as the superhumans that know it all and can do everything. This is more than often true, however, if we start blaming them for errors in the security specter of their code we are doing them wrong. It is not their fault, but more the overall way on how development is completed from the architecture to the release. This presentation will explore how easy it is to miss security-related details that can be used by attackers to breach the victim’s data. If these go undetected throughout your SDLC and make it through your DevOps process to the release, then devastation is unavoidable. Therefore, we will conclude by showing you how to identify them at the right place and time to avoid delays in your delivery schedule.

https://www.cybersecuritycloudexpo.com/global/talk/virtual-presentation-one-simple-missed-vulnerability-one-big-headache/
</details>

<details>
  <summary>WhiskeySAML and Friends</summary>
  
Solorigate was one of the most significant cybersecurity attacks we have ever faced. One tactic used during the attack was to extract a token signing certificate from the on-prem Active Directory Federation Services (ADFS) server. With the certificate, adversaries were able to impersonate any user of the target organization and exfiltrate information. The technique used to extract the certificate required access to the target server.

Secureworks is constantly conducting primary research to find new vulnerabilities and techniques the adversaries may exploit. Based on this research, we are also conducting applied research to build proofs-of-concept and tools to demonstrate and automate the exploitations.

In this talk, we will introduce a new technique that allows extracting the signing certificate remotely without logging in on the target server. We'll cover the conceptual design of the new technique and walk through how it was developed and we will introduce/demonstrate three tools written in Python, which allows performing the whole attack remotely and automatically with a small input data set and the weaponization of the technique.
  
  https://www.secureworks.com/blog/going-for-the-gold-penetration-testing-tools-exploit-golden-saml
  
</details>

<details>
  <summary>USBsamurai: One Cable to Pwn'em All</summary>
  
During the last years, hardware implants have become a popular attack vector in air-gapped environments such as industrial networks: Stuxnet (2010), Operation Copperfield (2017), and the recent ransomware attack that has led to a shutdown in a US natural gas facility are only some notable cases. In parallel, in an effort to raise the bar of red-teaming operations, security researchers have been designing and releasing powerful open-source devices with the intent to make Red-Teaming operations even more interesting and disruptive. Smoothing the path to new TTPs and improving old ones. As a result, hardware implants should always be included in the threat modeling of an industrial facility.
  
</details>

<details>
  <summary>Why Is Security on the Back Foot and Can Continuous Authentication Help?</summary>
  
Digital technology developments have been turbo-charged in the past 18 months. Organizational engagement with customers and citizens has been reimagined. Running an enterprise, irrespective of size, has evolved dramatically. The pace of change shows little sign of slowing, and organizations are battling to keep up with and get ahead of demand and what their competition is capable of. The security function has had to turn on a sixpence and security has gone “haywire” in attempts to match the pace of organizational change. What can they do to get ahead of the game? Identity isn’t a bad place to start, and in this session we look at the challenges facing the organization from a security perspective and the role of continuous authentication in addressing these challenges over the next few years.

</details>

<details>
  <summary>How Can Your Organization Become Ransomware Ready?</summary>
  
Ransomware attacks have rapidly increased in frequency and severity. What was initially considered a nuisance has been adopted by sophisticated attackers in complex, multi-phased attacks. The total cost of ransomware attacks can climb into millions of dollars. This is why Pentera, the Automated Security Validation platform, added the first active ransomware emulation framework, applying real and safe ransomware tactics and techniques, to your organization’s framework. This framework enables you to validate your organization’s readiness against a ransomware attack at any given moment.

  
</details>

<details>
  <summary>Securing the Modern API Ecosystem</summary>
Stopping API attacks requires a 360-degree view of API security risks and collaboration between security and development teams. From secure API development and testing to runtime threat defense, through continuous API posture management, APIs present a new attack surface to defend. We will explore strategies to efficiently achieve an active, sophisticated API defense posture across each phase of the API lifecycle. A key focus will be on practices that employ automation to dramatically improve control and without stifling innovation and speed.

  https://www.eccu.edu/how-can-you-secure-the-modern-api-ecosystem/
  
</details>

<details>
  <summary>Automating Architectural Risk Analysis with the Open Threat Model Format</summary>
  
Architectural risk analysis is a crucial security activity that’s typically carried out manually in workshops. Although valuable, they are often time-consuming, and with engineering teams under increasing pressure to deliver software faster, they require techniques to automate as much of the process as possible.
Fraser will explore these challenges and how Infrastructure as Code is uniquely able to meet them. He’ll introduce the Open Threat Model (OTM) format and how to create files automatically using open source tools. We’ll look at how you can operationalize threat modeling with OTM into a DevSecOps workflow - useful if you have multiple teams using different technologies.

</details>


<details>
  <summary>The Dry Runs Are Over: Cyber-Physical Attacks Are A Main Event
</summary>
  SolarWinds. Oldsmar. JBS. Colonial Pipeline. High-impact cyberattacks on our physical world have leapt from thriller movie theories to real-time calamities. From disruptions in fuel production and delivery to shortages of meat and cheese on grocery store shelves, these attacks have very real consequences. Making matters worse, bad actors have set the precedent to demand growing ransoms by staging increasingly brazen attacks. Join us to explore a brief history of how we got here, why these attacks are so seemingly easy to conduct, and what we should do to keep them from escalating to dangerous new heights.

</details>

<details>
  <summary>Attack Driven Development: Leveraging Threat Intelligence to Build Better Products
</summary>
Nearly every organization claims to do vulnerability research and threat intelligence, but how does that filter into building a better product? At Trend Micro, our end-to-end lifecycle of threat research allows us unparalleled access into all phases of the lifecycle of a bug: from finding to reporting to patching to exploitation. At each stage of this process, information about the vulnerability provides defenders the opportunity to implement strategies to mitigate the threat. This talk covers the various types of investigation and analysis done by Trend researchers and how this data improves products to provide class-leading protections for our customers.

  
  https://www.youtube.com/watch?v=ltzuP1wFZjQ
</details>

<details>
  <summary>Packet Carving for SATCOMs Hackers</summary>
  
Satellite broadband services from geostationary orbit are often unencrypted and can leak important and sensitive information to anyone with basic hardware and software knowledge. In this lab, we'll get some hands-on experience working with modern satellite internet protocols. We'll have environments set up where you can play with satellite data in a variety of formats and use open-source tools to convert satellite traffic recordings into meaningful traffic captures. The labs are designed for diverse backgrounds and skill levels so no prior experience with programming, SATCOMs, or protocol reversing is necessary, but, if you have it, there's stuff that should be fun for you too.
  
</details>

<details>
  <summary>Levers of Human Deception: The Science and Methodology Behind Social Engineering
</summary>
  
No matter how much security technology we purchase, we still face a fundamental security problem: people. Explore the different levers that social engineers and scam artists pull to make us more likely to do their bidding.
Roger will share his insights and examples of mental manipulation in everyday life: from the tactics used by tricky advertisers to sophisticated social engineering and online scams. Additionally, we’ll look at how to ethically use the very same levers when educating your users.
Key Takeaways

    The Perception Vs. Reality Dilemma 
    Understanding the OODA (Observe, Orient, Decide, Act) Loop 
    How social engineers and scam artists achieve their goals by subverting
    How we can defend ourselves and our organizations
  
https://techtalksummits.com/event/virtual/webinar/levers-of-human-deception-the-science-and-methodology-behind-social-engineering2
</details>

<details>
  <summary>Next Generation Security Operation Center How to Combat New Threats Effectively ,Efficiently and in Near Real Time</summary>
  
Current SOCs typically focus on SIEM as the nerve centre and hub. And the standard modus operandi has been to onboard all log sources from Network, (Hosts) OS, Endpoints and Cloud (rarely possible) and then hope for magic (correlation) to happen. There is a substantial time wasted in setting it up by ‘tuning’ log sources. And there is a huge challenge as a hierarchy of L1-L3 analysts is set up so even when there are real security issues- it takes too much time to actually respond in a timely manner.
So in short, Gen 1 SoCs are : too expensive to run, too slow to react and still do not do the job effectively.
The solution lies in a better way to set up Stiching of data across Network, Endpoints and Cloud Telemetry that clearly indicates that when a security incident has happened- its impact on Network, Hosts, Endpoints and Cloud is ‘stitched’ into 1 story. Thus giving the analysts a proper ‘Stitch(ed) story) in Time’ to act quickly. 

https://www.cybersecuritycloudexpo.com/global/talk/next-generation-security-operations-centre-how-to-combat-new-threats-effectively-efficiently-and-in-near-real-time-basis/
</details>


<details>
  <summary>How to Replace Your SIEM Using XDR and a Security Data Lake
 </summary>
  
NETGEAR gained a clarity into incidents using automatic investigations of alerts and threat signals, with advanced correlations across attack surfaces, delivering the essential context the SOC needs to act on legitimate threats.

By combining Hunters XDR with Snowflake’s Security Data Lake, the retailer eliminated the high data storage costs associated with SIEM, allowing NETGEAR to stop making sacrifices on data retention and avoid compromising on the number of data sources.
  
https://www.youtube.com/watch?v=7EUXAhO_QDo
</details>


<details>
  <summary> </summary>

</details>



