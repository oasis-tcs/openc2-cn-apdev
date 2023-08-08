
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

This OASIS Committee Note (CN) describes a process for developing
OpenC2 Actuator Profiles (APs), including the use of the JSON
Abstract Data Notation (JADN) information modeling language in
the development of APs. The process described here results in an
AP design and specification that aligns to the relevent use cases
and an associated rigorous JADN schema that binds the AP to the
OpenC2 language.

## 1.2 Glossary

<!-- Optional section with suggested subsections -->

### 1.2.1 Definitions of terms

-   **Action**: The task or activity to be performed (e.g.,
    'deny').

-   **Actuator**: The Consumer that executes the Command.

-   **Actuator Profile**: The document that defines a category of
    operations performed by an Actuator (e.g., 'Stateless Packet
    Filtering').

-   **Argument**: A property of a Command that provides
    additional information on how to perform the Command, such as
    date/time, periodicity, duration, etc.

-   **Command**: A Message defined by an Action-Target pair that
    is sent from a Producer and received by a Consumer.

-   **Consumer**: A managed device / application that receives
    Commands. Note that a single device / application can have
    both Consumer and Producer capabilities.

-   **Information Modeling**: A process to understand and
    document the essential information content relevant to a
    system, application, or protocol exchange without regard to
    how that information is represented in actual
    implementations.

-   **Message**: A content- and transport-independent set of
    elements conveyed between Consumers and Producers.

-   **Producer**: A manager application that sends Commands.

-   **Request**: A Message from a Producer to a Consumer used to
    convey a Command.

-   **Response**: A Message from a Consumer to a Producer
    acknowledging a Command or returning the requested resources
    or status to a previously received Command.

-   **Specifier**: A property or field that identifies a Target
    to some level of precision.

-   **Target**: The object of the Action, i.e., the Action is
    performed on the Target (e.g., IP Address).

### 1.2.2 Acronyms and abbreviations

| Acronym | Description |
|:-------:|--------------|
| AP      | Actuator Profile |
| IM      | Information Modeling
| JADN    | JSON Object Data Notation |
| JSON    | JavaScript Object Notation |
| LS      | Language Specification | 
| OASIS   | Organization for the Advancement of Structured Information Standards |
| OpenC2  | Open Command and Control |
| TC      | Technical Committee |
| UML     | Unified Modeling Language |

### 1.2.3 Document conventions

- Naming conventions
- Font colors and styles
- Typographic conventions

## 1.3 Background

This section provides background information on OpenC2, JADN, and
the role of actuator profiles (APs) to provide a context for the
process described in sections 2 and 3.

### 1.3.1 Open Command and Control (OpenC2)

OpenC2 is a suite of specifications that enables command and
control of cyber defense systems and components. OpenC2 typically
uses a request-response paradigm where a _Command_ is encoded by
a _Producer_ (managing application) and transferred to a
_Consumer_ (managed device or virtualized function) using a
secure transfer protocol, and the Consumer can respond with
status and any requested information. This request / response
paradigm is illustrated in Figure 1-1.

##### Figure 1-1: OpenC2 Request / Response Paradigm
![Figure 1-1: OpenC2 Request / Response
Paradigm](images/MessageFlow.png)

OpenC2 allows the application producing the commands to discover
the set of capabilities supported by the managed devices (i.e.,
an introspection capability). This capability permits the
managing application to adjust its behavior to take advantage of
the features exposed by the managed device. The capability
definitions can be easily extended in a noncentralized manner,
allowing standard and non-standard capabilities to be defined
with semantic and syntactic rigor.

> NOTE: add reference links to the following

OpenC2's approach to automating cybersecurity command and control
is described in the *OpenC2 Architecture Specification*. The
specifics of the OpenC2 language are defined in the 
*OpenC2 Language Specification*.

### 1.3.2 JSON Abstract Data Notation (JADN)

JSON Abstract Data Notation (JADN) is a UML-based information
modeling language that defines data structure independently of
data format. Information models are used to define and generate
physical data models, validate information instances, and enable
lossless translation across data formats. A JADN specification
consists of two parts: type definitions that comprise the
information model, and serialization rules that define how
information instances are represented as data. The information
model is itself an information instance that can be serialized
and transferred between applications. The model is documented
using a compact and expressive interface definition language,
property tables, or entity relationship diagrams, easing
integration with existing design processes and architecture
tools.

> NOTE: add reference links to the following

The OpenC2 TC has published a *JADN Ppecification*, and a
companion CN describing the use of JADN in Information Modeling
(IM).

### 1.3.3 OpenC2 Actuator Profiles

As described in the *OpenC2 Architecture Specification*, APs
serve the purpose of scoping the general purpose OpenC2 language
to the C2 of a particular cyberdefense function:  

> OpenC2 Actuator Profiles specify the subset of the OpenC2
> language relevant in the context of specific actuator
> functions. Cyber defense components, devices, systems and/or
> instances may (in fact are likely to) implement multiple
> profiles. A profile refines the meaning of language elements
> (actions, targets, command arguments, results) used to perform
> the actuator function, and often defines additional elements
> that are relevant and/or unique to that function.

The goal of this CN is to document a well-formed approach to
developing APs that takes advantage of the rigor provided by
applying JADN information modeling to the process.

-------

# 2 AP Development Process Overview

> introductory words

## 2.1 Process Steps

Figure 2-1 illustrates a process for the development of an Actuator Profile (AP)
based on defining use cases, prototopying messages, and formalizing that
material in a JADN information model. The process assumes a degree of iteration
toward completion and its execution does not need to be strictly linear.

> Note: inital draft graphic, to be refined as document develops

##### **Figure 2-1:  Actuator Profile Development Process**
![Figure 2-1: AP Development Process](images/CN-AP-Dev-Overview.drawio.png)

 1. **AP Development Initiation:** Identify the need, define the scope, receive
    TC approval, request a starter document, establish a work environment.
 2. **Develop AP Content:** a development loop for creating the AP,
 
    A) **Develop Use Cases:** Identify use case(s) for control of cyber defense
       function for the AP.

    B) **Develop Example Messages:** Develop example messages to implement the
       defined use case(s), and capture in an Examples appendix.
    
    C) **Develop JADN Schema:** Develop the JADN information model specifying
       the types needed to create and validate the example messages.
    
    D) **Link JADN Schema:**  Link to the JADN schema file(s) from Annex A.

    E) **Create Property Tables:** Use JADN tooling to generate property tables
       from the JADN schema.

    F) **Insert Property Tables and Associated Text:** Add the property tables
       for the schema to the body of the AP specification, and develop
       corresponding text content.
 3. **Interate To Completion:** As the AP matures the initial use case(s) can be
    refined and additional use cases can be defined and integrated as described
    in Step 2.
 4.  **Develop Final Example Messages from JADN Schema:** The example message
     content included in the AP should be finalized based on the JADN schema to
     ensure the messages are valid and conform to the schema.
 5.  **Define Conformance Requirements:** All OASIS specifications are required
     to include [conformance requirements](https://docs.oasis-open.org/templates/TCHandbook/ConformanceGuidelines.html). 
 6.  **Review, Approval, and Publication:** All OASIS specifications are
     required to follow the standard approval process, including [public
     review](https://www.oasis-open.org/policies-guidelines/tc-process-2017-05-26/#publicReview)
     prior to [final TC
     approval](https://www.oasis-open.org/policies-guidelines/tc-process-2017-05-26/#committeeSpec).


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
