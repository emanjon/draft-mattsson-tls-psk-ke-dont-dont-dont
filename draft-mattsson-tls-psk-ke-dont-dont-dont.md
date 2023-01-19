---
title: "NULL Encryption and Key Exchange Without Forward Secrecy are Dicouraged"
abbrev: "NULL and psk_ke don't don't don't"
category: std

docname: draft-mattsson-tls-psk-ke-dont-dont-dont-latest
submissiontype: IETF  # also: "independent", "IAB", or "IRTF"
number:
date:
consensus: true
v: 3
area: "Security"
workgroup: "Transport Layer Security"
keyword:
 - next generation
 - unicorn
 - sparkling distributed ledger
venue:
  group: "Transport Layer Security"
  type: "Working Group"
  mail: "tls@ietf.org"
  arch: "https://mailarchive.ietf.org/arch/browse/tls/"
  github: "emanjon/draft-mattsson-tls-psk-ke-dont-dont-dont"
  latest: "https://emanjon.github.io/draft-mattsson-tls-psk-ke-dont-dont-dont/draft-mattsson-tls-psk-ke-dont-dont-dont.html"

author:
- initials: J.
  surname: Preuß Mattsson
  name: John Preuß Mattsson
  org: Ericsson AB
  abbrev: Ericsson
  street: SE-164 80 Stockholm
  country: Sweden
  email: john.mattsson@ericsson.com

normative:
  RFC2119:
  RFC8174:
  RFC8446:
  RFC9113:
  RFC9147:
  I-D.ietf-tls-deprecate-obsolete-kex:
  I-D.ietf-tls-rfc8447bis:

informative:
  RFC5288:
  RFC7258:
  RFC7624:
  RFC7748:
  RFC8017:
  RFC8447:
  RFC9001:
  RFC9150:
  RFC9151:
  RFC9257:
  I-D.ietf-emu-aka-pfs:
  I-D.ietf-tls-rfc8446bis:
  I-D.irtf-cfrg-aegis-aead:

  Akhmetzyanova:
    target: https://eprint.iacr.org/2019/421.pdf
    title: "Continuing to reflect on TLS 1.3 with external PSK"
    author:
      -
        ins: L. Akhmetzyanova
      -
        ins: E. Alekseev
      -
        ins: E. Smyshlyaeva
      -
        ins: A. Sokolov
    date: April 2019

  AEGIS-PERF:
    target: https://github.com/jedisct1/openssl-family-bench/blob/master/img/boring-aeads.png
    title: "BoringSSL AEADs comparison"
    author:
      -
        ins: "Frank Denis"
    date: October 2022

  ANSSI-PFS:
    target: https://www.ssi.gouv.fr/uploads/2015/09/NT_IPsec_EN.pdf
    title: "Recommendations for securing networks with IPsec"
    author:
      -
        ins: "Agence nationale de la sécurité des systèmes d'information"
    date: August 2015

  ANSSI-TLS:
    target: https://www.ssi.gouv.fr/uploads/2017/02/security-recommendations-for-tls_v1.1.pdf
    title: "Security Recommendations for TLS"
    author:
      -
        ins: "Agence nationale de la sécurité des systèmes d'information"
    date: January 2017

  BoringSSL:
    target: https://boringssl.googlesource.com/boringssl/
    title: "BoringSSL"
    author:
      -
        ins: "Google"
    date: January 2023

  BSI:
    target: https://www.bsi.bund.de/SharedDocs/Downloads/EN/BSI/Publications/TechGuidelines/TG02102/BSI-TR-02102-2.pdf
    title: "Technical Guideline TR-02102-2 Cryptographic Mechanisms: Recommendations and Key Lengths Part 2 – Use of Transport Layer Security (TLS)"
    author:
      -
        ins: "Bundesamt für Sicherheit in der Informationstechnik"
    date: February 2022

  eBACS-DH:
    target: https://bench.cr.yp.to/results-dh.html
    title: "Measurements of public-key Diffie–Hellman secret-sharing systems, indexed by machine"
    author:
      -
        ins: "eBACS: ECRYPT Benchmarking of Cryptographic Systems"
    date: January 2023

  eBACS-KEM:
    target: https://bench.cr.yp.to/results-kem.html
    title: "Measurements of key-encapsulation mechanisms, indexed by machine"
    author:
      -
        ins: "eBACS: ECRYPT Benchmarking of Cryptographic Systems"
    date: January 2023

  Exfiltration:
    target: https://blog.apnic.net/2022/03/31/how-to-detect-and-prevent-common-data-exfiltration-attacks/
    title: "How to: Detect and prevent common data exfiltration attacks"
    author:
      -
        ins: "APNIC"
    date: March 2022

  Heist:
    target: https://theintercept.com/2015/02/19/great-sim-heist/
    title: "How Spies Stole the Keys to the Encryption Castle"
    author:
      -
        ins: "The Intercept"
    date: February 2015

  NIST-Lifetime:
    target: https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-57pt1r5.pdf
    title: "Recommendation for Key Management: Part 1 – General"
    author:
      -
        ins: "National Institute of Standards and Technology"
    date: May 2020

  NIST-TLS:
    target: https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-52r2.pdf
    title: "Guidelines for the Selection, Configuration, and Use of Transport Layer Security (TLS) Implementations"
    author:
      -
        ins: "National Institute of Standards and Technology"
    date: August 2019

  NIST-ZT:
    target: https://www.nccoe.nist.gov/sites/default/files/2022-12/zta-nist-sp-1800-35b-preliminary-draft-2.pdf
    title: "Implementing a Zero Trust Architecture"
    author:
      -
        ins: "National Institute of Standards and Technology"
    date: December 2022

  NIST-ZT2:
    target: https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-207.pdf
    title: "Zero Trust Architecture"
    author:
      -
        ins: "National Institute of Standards and Technology"
    date: August 2020

  NSA-ZT:
    target: https://media.defense.gov/2021/Feb/25/2002588479/-1/-1/0/CSI_EMBRACING_ZT_SECURITY_MODEL_UOO115131-21.PDF
    title: "Embracing a Zero Trust Security Model"
    author:
      -
        ins: "National Security Agency"
    date: February 2021

  Signal:
    target: https://signal.org/docs/specifications/doubleratchet/
    title: "The Double Ratchet Algorithm"
    author:
      -
        ins: "Signal"
    date: November 2016

  TS.33.210:
    target: "https://portal.3gpp.org/desktopmodules/Specifications/SpecificationDetails.aspx?specificationId=2279"
    title: "TS 33.210 Network Domain Security (NDS); IP network layer security"
    author:
      -
        ins: "3GPP"
    date: September 2022
    seriesinfo: 3GPP TS 33.210 17.1.0

  TS.33.501:
    target: "https://portal.3gpp.org/desktopmodules/Specifications/SpecificationDetails.aspx?specificationId=3169"
    title: "TS 33.501 Security architecture and procedures for 5G System"
    author:
      -
        ins: "3GPP"
    date: December 2022
    seriesinfo: 3GPP TS 33.501 18.0.0

--- abstract

Massive pervasive monitoring attacks using key exfiltration and made possible by key exchange without forward secrecy have been reported. If key exchange without Diffie-Hellman is used, static exfiltration of the long-term authentication keys enables passive attackers to compromise all past and future connections. Malicious actors can get access to long-term keys in different ways: physical attacks, hacking, social engineering attacks, espionage, or by simply demanding access to keying material with or without a court order. Exfiltration attacks are a major cybersecurity threat.  If NULL encryption is used an on-path attacker can read all application data. The use of psk_ke and NULL encryption are not following zero trust principles of minimizing the impact of breach and governments have already made deadlines for their deprecation. This document sets the Recommended values of psk_ke, TLS_SHA256_SHA256, TLS_SHA384_SHA384, ffdhe2048 to "D" and the Recommended values of rsa_pkcs1_sha256, rsa_pkcs1_sha384, and rsa_pkcs1_sha512 to "N".

--- middle

# Introduction

{{RFC8447}} added a Recommended column to many of the TLS registries. The Recommended column did originally non-normatively indicate parameters that are generally recommended for implementations to support. The meaning of the column was changed by {{I-D.ietf-tls-rfc8447bis}} to indicate that the IETF has consensus that the item is RECOMMENDED, i.e., using normative {{RFC2119}} language. {{I-D.ietf-tls-rfc8447bis}} also introduced a third value "D" indicating that an item is discouraged and SHOULD NOT or MUST NOT be used. This means that all current values need to be reevaluated. The current values also need to be reevaluated as attacks, government requirements, and best practices have changed in the more than 4 years since {{RFC8446}} and {{RFC8447}} were published.

This document evaluates TLS 1.3 pre-shared key exchange modes, (EC)DHE groups, signature algorithms, and cipher suites and changes the values in the Recommended column for psk_ke, TLS_SHA256_SHA256, TLS_SHA384_SHA384, ffdhe2048, rsa_pkcs1_sha256, rsa_pkcs1_sha384, and rsa_pkcs1_sha512. The document does not evaluate TLS 1.2 parameters. TLS 1.2 is obsolete {{RFC8446}} and NIST requires support for TLS 1.3 by January 1, 2024 {{NIST-TLS}}. This means that two NIST compatible implementations will never negotiate TLS 1.2 at the time this document would be published.

## Terminology

{::boilerplate bcp14}

# Key Exchange Without Forward Secrecy

Key exchange without forward secrecy enables passive monitoring {{RFC7258}}. Massive pervasive monitoring attacks using key exfiltration and made possible by key exchange without forward secrecy have been reported {{Heist}}, and many more have likely happened without ever being reported.  If key exchange without Diffie-Hellman is used, access to the long-term authentication keys enables passive attackers to compromise all past and future connections. Malicious actors can get access to long-term keys in different ways: physical attacks, hacking, social engineering attacks, espionage, or by simply demanding access to keying material with or without a court order. Exfiltration attacks are a major cybersecurity threat {{Exfiltration}}.

All cipher suites without forward secrecy have been marked as NOT RECOMMENDED in TLS 1.2 {{I-D.ietf-tls-rfc8447bis}}, and static RSA and DH are forbidden in TLS 1.3 {{RFC8446}}. A large number of TLS profiles and implementations forbid the use of key exchange without Diffie-Hellman.

- ANSSI states that for all versions of TLS: "The perfect forward secrecy property must be ensured" {{ANSSI-TLS}}.

- The general 3GPP TLS 1.2 profile follows {{RFC9113}} and states: "Only cipher suites with AEAD (e.g., GCM) and PFS (e.g.  ECDHE, DHE) shall be supported" {{TS.33.210}}.

- BoringSSL has chosen to not implement psk_ke, so that TLS 1.3 resumption always incorporates fresh key material {{BoringSSL}}.

Unfortunately, TLS 1.3 allows key exchange without forward secrecy in both full handshakes and resumption handshakes with the psk_ke. As stated in {{RFC8446}}, psk_ke does not fulfill one of the fundamental TLS 1.3 security properties, namely "Forward secret with respect to long-term keys".  When the PSK is a group key, which is now formally allowed in TLS 1.3 {{RFC9257}}, psk_ke fails yet another one of the fundamental TLS 1.3 security properties, namely "Secrecy of the session keys" {{Akhmetzyanova}} {{RFC9257}}. PSK authentication has yet another big inherent weakness as it often does not provide "Protection of endpoint identities".  It could be argued that PSK authentication should be not recommended solely based on this significant privacy weakness. The 3GPP radio access network that to a large degree relies on PSK are fixing the vulnerabilities by augmenting PSK with ECIES and ECDHE, see Annex C of {{TS.33.501}} and {{I-D.ietf-emu-aka-pfs}}.

Together with ffdhe2048 and rsa_pkcs1, psk_ke is one of the bad apples in the standards track TLS 1.3 fruit basket.  Organizations like BSI {{BSI}} has already produced recommendations regarding its deprecation.

- BSI states regarding psk_ke that "This mode should only be used in special applications after consultation of an expert." and has set a deadline that use is only allowed until 2026.

Two essential zero trust principles are to assume that breach is inevitable or has likely already occurred {{NSA-ZT}}, and to minimize impact when breach occur {{NIST-ZT}}. One type of breach is key compromise or key exfiltration. Different types of exfiltration are defined and discussed in {{RFC7624}}. Static exfiltration where the keys are transferred once has a lower risk profile than dynamic exfiltration where keying material or content is transferred to the attacker frequently. Forcing an attacker to do dynamic exfiltration minimizes the impact of breach and should be considered best practice. This significantly increases the risk of discovery for the attacker.

One way to force an attacker to do dynamic exfiltration is to frequently rerun ephemeral Diffie-Hellman. For IPsec, ANSSI {{ANSSI-PFS}} recommends enforcing periodic rekeying with ephemeral Diffie-Hellman, e.g., every hour and every 100 GB of data, in order to limit the impact of a key compromise. This should be considered best practice for all protocols and systems. The Double Ratchet Algorithm in the Signal protocol {{Signal}} enables very frequent use of ephemeral Diffie-Hellman. The practice of frequently rerunning ephemeral Diffie-Hellman follows directly from the two zero trust principles mentioned above.

In TLS 1.3, the application_traffic_secret can be rekeyed using key_update, a resumption handshake, or a full handshake. The term forward secrecy is not very specific, and it is often better to talk about the property that compromise of key A does not lead to compromise of key B. {{fig-impact}} illustrates the impact of some examples of static key exfiltration when psk_ke, key_update, and (ec)dhe are used for rekeying.  Each time period T{{{ᵢ}}} uses a single application_traffic_secret. {{{✘}}} means that the attacker has access to the application_traffic_secret in that time period and can passively eavesdrop on the communication. {{{✔}}} means that the attacker does not have access to the application_traffic_secret. Exfiltration and frequently rerunning EC(DHE) is discussed in Appendix F of {{I-D.ietf-tls-rfc8446bis}}.

~~~~~~~~~~~~~~~~~~~~~~~ aasvg
 rekeying with psk_ke
 static exfiltration of psk in T₃:
+-----+-----+-----+-----+-----+-----+-----+-----+     +-----+-----+
|  ✘  |  ✘  |  ✘  |  ✘  |  ✘  |  ✘  |  ✘  |  ✘  | ... |  ✘  |  ✘  |
+-----+-----+-----+-----+-----+-----+-----+-----+     +-----+-----+
   T₀    T₁    T₂    T₃    T₄    T₅    T₆    T₇   ...   Tₙ₋₁   Tₙ
 <--------------------------------------------------------------->

 rekeying with key_update
 static exfiltration of application_traffic_secret in T₃:
+-----+-----+-----+-----+-----+-----+-----+-----+     +-----+-----+
|  ✔  |  ✔  |  ✔  |  ✘  |  ✘  |  ✘  |  ✘  |  ✘  | ... |  ✘  |  ✘  |
+-----+-----+-----+-----+-----+-----+-----+-----+     +-----+-----+
   T₀    T₁    T₂    T₃    T₄    T₅    T₆    T₇   ...   Tₙ₋₁   Tₙ
                   <--------------------------------------------->

 rekeying with (ec)dhe
 static exfiltration of all keys in T₃:
+-----+-----+-----+-----+-----+-----+-----+-----+     +-----+-----+
|  ✔  |  ✔  |  ✔  |  ✘  |  ✔  |  ✔  |  ✔  |  ✔  | ... |  ✔  |  ✔  |
+-----+-----+-----+-----+-----+-----+-----+-----+     +-----+-----+
   T₀    T₁    T₂    T₃    T₄    T₅    T₆    T₇   ...   Tₙ₋₁   Tₙ
                   <--->
~~~~~~~~~~~~~~~~~~~~~~~
{: #fig-impact title="Impact of static key exfiltration in time period T3 when psk_ke, key_update, and (ec)dhe are used." artwork-align="center"}

Modern ephemeral key exchange algorithms like x25519 {{RFC7748}} are very fast and have small message overhead. The public keys are 32 bytes long and the cryptographic operations take 53 microseconds per endpoint on a single core AMD Ryzen 5 5560U {{eBACS-DH}}. Ephemeral key exchange with the quantum-resistant algorithm Kyber that NIST will standardize is even faster. For the current non-standardized version of Kyber512 the cryptographic operations take 12 microseconds for the client and 8 microseconds for the server {{eBACS-KEM}}.

<!--(102661 + 110972) / 4.062 / 10^3 -->
<!--(21880 + 26067) / 4.062 / 10^3 -->
<!--(32241) / 4.062 / 10^3 -->

Unfortunately, psk_ke is marked as "Recommended" in the IANA PskKeyExchangeMode registry. This may severely weaken security in deployments following the "Recommended" column.  Introducing TLS 1.3 in 3GPP had the unfortunate and surprising effect of drastically lowering the minimum security when TLS is used with PSK authentication.  Some companies in 3GPP have been unwilling to mark psk_ke as not recommended as it is so clearly marked as "Recommended" by the IETF. By labeling psk_ke as "Recommended", IETF is legitimizing and implicitly promoting bad security practice.

This document sets the Recommended value of psk_ke to "D" indicating discouraged.

# Cipher Suites with NULL Encryption

Cipher suites with NULL encryption enables passive monitoring {{RFC7258}} and were completely removed from TLS 1.3 {{RFC8446}}. Unfortunately, the independent stream document {{RFC9150}} reintroduced cipher suites with NULL Encryption in TLS 1.3 even though NULL encryption violates several of the fundamental TLS 1.3 security properties, namely "Protection of endpoint identities", "Confidentiality", and "Length concealment". Some companies in 3GPP have already suggested to use {{RFC9150}} in QUIC but luckily this is forbidden by {{RFC9001}} and hopefully it will stay like that.

Modern encryption algorithms like AES-GCM {{RFC5288}} are very fast and have small message overhead. Upcoming algorithms like AEGIS {{I-D.irtf-cfrg-aegis-aead}} is much faster than AES-GCM {{AEGIS-PERF}}. NULL encryption has no raison d'{{{ê}}}tre in two-party protocols.

Two essential zero trust principles are to assume that breach is inevitable or has likely already occurred {{NSA-ZT}}, and to minimize impact when breach occur {{NIST-ZT}}. One type of breach is an on-path attacker present on the enterprise network. In {{NIST-ZT2}}, NIST states as the first basic assumption for network connectivity for any organization that utilizes Zero trust is that:

- "The entire enterprise private network is not considered an implicit trust zone. Assets should always act as if an attacker is present on the enterprise network, and communication should be done in the most secure manner available. This entails actions such as authenticating all connections and encrypting all traffic."

This document sets the Recommended value of TLS_SHA256_SHA256 and TLS_SHA384_SHA384 to "D" indicating discouraged.

# 2048-bit Finite Field Diffie-Hellman

Government organizations like NIST, ANSSI, BSI, and NSA have already produced recommendations regarding the deprecation of ffdhe2048. NIST {{NIST-Lifetime}} and ANSSI {{ANSSI-TLS}} only allow 2048-bit Finite Field Diffie-Hellman if the application data does not have to be protected after 2030. If the application data had a security life of ten years, NIST and ANSSI allowed use of ffdhe2048 until December 31, 2020. BSI {{BSI}} allowed use of ffdhe2048 up to the year 2022. The Commercial National Security Algorithm Suite (CNSA) {{RFC9151}} forbids the use of ffdhe2048. This document sets the Recommended value of ffdhe2048 to "D" indicating discouraged.

# Signature Algorithms with PKCS #1 v1.5 Padding

Recommendations regarding RSASSA-PKCS1-v1_5 varies. The RSA Cryptography Specifications {{RFC8017}} specifies that "RSASSA-PSS is REQUIRED in new applications. RSASSA-PKCS1-v1_5 is included only for compatibility with existing applications.". BSI {{BSI}} allows use of the PKCS #1 v1.5 padding scheme in TLS certificates up to the year 2025. The Commercial National Security Algorithm (CNSA) {{RFC9151}} requires offer of rsa_pkcs1_sha384 . This document sets the Recommended value of rsa_pkcs1_sha256, rsa_pkcs1_sha384, and rsa_pkcs1_sha512 to "N".

# IANA Considerations

## TLS PskKeyExchangeMode

IANA is requested to update the TLS PskKeyExchangeMode registry under the Transport Layer Security (TLS) Parameters heading'. For the following entry the the "Recommended" value has been set to "D" indicating that the item is "Discouraged".

| Desctiption | Recommended |
| psk_ke | D |

## TLS Cipher Suites

IANA is requested to update the TLS Cipher Suites registry under the Transport Layer Security (TLS) Parameters heading. For all cipher suites listed in Appendix A of {{RFC9113}}, all cipher suites listed in Appendix A of {{I-D.ietf-tls-deprecate-obsolete-kex}}, and the following entries the "Recommended" value has been set to "D" indicating that the item is "Discouraged".

| Desctiption | Recommended |
| TLS_SHA256_SHA256 | D |
| TLS_SHA384_SHA384 | D |
| TLS_PSK_DHE_WITH_AES_128_CCM_8 | D |
| TLS_PSK_DHE_WITH_AES_256_CCM_8| D |
| TLS_PSK_WITH_CHACHA20_POLY1305_SHA256 | D |

## TLS Supported Groups

IANA is requested to update the TLS Supported Groups registry under the Transport Layer Security (TLS) Parameters heading. For the following entries the "Recommended" value has been set to "D" indicating that the item is "Discouraged".

| Desctiption | Recommended |
| sect163k1 | D |
| sect163r1 | D |
| sect163r2 | D |
| sect193r1 | D |
| sect193r2 | D |
| sect233k1 | D |
| sect233r1 | D |
| sect239k1 | D |
| secp160k1 | D |
| secp160r1 | D |
| secp160r2 | D |
| secp192k1 | D |
| secp192r1 | D |
| secp224k1 | D |
| secp224r1 | D |
| ffdhe2048 | D |

## TLS SignatureScheme

IANA is requested to update the TLS SignatureScheme registry under the Transport Layer Security (TLS) Parameters heading. For the following entries the the "Recommended" value has been set to "D" indicating that the item is "Discouraged" or to "N".

| Desctiption | Recommended |
| rsa_pkcs1_sha1 | D |
| ecdsa_sha1 | D |
| rsa_pkcs1_sha256 | N |
| rsa_pkcs1_sha256_legacy | D |
| rsa_pkcs1_sha384 | N |
| rsa_pkcs1_sha384_legacy | D |
| rsa_pkcs1_sha512 | N |
| rsa_pkcs1_sha512_legacy| D |

--- back

# Acknowledgements
{: numbered="false"}

The authors want to thank {{{Ari Keränen}}}, {{{Eric Rescorla}}}, and {{{Paul Wouters}}} for their valuable comments and feedback.
