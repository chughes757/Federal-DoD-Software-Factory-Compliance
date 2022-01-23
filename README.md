# Federal-DoD-Compliance-Innovation
This repository is a collection of resources to help facilitate compliance innovation utilizing Cloud, DevSecOps and Software Factory technologies and implementations. 

## Background

There has been an increased push for to adopt Cloud, DevSecOps and Software Factories within the U.S. Federal and Department of Defense (DoD) enviroments. However, one of the largest impediments to these outcomes often is the incredibly cumbersome and bureaucratic compliance requirements in Federal environments. This repository will be a collection of resources that help facilitate compliance innovation which can lead to improved outcomes for U.S. Citizens, Warfighters and the nation as whole. 

Federal information systems adhere to what is known as the Risk Management Framework, or RMF. It is published and created by NIST and there are a wealth of resources one can dive into to understand RMF. RMF is what Federal information systems follow throughout their system development lifecycle and where the concept of Authorities to Operate, Continuous Monitoring and countless other relevant processes and practives are derived.

![image](https://user-images.githubusercontent.com/94196833/150681001-f59bb5c5-4383-420a-85cd-3bf9b64d7e46.png)

NIST RMF Resource Center (https://csrc.nist.gov/projects/risk-management/about-rmf)

The push for Security Compliance innovation in the Federal and DoD community has a lengthy history, with many innovators and pioneers. That said, this talk with Jez Humble titled "When DevOps Meets Regulation: Integrating Continuoius with Government" documents one of the early efforts in this space. It involved the work of the Generasl Service Administration's 18F, which utilized Cloud Infrastructure-as-Service (IaaS) coupled with an accredited Platform-as-a-Service (cloud.gov) to streamline compliance efforts using Cloud, Open Sourced security documentation, machine readable artifacts and security control inheritance. 

Video (https://youtu.be/STRpThSqKDk)



## Table of contents

- [Machine Readable Documentation](#machine-readable-documentation)
- [Security Control Inheritance](#security-control-inheritance)
- [Pre-Hardened Infrastructure-as-Code (IaC), Policy-as-Code (PaC) and artfiacts](#Pre-Hardened-Infrastructure-as-Code-(IaC)-Policy-as-Code-(PaC)-and-artfiacts)
- [Continuous Authority to Operate (cATO)/Ongoing Authorization (OA)](#Continuous-Authority-to-Operate-(cATO)-Ongoing-Authorization-(OA))
- [Continuous Monitoring ](#Continuous-Monitoring)
- [Creators](#creators)
- [Thanks](#thanks)


## DevSecOps 

Given that much of the success of cATO and OA efforts is being facilitated by DevSecOps practices and processes, it wouldn't be appropriate to not include some relevant DevSecOps resources in this repo. 

- DoD Enterprise DevSecOps 2.0 Fundamentals (https://software.af.mil/wp-content/uploads/2021/05/DoD-Enterprise-DevSecOps-2.0-Fundamentals.pdf)
- DoD Enterprise DevSecOps 2.0 Strategy Guide (https://software.af.mil/wp-content/uploads/2021/05/DoD-Enterprise-DevSecOps-2.0-Strategy-Guide.pdf)
- DoD Enterprise DevSecOps 2.0 Tools and Activities Guidebook (https://software.af.mil/wp-content/uploads/2021/05/DoD-Enterprise-DevSecOps-2.0-Tools-and-Activities-Guidebook.pdf)
- DoD Enterprise DevSecOps 2.0 Playbook (https://software.af.mil/wp-content/uploads/2021/05/DoD-Enterprise-DevSecOps-2.0-Playbook.pdf)
- DoD Enterprise DevSecOps Initiaitive - Ref Design 1.0 (https://dodcio.defense.gov/Portals/0/Documents/DoD%20Enterprise%20DevSecOps%20Reference%20Design%20v1.0_Public%20Release.pdf?ver=2019-09-26-115824-583)

## Machine Readable Documentation

One of the most challenging aspects of Federal and DoD compliance initiaitives is documenting the various security controls, control implementation statements and associated documentation for Federal IT systems to go into production environments. The below resources will highlight some of the efforts underway to make traditionally static and detailed documentation into machine readable formats. The benefits of this is that compliance validation can be semi-automated, re-usable and streamlined. 

Putting these typically static documents into code format allows system owners, assessors and other relevant agency and inter-agency POC's to ingest and share the documentation, leverage applications to review them and much more. 

- The Open Security Controls Assessment Language (OSCAL): NIST is developing the Open Security Controls Assessment Language (OSCAL) as a standardized, data-centric framework that can be applied to an information system for documenting and assessing its security controls. Today, security controls and control baselines are represented in proprietary formats, requiring data conversion and manual effort to describe their implementation. An important goal of OSCAL is to move the security controls and control baselines from a text-based and manual approach (using word processors or spreadsheets) to a set of standardized and machine-readable formats. With systems security information represented in OSCAL, security professionals will be able to automate security assessment, auditing, and continuous monitoring processes.

### OSCAL Resources 

- OSCAL 1.0.0 Release Candidate 2 (https://github.com/usnistgov/OSCAL/releases)
- Centers for Medicare and Medicaid (CMS) Rapid ATO (https://ato.cms.gov/rato.html)
- GovReady: What does a working OSCAL Component Library Really Look Like? (https://www.nist.gov/system/files/documents/2021/02/22/Day2.4-T1-Greg-Working%20Component%20Library.pdf)
- FedRAMP OSCAL Resources and Templates (https://www.youtube.com/watch?v=WCPkt56vZ-s)
- AWS Summit DC 2021: Accelerating FedRAMP with OSCAL (https://www.youtube.com/watch?v=YW7YSbSoYHI)


## The Federal Risk and Authorization Management Program (FedRAMP)

Given that many of the software factory implementations are predicated on the implementation of building on top of authorized Cloud services, no discussion would be complete without including FedRAMP. That said, FedRAMP is a large program with its own unique processes, policies and marketplace so this will serve as a pointer to FedRAMP. Anyone building a software factory on Cloud in Federal and DoD environments MUST ensure they're doing so on FedRAMP authorized cloud services, which can be found on the FedRAMP Marketplace. 


- FedRAMP (https://www.fedramp.gov/)

## DoD Cloud Security Requirements Guide (SRG)

Building on FedRAMP, if you're utilizing Cloud in the Department of Defense (DoD) you have to adhere to what is known as the Cloud Computing Security Requirements Guide (SRG). The SRG outlines the security model by which DoD will leverage cloud computing, along with the security controls and requirements necessary for using cloud-based solutions. It lays out how DoD adds additional controls on FedRAMP processes, known as "FedRAMP+" as well as categorizing various Impact Levels (IL)'s for DoD systems and data in the cloud. 

- DoD Cloud Computing SRG (https://dl.dod.cyber.mil/wp-content/uploads/cloud/zip/U_Cloud_Computing_SRG_V1R4.zip)

## Security Control Inheritance

As mentioned in the background section, security control inheritance is an absolutely critical part to streamlining Federal compliance burdens. It involves inheriting controls from Cloud IaaS, on-premise data centers, Platform-as-a-Service implementations and others to minimize the number of controls a system or application owner must meet. That said, it requires a thorough understanding of the Shared Resposibility Model, which involves inheriting controls and understanding where the control providers responsibility ends and yours begins. These controls typically are inherited entirely, shared between you and the control provider, or fully up to you and it is key to understanding which of those it is, across your entire security control baseline. 

- Security Control Inheritance Article (https://rmf.org/2019/04/05/security-control-inheritance/)
- Security Control Inheritance Artice (https://www.telos.com/2020/04/inheritance-role-in-cloud-compliance/)
- Shared Responsibility Article (https://www.csoonline.com/article/3619799/the-shared-responsibility-model-explained-and-what-it-means-for-cloud-security.html)
- AWS Shared Responsibility Model (https://aws.amazon.com/compliance/shared-responsibility-model/)
- Azure Shared Responsibility Model (https://docs.microsoft.com/en-us/azure/security/fundamentals/shared-responsibility)

## Pre-Hardened Infrastructure-as-Code (IaC), Policy-as-Code (PaC) and artfiacts. 

Among the push for cloud adoption, one of the most prevalent technology and paradigm shifts has been the increased use of Infrastructure-as-Code (IaC). Traditional legacy IT environments required physically setting up and configuring hardware and infrastructure through manual processes. With the advent of cloud computing and growth of IaC, organizations are now provisioning IT infrastructure through machine-readable files, which can be templatized, reusable and portable. There’s many flavors, whether you’re dealing with Cloud Service Provider (CSP) native options such as Amazon Web Services (AWS)’s CloudFormation or Microsoft Azure’s ARM templates and blueprints. That said, your choices aren’t limited to CSP-native options, and there are vendor agnostic options as well, the most popular being Terraform by HashiCorp. 

This paradigm shift hasn’t only transformed infrastructure and operations of IT environments but is also bringing many security benefits as well. Much like the manual activities of provisioning infrastructure in the days of legacy IT environments, security traditionally has handled IT security policies in a manual “paper” based fashion. This generally included articulating policies for IT systems in word and PDF documents and then going out and validating that systems were provisioned and configured in a manner that aligned with said policies. This is an incredibly tedious, cumbersome and inefficient way of approaching security. 

With the widespread adoption of IaC, we’re now seeing concurrent adoption of Policy-as-Code (PaC). PaC essentially articulates policies in code, which supports several benefits. These include guardrails for automated verification of activities, codification of organizational security policies, version control, and simply a more effective and efficient method of security policy enforcement.

Organizations such as the Hosting and Compute Office in DISA and the DoD Platform One program have created pre-hardned IaC templates which include relevant compliance requirments baked into the templates. This speeds up ATO activities and maximizes the value of reciprocity.

Below are a collection of Federal and commercial IaC and PaC resources. PaC provides support for many relevant public sector compliance frameworks, including HIPAA, NIST and more. You can now utilize pre-provided libraries of PaC policies, or create custom policies. 
 

- DoD Cloud Infrastructure-as-Code (https://www.ccpo.mil/Products/DOD-Cloud-IaC/)
- DoD Platform One Services, including IaC, Iron Bank and More (https://software.af.mil/dsop/services/)
- Open Policy Agent (https://www.openpolicyagent.org/)
- Terrascan (https://www.openpolicyagent.org/)
- Checkov (https://github.com/bridgecrewio/checkov)


## Continuous Authority to Operate (cATO)/Ongoing Authorization (OA)

cATO, as it has been called is actually the concept Ongoing Authorization. Ongoing Authorization is not new and is mentioned 90 times in NIST's 800-37 RMF Document. NIST defines OA as "that is, the continuous monitoring program is sufficiently robust and mature to provide the authorizing official with the needed information to conduct ongoing risk determination and risk acceptance activities regarding the security and privacy posture of the system and the ongoing effectiveness of the controls employed within and inherited by the system"

In the modern Software Factory environment, this generally materializes as maximizing security control inheritance through CSP's IaaS/PaaS services, building PaaS services on top of IaaS offerings to drive down the control burden on development teams/system owners. These teams get hosted in authorized platforms where control inheritance is possible. Building on the inheritance, modern CI/CD practices and technologies are used, including the integration of automated security tooling to scan new code going through pipelines to ensure the risk introduced to the system still meets the Authorizing Officials (AO)'s risk tolerance. This allows development teams to continuous deliver value (code) through pipelines to their systems residing in platforms which are accredited and hardened. This process, coupled with near real-time Continuous Monitoring helps bring the goal of OA to life. 

Many Federal systems have pursued OA and made great headway in terms of utilizing people, process and technology to bring to bear the OA or cATO concept. Some of the early pioneers include GSA's 18F/Cloud.gov, USAF's Kessel Run and Platform One, Army's Software Factory/Enterprise Cloud Management Agency (ECMA), the Space Force and Centers for Medicare and Medicaid's (CMS)'s batCAVE. 

- NIST Ongoing Authorization Slide Deck (https://csrc.nist.gov/CSRC/media/Presentations/1040-Ongoing-Authorization-Dempsey/images-media/1040%20Ongoing%20Authorization-Dempsey.pdf)
- NIST Ongoing Authorization Supplemental Guidance (https://nvlpubs.nist.gov/nistpubs/CSWP/NIST.CSWP.06032014.pdf)
- DoD DevSecOps Enterprise Strategy Guide (https://dodcio.defense.gov/Portals/0/Documents/Library/DoDEnterpriseDevSecOpsStrategyGuide.pdf)
- DSAWG cATO Brief (https://software.af.mil/wp-content/uploads/2020/11/DoD-Enterprise-DevSecOps-Initiative-DSAWG-cATO-brief-v1.0.pptx)
- DoD Platform One cATO Ask Me Anything (https://repo1.dso.mil/platform-one/bullhorn-delivery-static-assets/-/raw/master/cso/ama/2020-11-17-AMA.mp4)
- DoD Platform One Department of the Air Force-wide mandated cATO Reciprocity Memo (https://software.af.mil/wp-content/uploads/2021/01/cATO-DevSecOps-v3-signed.pdf)

## Continuous Monitoring 

Once Government systems receive an Authority to Operate (ATO), they enter a phase known as Continuous Monitoring. This defined by NIST as "Information security continuous monitoring (ISCM) is defined as maintaining ongoing awareness of information security, vulnerabilities, and threats to support organizational risk management decisions." 

This traditionally has meant that during a 3 year ATO lifecycle, the system owner(s) would take 33% of the controls and review them annually, in an attempt to "continuously" monitor 100% of the control baseline during the ATO period. This gets codified in the system owners Continuous Monitoring Plan. 

The problem with this approach is that it is far from "continuous". It is nothing more than a snapshot-in-time, showing how a subset of controls are performing during the window of assessment, which neither gives insight into the actual control compliance in a continuous fashion nor the actual deviations and concerns. 

With the introduction of Cloud-native environments, API-driven ecosystems and more, the activity of Continuous Monitoring, or "ConMon" as it is called has changed drastically. Cloud native services from hyperscale CSP's allows near real-time compliance assessment, run in an automated and continual fashion. Native services such as Azure Defender and AWS Audit Manager support the ability to scan your cloud environments and their workloads for compliance adherence to several industry frameworks, most relevant here being NIST 800-53. This changes the paradigm of Continuous Monitoring and brings it closer to reality, rather than a theatrical exercise. 

- NIST Information Security Continuous Monitoring (ISCM) for Federal Information Systems and Organizations (https://nvlpubs.nist.gov/nistpubs/legacy/sp/nistspecialpublication800-137.pdf)
- Azure Defender (https://docs.microsoft.com/en-us/azure/defender-for-cloud/regulatory-compliance-dashboard)
- AWS Audit Manager (https://aws.amazon.com/audit-manager/)

## Relevant Articles & Videos

- It's time for RegOps: Bringing DevOps to Compliance (https://www.linkedin.com/pulse/its-time-regops-bringing-devops-compliance-regscale/?trk=public_post-content_share-article)
- Dev[SecAudCom]Ops—Not Really, But Don’t Overlook Audit and Compliance as Part of Security (https://www.nextgov.com/it-modernization/2021/12/devsecaudcomopsnot-really-dont-overlook-audit-and-compliance-part-security/360024/)
- ATARC Dear Security, Compliance, and Auditors, We’re Sorry. Love, DevOps (https://www.youtube.com/watch?v=HXC0t1trNLg)
- AWS Public Sector Blog: How Booz Allen obtains C-ATO to accelerate service delivery in federal organizations using AWS (https://aws.amazon.com/blogs/publicsector/how-booz-allen-obtains-c-ato-to-accelerate-service-delivery-in-federal-organizations-using-aws/)
- Anchore: Continuous Authority to Operate: The Realities and the Myths (https://anchore.com/blog/continuous-authority-to-operate-the-realities-and-the-myths/)
- USAF Continuous ATO Playbook (https://govtribe.com/file/government-file/fa877020r0518-air-force-continuous-ato-playbook-dot-pdf)
- How DevSecOps Helps the U.S. Federal Government Achieve Continuous ATO (https://thenewstack.io/how-devsecops-helps-the-u-s-federal-government-achieve-continuous-ato/)
- Security Compass: Acheiving Rapid or Continuous ATO (https://www.securitycompass.com/sdelements/federal-us-government/free-ato-course/)
- Achieving Continuous Delivery for NIST RMF (caTO) Ongoing Authorization Continuous ATO (https://rise8.us/thoughts/continuous-delivery-for-nist-rmf-cato/)
- DoD Enterprise DevSecOps Community of Practice: Army cRMF and Platform One cATO (https://software.af.mil/wp-content/uploads/2021/06/06-23-2021-DevSecOps-CoP-Slides-Final.pdf)

## Creators

**Chris Hughes**

- <https://github.com/chughes757>

## Thanks

Special thanks goes out to all the compliance innovators that made this compilation of resources possible. From GSA/18F, Cloud.gov, Kessel Run, Platform One, Army Software Factory/Enterprise Cloud Management Agency (ECMA),CMS batCAVE and Rapid ATO, and the countless other innovative Federal programs and teams who are constantly working to make a better Government, Military and Nation for U.S. citizens. 

