# Security Incident Report: CLD-IR-0001

| | |
|---|---|
| **Report ID** | CLD-IR-0001 |
| **Related ticket** | CLD-0001 Suspicious sign-in activity: daniel.reeve@cloudora.io |
| **Report title** | CEO account takeover via password spray |
| **Analyst** | Radosław Huppert |
| **Date of report (UTC)** | 10-08-2026 |
| **Incident severity** | P1 - Executive account, active enterprise deal |
| **Status** | Open / Contained / Eradicated / Closed |
| **Classification** | This is training copy of fictional company named Cloudora (MyFirstHack scenario) |

---

## 1. Executive summary

> Four to five sentences a non-technical executive can read in 60 seconds: what happened, how it was found, what the attacker did, what has been done about it, and what the business risk was.
>
> No IP addresses, no query syntax, no acronyms without expansion.
>
> **Write this section LAST, after everything else is filled in.**

<!-- Write the executive summary here. -->

---

## 2. Incident timeline


| Time (UTC) | Source | Event |
|---|---|---|
| 8-8-2026 00-05 AM | Sign in | First attempt of password spray from 102.89.x.x IP (Lagos Nigeria) failed 44 logins | 
| 9-8-2026 00-05 AM | Sign in | Second attempt of password spray from 102.89.x.x IP (Lagos Nigeria) failed 36 logins | 
| 10-8-2026 00-05 AM | Sign in | Third attempt of password spray from 102.89.x.x IP (Lagos Nigeria) failed 34 logins | 
| 10-8-2026 3:12:05 AM | Sign in | Successful login from 102.89.44.17 IP into daniel.reeve@cloudora.io account, Windows 10, Chrome 125, initial access mitre: T1078 | 
| 10-8-2026 3:14:30 AM | Sign in | daniel.reeve@cloudora.io opened Outlook Web  | 
| 10-8-2026 3:18:44 AM | Audit | Attacker added own authenticator app on device 'Pixel 6' T1098.005  | 
| 10-8-2026 3:26:02 AM | Sign in | daniel.reeve@cloudora.io opened Azure Portal  | 
| 10-8-2026 3:31:09 AM | Audit | Attacker added new inbox rule which is hiding new emails from finance@cloudora.io or containing 'invoice' T1564.008  | 
| 10-8-2026 3:47:18 AM | Sign in | Successful login from 102.89.45.101 IP into priya.nair@cloudora.io account, Windows 10, Chrome 125, initial access mitre: T1078 | 
| 10-8-2026 3:52:40 AM | Sign in | priya.nair@cloudora.io opened SharePoint Online |
| 10-8-2026 8:41:00 AM | Sign in | Successful login from 203.0.113.11 (London) IP into daniel.reeve@cloudora.io account. Usual IP address and Location |
| 10-8-2026 8:55:00 AM | IT alert | Cloudora IT admin flagged unusual logins from Lagos, Nigeria into daniel.reeve@cloudora.io account | 


---

## 3. Findings


### Finding 1 Password spray before accessing daniel.reeve@cloudora.io account

**Finding:**  
Searching through login attempts there was a password spray attack which has started on august 8th. First night there was 44 failed login attempts(50126), Second night there was 36 failed login attempts(50126) and third night 
there was 34 failed login attempts(50126) and also 2 successful logins into daniel.reeve@cloudora.io account and priya.nair@cloudora.io account.

**Evidence:**  
<!-- Identify the query, log source, relevant rows, screenshots, or other evidence. -->

**Why it matters:**  
This matters because there could be more accounts in the future which can be potential victims. 

---

### Finding 2 Suspicious new device registration on MFA platform 

**Finding:**  
Attacker after successful login into daniel account established persistence through adding device named 'Pixel 6' into MFA application.  

**Evidence:**  
<!-- Identify the query, log source, relevant rows, screenshots, or other evidence. -->

**Why it matters:**  
Rese

---

### Finding 3

**Finding:**  
<!-- State the established fact in one sentence. -->

**Evidence:**  
<!-- Identify the query, log source, relevant rows, screenshots, or other evidence. -->

**Why it matters:**  
<!-- Explain why this finding matters. -->

---

### Finding 4

**Finding:**  
<!-- State the established fact in one sentence. -->

**Evidence:**  
<!-- Identify the query, log source, relevant rows, screenshots, or other evidence. -->

**Why it matters:**  
<!-- Explain why this finding matters. -->

---

## 4. Indicators of compromise (IOCs)

> Everything another analyst would need to detect or block this attacker: IP addresses, device names, rule names, user agents. One row per indicator, with where you found it.

| Type | Value | First seen (UTC) | Context |
|---|---|---|---|
| | | | |
| | | | |
| | | | |
| | | | |
| | | | |

<!-- Add more rows as needed. -->

---

## 5. MITRE ATT&CK mapping

> Map each attacker behaviour you observed to a technique. Use the technique ID and name, and point to the finding that evidences it. Only map what you actually saw in the logs.

| Tactic | Technique ID | Technique name | Evidenced by |
|---|---|---|---|
| | | | |
| | | | |
| | | | |
| | | | |

---

## 6. Scope

> Who and what was affected. List:
>
> (a) accounts confirmed compromised,  
> (b) accounts targeted but not breached,  
> (c) accounts investigated and cleared (false positives),  
>
> with the evidence for each. If you have not checked scope, the incident is not scoped - say so explicitly.

### Accounts confirmed compromised

<!-- List accounts confirmed compromised and the evidence supporting each one. -->

- 

### Accounts targeted but not breached

<!-- List accounts targeted but not breached and the evidence supporting each one. -->

- 

### Accounts investigated and cleared (false positives)

<!-- List investigated accounts determined not to be compromised and the evidence supporting each one. -->

- 

---

## 7. Actions taken

> What was actually done, by whom, at what time (UTC), in order. Containment first (stop the bleeding), then eradication (remove attacker access and persistence), then verification (prove it worked). An action without a timestamp did not happen.

| Time (UTC) | Action | Performed by | Verified how |
|---|---|---|---|
| | | | |
| | | | |
| | | | |
| | | | |
| | | | |

<!-- Add more rows as needed. -->

---

## 8. Recommendations

> What the client should change so this attack fails next time. Be specific and prioritised: quick wins first, then strategic changes. Every recommendation should trace back to a finding.

1. 
2. 
3. 
4. 

---

## 9. Lessons learned

> What worked in this investigation, what was slow or missing, and what the SOC should do differently. This section is about the response, not the attacker.

### What worked

- 
- 

### What was slow or missing

- 
- 

### What the SOC should do differently

- 
- 

---

> **Template notes:** Keep all times UTC; write findings as you work, not at the end; the executive summary is written last but appears first.
