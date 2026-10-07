# Architektonia Research Institute — Security Policy

**Document:** `SECURITY.md`  
**Version:** v0.1  
**Repository:** `architektonia`  
**Status:** Public  
**Function:** Public security reporting and responsible disclosure policy

---

# 1. Purpose

The Architektonia Research Institute welcomes responsible reporting of security issues that could affect its public repositories, research infrastructure, information, contributors, or institutional systems.

This document defines:

- what should be reported;
- what should not be publicly disclosed;
- how security-sensitive information should be handled;
- the general process following a report; and
- the boundary between responsible disclosure and unsafe publication.

This document intentionally does **not** describe Architektonia's internal security architecture.

```text
PUBLIC SECURITY POLICY
        ≠
INTERNAL SECURITY ARCHITECTURE
```

Security mechanisms, containment architectures, credentials, operational configurations, detailed threat models, internal vulnerabilities, defensive implementations, and security-sensitive research may be maintained through controlled institutional processes.

---

# 2. What Should Be Reported

Security concerns should be reported when they could reasonably affect the confidentiality, integrity, availability, authority, containment, or responsible operation of Architektonia systems or information.

Examples may include:

- exposed credentials or secrets;
- unauthorized access;
- authentication or authorization failures;
- unintended access to private information;
- privilege escalation;
- repository permission errors;
- security-relevant configuration errors;
- data exposure;
- vulnerabilities in Architektonia software;
- unsafe execution paths;
- containment failures;
- unauthorized external effects;
- vulnerabilities affecting research infrastructure;
- security weaknesses involving AI or automated systems;
- mechanisms capable of bypassing intended institutional controls; or
- other conditions that could materially compromise Architektonia systems, information, or participants.

When uncertain whether something is security-sensitive, contributors should prefer **private reporting over public disclosure**.

---

# 3. What Must Not Be Publicly Reported

Potentially exploitable security information should not be submitted through:

- public GitHub issues;
- public pull requests;
- public discussions;
- public comments;
- public research datasets;
- public documentation; or
- other publicly accessible channels.

This includes information such as:

- passwords;
- API keys;
- authentication tokens;
- private keys;
- credentials;
- confidential configuration values;
- exploitable vulnerabilities;
- detailed bypass techniques;
- active attack paths;
- sensitive infrastructure information;
- private endpoints;
- security-sensitive logs;
- confidential system information; or
- information that could materially facilitate unauthorized access, evasion, exploitation, or harmful external effects.

```text
IF PUBLICATION COULD
INCREASE THE SECURITY RISK
        ↓
DO NOT PUBLISH
        ↓
REPORT PRIVATELY
```

If sensitive information has already been published accidentally, avoid reproducing it further.

Report the exposure through the appropriate private channel as soon as reasonably possible.

---

# 4. Responsible Security Reporting

A useful security report should contain enough information for the issue to be understood and investigated without unnecessarily increasing the risk created by the report itself.

Where appropriate, include:

- a concise description of the issue;
- the affected repository, component, or system;
- the conditions under which the issue occurs;
- the observed behavior;
- the expected behavior;
- the potential security consequence;
- reproducible steps where safe and appropriate;
- relevant technical evidence; and
- any immediate containment concern.

Do not include secrets or unrelated confidential information merely to demonstrate that access was possible.

The governing principle is:

> **Provide enough information to investigate the vulnerability, but no more sensitive information than the investigation reasonably requires.**

---

# 5. Security Reporting Channel

Until Architektonia establishes a dedicated security reporting channel, **do not publicly disclose potentially exploitable vulnerabilities**.

If GitHub private vulnerability reporting is enabled for the affected repository, it should be preferred for repository-specific vulnerabilities.

Otherwise, potential reporters should use an explicitly designated private contact method once published by the Institute.

If no appropriate private reporting channel is available, avoid publishing exploit details publicly while seeking a safe means of contacting the Institute.

The absence of a convenient reporting mechanism does not make public disclosure of immediately exploitable information safe.

---

# 6. Security Response Process

Security reports should normally move through a process similar to:

```text
PRIVATE REPORT
      ↓
ACKNOWLEDGE
      ↓
TRIAGE
      ↓
CONTAIN
      ↓
INVESTIGATE
      ↓
REMEDIATE
      ↓
VERIFY
      ↓
DISCLOSURE DECISION
      ↓
CLOSE / MONITOR
```

The exact process may vary according to severity, uncertainty, affected systems, legal obligations, available resources, and the nature of the vulnerability.

Immediate containment may occur before complete understanding when the potential consequences justify it.

```text
PROTECT FIRST WHEN NECESSARY
        ↓
UNDERSTAND
        ↓
REMEDIATE
        ↓
LEARN
```

---

# 7. Responsible Disclosure

Architektonia supports responsible disclosure of security findings.

Responsible disclosure requires balancing:

```text
SCIENTIFIC OPENNESS
        +
PUBLIC INTEREST
        +
REPRODUCIBILITY
        +
SECURITY
        +
PROTECTION OF PEOPLE AND SYSTEMS
```

Public disclosure may be appropriate after:

- the vulnerability has been understood;
- immediate risk has been contained;
- remediation has been implemented where reasonably possible;
- affected parties have had a reasonable opportunity to respond;
- sensitive details have been removed or appropriately limited; and
- publication no longer creates disproportionate security risk.

Responsible disclosure does not require publication of every operational detail.

A vulnerability can often be documented scientifically without publishing the complete mechanism required to exploit it.

---

# 8. The Boundary of Responsible Disclosure

Architektonia distinguishes between knowledge that helps others understand a security problem and knowledge that unnecessarily increases the capability to exploit it.

```text
UNDERSTANDING
      ≠
OPERATIONAL EXPLOITABILITY
```

Where possible, public disclosure should preserve:

```text
WHAT FAILED

WHY IT MATTERS

WHAT WAS LEARNED

HOW THE CLASS OF PROBLEM
CAN BE UNDERSTOOD
```

without unnecessarily publishing:

```text
LIVE CREDENTIALS

ACTIVE ATTACK PATHS

UNREMEDIATED BYPASSES

SENSITIVE CONFIGURATIONS

OPERATIONAL EXPLOIT CHAINS

DETAILS THAT MATERIALLY
ENABLE HARMFUL REPRODUCTION
```

The objective is not secrecy for its own sake.

It is **responsible control of information whose disclosure can itself create capability**.

---

# 9. Security Research

Architektonia may conduct scientific and technical research involving:

- system security;
- AI safety;
- containment;
- authorization;
- institutional control;
- computational agents;
- human–AI systems;
- failure modes;
- adversarial conditions; and
- other security-relevant questions.

The existence of such research does not imply that all experiments, methods, vulnerabilities, source code, datasets, configurations, or results will be publicly released.

```text
SCIENTIFIC VALUE
      ≠
AUTOMATIC PUBLICATION
```

Security-sensitive research may require controlled access, delayed publication, partial publication, abstraction, redaction, or continued confidentiality.

Publication decisions should consider both scientific value and the capabilities created by disclosure.

---

# 10. AI and Autonomous Systems

Security findings involving artificial intelligence or automated agents should be reported when they reveal materially significant failures involving matters such as:

- unintended capabilities;
- unauthorized actions;
- boundary violations;
- containment failures;
- access-control failures;
- unintended external effects;
- unsafe propagation;
- manipulation of protected resources; or
- bypass of intended human or institutional authorization.

Public reports should not disclose operational details that materially increase the ability of an AI system, human operator, or automated process to reproduce an unresolved harmful pathway.

Security evaluation of advanced systems may therefore require stronger information controls than ordinary software defect reporting.

---

# 11. Good-Faith Security Research

Architektonia values good-faith efforts to identify and responsibly report security weaknesses.

Good-faith security research should seek to:

- minimize harm;
- avoid unnecessary access;
- avoid unnecessary collection of information;
- avoid persistence after sufficient evidence has been obtained;
- avoid disruption of research or institutional activities;
- protect confidential information encountered during investigation;
- report vulnerabilities responsibly; and
- allow reasonable remediation before public disclosure.

Discovery of a vulnerability does not create authorization to expand access beyond what is reasonably necessary to demonstrate the issue.

```text
DISCOVERY OF ACCESS
      ≠
AUTHORIZATION TO EXPLORE
```

Where testing could create significant risk, prior authorization should be obtained.

---

# 12. Confidentiality of Security Reports

Security reports may contain information that itself creates risk.

Access to reports should therefore be limited according to legitimate need.

```text
SECURITY INFORMATION
        ↓
NEED TO KNOW
        ↓
AUTHORIZED ACCESS
```

Security reports should not automatically become public institutional records.

Relevant scientific lessons may later be published without exposing the sensitive operational information contained in the original report.

---

# 13. No Security Through Public Obscurity

Architektonia does not assume that a system is secure merely because its design is unpublished.

Security should depend on appropriate architecture, controls, verification, monitoring, and governance.

At the same time:

```text
SECURITY SHOULD NOT
DEPEND ON SECRECY ALONE

BUT

THAT DOES NOT MEAN
EVERY SECURITY DETAIL
SHOULD BE PUBLIC
```

Confidentiality can itself be a legitimate protective boundary when information materially enables exploitation.

---

# 14. Security and Scientific Openness

Architektonia is committed to scientific openness.

Security introduces a necessary qualification:

> **Open science does not require open attack capability.**

The Institute should seek the greatest degree of scientific transparency compatible with responsible protection of people, systems, research, institutional infrastructure, and legitimate confidential information.

Where full publication would create disproportionate risk, Architektonia may publish:

- abstracted findings;
- redacted results;
- aggregated evidence;
- methodological lessons;
- vulnerability classes;
- post-remediation analyses; or
- other forms of scientific knowledge that preserve useful understanding without unnecessarily transferring harmful capability.

---

# 15. Relationship to Other Architektonia Policies

This policy should be interpreted together with:

- `README.md` — public institutional presentation;
- `CODE_OF_CONDUCT.md` — conduct within Architektonia research activities;
- `CONTRIBUTING.md` — contributor recruitment and participation;
- `LICENSING.md` — licensing and protection of intellectual and technological material; and
- repository-specific security requirements where applicable.

More sensitive environments may operate under substantially stronger internal security policies.

Those internal policies do not need to be reproduced in public repositories.

---

# 16. Evolution of This Policy

This document represents the initial public security policy of the Architektonia Research Institute.

It may evolve as the Institute develops:

- dedicated security contacts;
- private vulnerability reporting;
- incident-response procedures;
- security classification systems;
- security review processes;
- AI security research;
- responsible disclosure procedures;
- specialized security personnel; and
- more mature technical infrastructure.

Changes should be versioned and publicly traceable.

---

**Architektonia Research Institute**  
`SECURITY.md` — v0.1

> **Disclose enough to advance understanding. Protect what would unnecessarily increase the capability to cause harm.**
