##About:
DNS Sinkhole list of FQDNs from LevelBlue (AlienVault) OTX pivots by "MalwareMorghulis"

Data was curated from automated and manual pivots to uncover suspicious or potentially hostile infrastructure.

These monikers for campaign tracking are my own naming convention - unrelated to CrowdStrike, Mandiant, Palo Alto, etc. They are named for fun based on the TTP observed.

Eventually, the lists will be reduced to regexes for maintenance purposes, ease of change-control, and due to UI limitations of LevelBlue OTX.

UPDATE: Based on available open-source reporting, these campaign activity clusters are likely associated with "Smishing Triad" (a cybercriminal group believed to be located in China).

##DGA Tracker:
- Cats Cradle: SMS spearphishing utilizing random characters (approximately 5-9 characters)
- Double Helix: SMS spearphishing utilizing dual-word concatenation (even words are truncated)
- Easy Rider: Toll-themed or EZ-Pass themed SMS spearphishing utlizing random character concatenation.
- Empty Promise: Fake recruiter spam, from emails, asking the user to contact them over third-party messengers: Telegram, WhatsApp, etc.
- Pandoras Box: USPS-themed SMS Spearphishing Domains (typically package tracking or typo-squatting service offerings like Informed Delivery)

##Generic List:
- Blocklist: Generic blocklist for sinkholing (some overlap here, but will eventually be independent from the 3x below).

##TLD Block List (See WARNING below):
- TLD_IANA_Generic.txt: Contains ALL* (at least in 2024) generic TLDs (gTLDs) authorized by IANA for blocking entire swaths of the Internet.
- TLD_IANA_CountryCodes.txt: Contains ALL* (at least in 2024) Country Code TLDs (ccTLDs) authorized by IANA for blocking entire swaths of the Internet.

##Special Thanks:
1) DomainTools - for your support and helping me stay in the fight! The IRIS Investigate tool is amazing and I've been using it for expanding and long-term analysis in the DGA clusters.
2) ExtraHop - for giving me the time & opportunity to pursue these side-hobby research objectives!

Honorable Mentions - Thank You for your support!
1) Sublime Security
2) Epeios
3) Daniel P at Malpedia
4) Paul B at MalBeacon
5) Hunt.io

##Disclaimer:
- These lists are provided "as-is". This may break infrastructure because some nameservers could be in this list. Fork & prune or use at your own risk.
- **WARNING**: Please modify these TLD blocks as necessary and in your own repo. You have to point your PiHole to your own repo for any custom TLD blocklists because these TLD lists will block almost everything (even *.com, etc).
- **NOTE**: There are also way more efficient methods (ie: geolocation lists) or optimized entries to add TLDs into sinkholes, such as in single-line groupings with pipe '|' characters.

##References:
- https://www.silentpush.com/blog/smishing-triad/
- https://krebsonsecurity.com/2025/04/china-based-sms-phishing-triad-pivots-to-banks/
- https://malpedia.caad.fkie.fraunhofer.de/actor/smishing_triad
- https://www.wired.com/story/smishing-triad-scam-group/
- https://www.resecurity.com/blog/article/smishing-triad-is-now-targeting-toll-payment-services-in-a-massive-fraud-campaign-expansion
