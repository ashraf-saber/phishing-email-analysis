# Case 02: DNS Capture Analysis

## Summary
I analyzed a DNS capture (dns.cap) with 38 packets between a client (192.168.170.8) and a DNS server (192.168.170.20).

## Evidence
- 19 queries and 19 responses.
- Query types seen: TXT, MX, LOC, PTR, A, AAAA.
- Each response matches its query by the same Transaction ID (example: 0x1032 for the TXT query on google.com).
- Reply code: No error.
- Response time for the first query: 530 microseconds.

## Findings
- Every query has a matching response.
- No random-looking or suspicious domain names.
- The record types are normal for daily DNS use (IP lookups, mail servers, reverse lookups, SPF text records).

## Verdict
Benign. The traffic is normal DNS: IDs match, replies are fast, and there are no errors or odd domains.
