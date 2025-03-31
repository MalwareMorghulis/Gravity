# About
DNS Sinkhole list of FQDNs from LevelBlue (AlienVault) OTX pivots by "MalwareMorghulis"

Data was curated from automated and manual pivots to uncover suspicious or potentially hostile infrastructure.

These monikers are my own naming convention - unrelated to CrowdStrike, Mandiant, Palo Alto, etc. They are named for fun based on the TTP observed.

It is currently unconfirmed whether or not these activity clusters are related or the same threat actor. Pending deeper review at this time.

Eventually, the lists will be reduced to regexes for maintenance purposes, ease of change-control, and due to UI limitations of LevelBlue OTX.

# Generic List:
- Blocklist: Generic blocklist for sinkholing (some overlap here, but will eventually be independent from the 3x below).

# TLD Block List (See WARNING below):
- TLD_IANA_Generic.txt: Contains ALL* (at least in 2024) generic TLDs (gTLDs) authorized by IANA for blocking entire swaths of the Internet.
- TLD_IANA_CountryCodes.txt: Contains ALL* (at least in 2024) Country Code TLDs (ccTLDs) authorized by IANA for blocking entire swaths of the Internet.

**WARNING**: Please modify these TLD blocks as necessary and in your own repo. You have to point your PiHole to your own repo for any custom TLD blocklists because these TLD lists will block almost everything (even *.com, etc).
**NOTE**: There are also way more efficient methods (ie: geolocation lists) or optimized entries to add TLDs into sinkholes, such as in single-line groupings with pipe '|' characters.

# DGA Tracker
- Cats Cradle: SMS spearphishing utilizing random characters (approximately 5-9 characters)
- Double Helix: SMS spearphishing utilizing dual-word concatenation (even words are truncated)
- Easy Rider: Toll-themed or EZ-Pass themed SMS spearphishing utlizing random character concatenation.
- Pandoras Box: USPS-themed SMS Spearphishing Domains (typically package tracking or typo-squatting service offerings like Informed Delivery)

# Special Thanks
Thank you to DomainTools for your support and helping me stay in the fight! The Iris tool is amazing and I've been using it for expanding and long-term analysis in the DGA clusters.

# Disclaimer
1) This list is provided "as-is". This may break infrastructure because some nameservers could be in this list. Use at your own risk.
