---
title: Examples
weight: 5
---

#### Mobile Phone Spoofing

Consider a malicious mobile application that includes behaviors to determine which financial applications are installed on the mobile device, provide spoofed inputs to perform actions on behalf of the user, and capture the screen content. The application then uses those capabilities to deploy a smart contract that drains funds into the attacker’s wallets on the digital asset platform, which are then exfiltrated by using layering to launder the funds. The following ATT&CK and AADAPT techniques can be applied to describe such behaviors: 

1. (ATT&CK) T1418: Software Discovery – Discovers the presence of digital asset and finance-related applications that use smart contracts.
2. (ATT&CK) T1516: Input Injection – Performs actions on behalf of the user of the mobile device. 
3. (ATT&CK) T1513: Screen Capture – Captures the screen along with sensitive information on crypto wallets such as private keys and wallet addresses. 
4. (AADAPT) ADT3012.002: Exploit Smart Contract Implementation: Evil Contract – Signs a malicious smart contract that transfers funds from the victim’s accounts into the attacker’s accounts. 
5. (AADAPT) ADT3028.003: Siphon Funds: Layering – Sends portions of the stolen funds from the attacker’s wallets to various mixers and loosely regulated exchanges, making it hard to trace.  

The above example shows how techniques from AADAPT and ATT&CK can be used together to comprehensively describe attacks and adversary behaviors on digital asset systems.

#### Bybit Hack

In February 2025, ByBit, a major centralized cryptocurrency exchange (CEX), suffered the largest crypto hack to date, resulting in the loss of approximately $1.5 billion in Ethereum tokens. The attack was executed through a sophisticated manipulation of the exchange’s multi-signature wallet smart contract. Attackers crafted a malicious transaction that altered the wallet’s logic, enabling them to seize control of its assets. 

To conceal their actions, the hackers presented a masked user interface to the wallet signers, making it appear as though they were authorizing a routine transfer from a cold wallet to a hot wallet. In reality, the transaction directed funds to a malicious address. This deception allowed the attackers to transfer ownership of the wallet to themselves and subsequently drain its contents. The consequences of the hack were severe, not only in terms of financial loss but also in undermining trust in centralized exchanges and highlighting vulnerabilities in multi-signature wallet implementations. The following ATT&CK and AADAPT techniques can be applied to describe such behaviors. For brevity, we have delineated only a subset of the techniques that we believe were used: 

1. (AADAPT) ADT3029 Smart Contract Implementation Analysis – Analyzes smart contract implementations to identify any vulnerabilities. 
2. (ATT&CK) T1584 Compromise Infrastructure – Compromises a developer machine. 
3. (AADAPT) ADT3001 Acquire Accounts – Obtains control over valid system accounts to facilitate siphoning stolen funds. 
4. (ATT&CK) T1195.002 Compromise Software Supply Chain – Injects malicious code into digital wallet system UI using the compromised machine. 
5. (ATT&CK) T1036 Masquerading – Passes the tampered transaction to signers while appearing as a routine benign transfer of funds. 
6. (AADAPT) ADT3028.003 Siphon Funds: Layering – Siphons stolen funds into small batches, before swapping and redistributing the tokens across multiple accounts. 
7. (AADAPT) ADT3005 Cross Chain Swaps (Hopping) – Uses several DeFi platforms and blockchain services to exchange the stolen funds.



© 2025 THE MITRE CORPORATION. ALL RIGHTS RESERVED. APPROVED FOR PUBLIC RELEASE. DISTRIBUTION UNLIMITED. PUBLIC RELEASE CASE NUMBER 25-2215