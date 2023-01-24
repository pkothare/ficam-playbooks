---
layout: page
collection: playbooks
title: Phishing-Resistant Authenticators
pubdate: 2022-12
date: December 30, 2022
type: Markdown
permalink: /playbooks/phish/
description: The Phishing-Resistant Authenticator Playbook help agencies understand what are and how to use phishing-resistant authenticators from OMB Memo 22-09.
sticky_sidenav: true
sidenav: phish

subnav:
  - text: Executive Summary
    href: '#executive-summary'
  - text: Federal Zero Trust Strategy
    href: '#federal-zero-trust-strategy'
  - text: What is Phishing-Resistant?
    href: '#what-is-phishing-resistant'
---

Version 1.0<br>
December xx, 2022

<img src="{{site.baseurl}}/assets/img/logo-gsa.png" width="64" height='64' align="left" alt="U.S. General Services Administration Logo">
<img src="{{site.baseurl}}/assets/img/logo-cio.png" width="64" height='64' align="left" alt="U.S. Federal Chief Information Officer Council Logo">
<img src="{{site.baseurl}}/assets/img/logo-cisa.png" width="64" height='64' align="left" alt="U.S. Department of Homeland Security Cybersecurity and Infrastructure Security Agency Logo"><br><br><br>

This playbook is a collaboration among the General Services Administration Office of Government-wide Policy Identity Assurance and Trusted Access Division, Federal Chief Information Security Officer Council ICAM Subcommittee, and the Department of Homeland Security (DHS) Cybersecurity and Infrastructure Security Agency (CISA).

# Executive Summary



# Playbook Purpose
Agencies that are in “wait and see” mode with their own FICAM implementations may learn from the successes and challenges of early adopter agencies who participate in playbook development. Playbooks are intended to be a “living document,” the playbook will be a resource to federal agencies to capture the lessons learned from early adopters and to provide a reference for standards-based digital identity best practices as lessons learned and standards continue to evolve.

# Federal Zero Trust Strategy

## OMB Memo 22-09
*Moving the U.S. Government Toward Zero Trust*

The goal of this strategy is to make bold changes to accelerate agencies toward a **shared baseline of early zero trust maturity.** 

Moving to a zero trust architecture will be a multi-year journey for agencies.

The Federal Government will learn and adjust as new technologies and practices emerge.
This strategy places significant emphasis on **stronger enterprise identity** and **access controls**, including phishing-resistant, multi-factor authentication.

## Why the policy change?
*Holistic authenticator strategy*

![Policy Flow Chart](https://cdn720.s3.amazonaws.com/gsa/flowchart.png)

# Phishing-resistant Authenticators

## What is Phishing?
![Phishing](https://cdn720.s3.amazonaws.com/gsa/phishing-link.png)
User clicks on phishing link for fraudulent website. Inputs username and password and SMS or App One Time PIN. 
![Password Hash Icon](https://cdn720.s3.amazonaws.com/gsa/creds-icon.png)
Adversary replays credentials and MFA to authentic website.
![Credential Icons](https://cdn720.s3.amazonaws.com/gsa/pass-hash-icon.png)
Adversary steals user data or performs discovery and lateral movement.

## What is MFA?
![Something you have icon](https://cdn720.s3.amazonaws.com/gsa/something-you-have.png)
Something you have
AND
![Something you are icon](https://cdn720.s3.amazonaws.com/gsa/something-you-are.png)
Something you are
OR
![Something you know icon](https://cdn720.s3.amazonaws.com/gsa/something-you-know.png)
Something you know
## What is Phishing-resistant?
| Phishable | Phishing Resistant* |  |
|--|--|--|
|Single Factor  | Multi-factor (MFA) |
|Username / Password  | Push Notification One Time Pin SMS PIN |
|Username / Password  | Push Notification <br>One Time Pin <br>SMS  PIN | Public Key Infrastructure <br>PIV Card <br>**Fast ID Online (FIDO)**
|Weakest  | &#8594; | Strongest


![USB](https://cdn720.s3.amazonaws.com/gsa/usb-picture.jpg)
*Key characteristic of phishing-resistant authenticators is they use out of band identifiers like public key cryptography (asymmetric public-private) key pairs.

![USB](https://cdn720.s3.amazonaws.com/gsa/phishing-resistant.png)

## What is the FIDO Alliance?
*Fast Identity Online (FIDO)*

 - An industry association of technology vendors.
 - Publishes MFA standards, certifies vendor products and new professional
   certification program.

| FIDO 1.0 (Dec 2014) | FIDO 2.0 (FIDO2) (Apr 2018) |
|--|--|
| Universal Two Factor (U2F) - Standard spec for physical FIDO security key using USB, NFC, or Bluetooth on supported browsers and OS. | Client to Authenticator Protocol (CTAP) 2 - Added mobile device support for passwordless using WebAuthN. |
|Universal Two Factor (U2F) - Standard spec for physical FIDO security key using USB, NFC, or Bluetooth on supported browsers and OS.| Web Authentication (WebAuthN) - W3C standard for set of web APIs to allow FIDO UAF/CTAP2 authentication in/to browsers from platforms/devices.|

## What is a FIDO token?
*Platform and Roaming Authenticators*
We see “Bound” Authenticators
![“Bound” Authenticators](https://cdn720.s3.amazonaws.com/gsa/bound-auth.png)
(authenticators that are an integral part of a smartphone or laptop)

We see “Roaming” Authenticators
![“Roaming” Authenticators](https://cdn720.s3.amazonaws.com/gsa/roaming-auth.png)
(authenticators that can be connected to different smartphones/laptops using CTAP)
**In both categories you find support for different modalities**
![User Presence Challenge](https://cdn720.s3.amazonaws.com/gsa/modalities.png)
User Presence Challenge (“A” user)
![User Verification Methods](https://cdn720.s3.amazonaws.com/gsa/verficiation.png)
User Verification Methods (“THE” user)

## OMB Memo 22-09
*Moving the U.S. Government Toward Zero Trust*

 - OMB Memo 22-09 allows the use a FIDO2 authenticator when a PIV or
   Derived PIV is impractical.
 - FIPS and FIDO2.
 - Native support in cloud platforms and modern devices.

I can revoke certificates and this doesn’t use certificates. How do I revoke it? Remove the binding between between the authenticator and the identity record.

ICAM@GSA.gov for questions.

# Use Cases
*Where should I use Phishing-resistant?*

 1. Alternative Authenticator - When PIV, PKI, and Derived PIV is impractical, use a phishing-resistant alternative such as FIDO2 and WebAuthN.
 2. Back-up Authenticator - Agencies shouldn’t allow a U/P or non-phishing resistant policy exception while an employee waits for a PIV smart card.
 3. Ineligible PIV Population - This includes temporary workers, short-term staff, and any other type of worker that falls outside the scope of PIV.
 4. Technology Doesn’t Support PKI - Cloud and mobile authentication do not natively support PKI. Use platform authenticators.
 5. Mission application for public users - Agencies should allow the use of phishing-resistant on mission applications.
## Why FIDO2 in 22-09?
*What’s wrong with PIV?*
![FIDO2](https://cdn720.s3.amazonaws.com/gsa/fido2.png)
## PKC vs PKI
![PKC vs PKI](https://cdn720.s3.amazonaws.com/gsa/pkc-vs-pki.png)

## Register (Bind) an Authenticator

![Register (Bind) an Authenticator](https://cdn720.s3.amazonaws.com/gsa/ra-1.png)
![Register (Bind) an Authenticator](https://cdn720.s3.amazonaws.com/gsa/ra-2.png)
![Register (Bind) an Authenticator](https://cdn720.s3.amazonaws.com/gsa/ra-3.png)
