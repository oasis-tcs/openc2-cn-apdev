
![OASIS Logo](https://docs.oasis-open.org/templates/OASISLogo-v3.0.png)

## OASIS Committee Note

-------

# OpenC2 Actuator Profile Development Process Version 1.0

## Committee Note 01

## 03 July 2023

&nbsp;

#### This stage:
https://docs.oasis-open.org/openc2/cn-appdev/v1.0/cn01/cn-appdev-v1.0-cn01.md (Authoritative) \
https://docs.oasis-open.org/openc2/cn-appdev/v1.0/cn01/cn-appdev-v1.0-cn01.html \
https://docs.oasis-open.org/openc2/cn-appdev/v1.0/cn01/cn-appdev-v1.0-cn01.pdf

#### Previous stage:
N/A

#### Latest stage:
https://docs.oasis-open.org/openc2/cn-appdev/v1.0/cn-appdev-v1.0.md (Authoritative) \
https://docs.oasis-open.org/openc2/cn-appdev/v1.0/cn-appdev-v1.0.html \
https://docs.oasis-open.org/openc2/cn-appdev/v1.0/cn-appdev-v1.0.pdf

#### Technical Committee:
[OASIS Open Command and Control (OpenC2) TC](https://www.oasis-open.org/committees/openc2/)

#### Chairs:
Duncan Sparrell (duncan@sfractal.com), [sFractal Consulting LLC](https://www.sfractal.com/) \
Michael Rosa (mjrosa@nsa.gov), [National Security Agency](https://www.nsa.gov/)

#### Editors:
David Lemire (david.lemire@hii-tsd.com), [National Security Agency](http://www.nsa.gov/) \
David Kemp (d.kemp@cyber.nsa.gov), [National Security Agency](https://www.nsa.gov/)

#### Related work:
This document is related to:
* Related specifications (include hyperlink, preferably to HTML format) \
`(remove "Related work" section if no entries)`

#### Abstract:
Open Command and Control (OpenC2) is a concise and extensible language to enable machine-to-machine communications for purposes of command and control of cyber defense components in a manner that is agnostic of the underlying products, technologies, transport mechanisms or other aspects of the implementation. OpenC2 Actuator Profiles (APs) specify the subset of the OpenC2 language relevant in the context of specific actuator functions. A profile refines the meaning of language elements used to perform the actuator function, and often defines additional elements that are relevant and/or unique to that function. This Committee Note describes the TC’s process for using the JSON Abstract Data Notation (JADN) information modeling language in the development of APs, resulting in a rigorous schema for an AP properly integrated with the base OpenC2 language.

#### Status:
This is a Non-Standards Track Work Product. The patent provisions of the OASIS IPR Policy do not apply.

This document was last revised or approved by the OASIS Open Command and Control (OpenC2) TC on the above date. The level of approval is also listed above. Check the "Latest stage" location noted above for possible later revisions of this document. Any other numbered Versions and other technical work produced by the Technical Committee (TC) are listed at https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=openc2#technical.

TC members should send comments on this document to the TC's email list. Others should send comments to the TC's public comment list, after subscribing to it by following the instructions at the "Send A Comment" button on the TC's web page at https://www.oasis-open.org/committees/openc2/.
#### Citation format:
When referencing this document the following citation format should be used:

**[AP-Dev-v1.0]**

_OpenC2 Actuator Profile Development Process Version 1.0_. Edited by David Lemire and David Kemp. 03 July 2023. OASIS Committee Note 01. https://docs.oasis-open.org/openc2/cn-appdev/v1.0/cn01/cn-appdev-v1.0-cn01.html. Latest stage: https://docs.oasis-open.org/openc2/cn-appdev/v1.0/cn-appdev-v1.0.html.

#### Notices
Copyright &copy; OASIS Open 2023. All Rights Reserved.

Distributed under the terms of the OASIS [IPR Policy](https://www.oasis-open.org/policies-guidelines/ipr/).

The name "OASIS" is a trademark of [OASIS](https://www.oasis-open.org/), the owner and developer of this specification, and should be used only to refer to the organization and its official outputs.

For complete copyright information please see the full Notices section in an Appendix below.

-------

# Table of Contents
[[TOC will be inserted here]]

-------

<!-- Insert a "line rule" (three or more hyphens alone on a new line, following a blank line) before each major section. This is used to generate a page break in the PDF format. -->

# 1 Introduction

_This document is non-normative in its entirety._

## 1.1 Purpose

> briefly summarize the purpose of this CN

## 1.2 Glossary

<!-- Optional section with suggested subsections -->

### 1.2.1 Definitions of terms

### 1.2.2 Acronyms and abbreviations

### 1.2.3 Document conventions

- Naming conventions
- Font colors and styles
- Typographic conventions

## 1.3 Background

### 1.3.1 Open Command and Control (OpenC2)

### 1.3.2 JSON Abstract Data Notation (JADN)

### 1.3.3 OpenC2 Actuator Profiles

-------

# 2 AP Development Process Overview

> introductory words

## 2.1 Process Steps

> Note: inital draft graphic, to be refined as document develops

##### **Figure 2-1:  Actuator Profile Development Process**
![Figure 2-1: AP Development Process](images/CN-AP-Dev-Overview.drawio.png)

 1. AP Develompent Initiation
 1. Develop Use Cases
 1. Develop Example Messages
 1. Develop JADN Schema
 1. Link JADN Schema
 1. Create Property Tables
 1. Insert Property Tables
 1. Develop Specification Text
 1. Interate To Completion
 1. Develop Final Example Messages from JADN Schema
 1. Define Conformance Requirements
 1. Review, Approval, and Publication


## 2.2 AP Specification Structure

 * Body
   * sections
 * Annex(es)
 * Appendices
 * Associated schema files

-------

# 3 AP Development Process Walkthrough

## 3.1 AP Develompent Initiation

## 3.2 Develop Use Cases

## 3.3 Develop Example Messages

## 3.4 Develop JADN Schema

## 3.5 Link JADN Schema

## 3.6 Create Property Tables

## 3.7 Insert Property Tables

## 3.8 Develop Specification Text

## 3.9 Interate To Completion

## 3.10 Develop Final Example Messages from JADN Schema

## 3.11 Define Conformance Requirements

## 3.12 Review, Approval, and Publication


-------

# Appendix A. Informative References

 * OpenC2 Architecture
 * OpenC2 Language Spec
 * JADN Spec
 * Information Modeling with JADN CN
 * OASIS Work Product Process Documentation

<!-- Required section -->

This appendix contains the informative references that are used in this document.

While any hyperlinks included in this appendix were valid at the time of publication, OASIS cannot guarantee their long-term validity.

(Reference sources:
For references to IETF RFCs, use the approved citation formats at: \
https://docs.oasis-open.org/templates/ietf-rfc-list/ietf-rfc-list.html. \
For references to W3C Recommendations, use the approved citation formats at: \
https://docs.oasis-open.org/templates/w3c-recommendations-list/w3c-recommendations-list.html. \
Remove this note before submitting for publication.)

###### [OpenC2-HTTPS-v1.0]
_Specification for Transfer of OpenC2 Messages via HTTPS Version 1.0_. Edited by David Lemire. Latest stage: http://docs.oasis-open.org/openc2/open-impl-https/v1.0/open-impl-https-v1.0.html
###### [OpenC2-SLPF-v1.0]
_Open Command and Control (OpenC2) Profile for Stateless Packet Filtering Version 1.0_. Edited by Joe Brule, Duncan Sparrell, and Alex Everett. Latest stage: http://docs.oasis-open.org/openc2/oc2slpf/v1.0/oc2slpf-v1.0.html

-------

# Appendix B. Acknowledgments

(Note: A Work Product approved by the TC must include a list of people who participated in the development of the Work Product. This is generally done by collecting the list of names in this appendix. This list shall be initially compiled by the Chair, and any Member of the TC may add or remove their names from the list by request.  
Remove this note before submitting for publication.)

## B.1 Special Thanks

<!-- This is an optional subsection to call out contributions from TC members. If a TC wants to thank non-TC members then they should avoid using the term "contribution" and instead thank them for their "expertise" or "assistance". -->

Substantial contributions to this document from the following individuals are gratefully acknowledged:

Participant Name, Affiliation or "Individual Member"

## B.2 Participants

<!-- A TC can determine who they list here, however, TC Observers must not be listed. It is common practice for TCs to list everyone that was part of the TC during the creation of the document, but this is ultimately a TC decision on who they want to list and not list, and in what order. -->

The following individuals have participated in the creation of this document and are gratefully acknowledged:

** OASIS Open Command and Control (OpenC2) TC Members:**

| First Name | Last Name | Company |
| :--- | :--- | :--- |
Philippe | Alcon | Marvelous Networks
Alex | Amir | Viacat
Kris | Anders | Trend Mission
Darren | Anysteel | Macro Networks

-------

# Appendix C. Revision History
| Revision | Date | Editor | Changes Made |
| :--- | :--- | :--- | :--- |
| filename-v1.0-wd01 | yyyy-mm-dd | Editor Name | Initial working draft |

------

# Appendix D. Notices

Copyright &copy; OASIS Open 2023. All Rights Reserved.

All capitalized terms in the following text have the meanings assigned to them in the OASIS Intellectual Property Rights Policy (the "OASIS IPR Policy"). The full [Policy](https://www.oasis-open.org/policies-guidelines/ipr/) may be found at the OASIS website.

This document and translations of it may be copied and furnished to others, and derivative works that comment on or otherwise explain it or assist in its implementation may be prepared, copied, published, and distributed, in whole or in part, without restriction of any kind, provided that the above copyright notice and this section are included on all such copies and derivative works. However, this document itself may not be modified in any way, including by removing the copyright notice or references to OASIS, except as needed for the purpose of developing any document or deliverable produced by an OASIS Technical Committee (in which case the rules applicable to copyrights, as set forth in the OASIS IPR Policy, must be followed) or as required to translate it into languages other than English.

The limited permissions granted above are perpetual and will not be revoked by OASIS or its successors or assigns.

This document and the information contained herein is provided on an "AS IS" basis and OASIS DISCLAIMS ALL WARRANTIES, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO ANY WARRANTY THAT THE USE OF THE INFORMATION HEREIN WILL NOT INFRINGE ANY OWNERSHIP RIGHTS OR ANY IMPLIED WARRANTIES OF MERCHANTABILITY OR FITNESS FOR A PARTICULAR PURPOSE.

The name "OASIS" is a trademark of [OASIS](https://www.oasis-open.org/), the owner and developer of this specification, and should be used only to refer to the organization and its official outputs. OASIS welcomes reference to, and implementation and use of, specifications, while reserving the right to enforce its marks against misleading uses. Please see https://www.oasis-open.org/policies-guidelines/trademark/ for above guidance.
