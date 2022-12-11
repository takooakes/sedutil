Sorry for this odd PR. Your fork doesn't have issues enabled.

Hey takooakes, looks like you've got one of the more active forks of sedutil so maybe you could help.

I've got a few "Intel SSD Pro 1500" drives with locked ATA passwords that I'd like to PSID revert into being usable. The problem is sedutil-cli thinks they're not OPAL drives.

- The spec sheet for them is here: [https://www.intel.com/content/dam/www/p ... cation.pdf](https://www.intel.com/content/dam/www/public/us/en/documents/product-specifications/ssd-pro-1500-series-sata-specification.pdf)
- That spec sheet says they "support the TCG Opal SSC Specification Version 1.0 Rev 3.0 mandatory commands"
- The spec sheet says they support "PSID (Physical presence Security ID) Revert for SSD Repurposing"
- They have 32 character PSIDs printed on their labels that I can clearly read

I've tried your fork with no luck
```
sudo ./sedutil-cli --scan
Scanning for Opal compliant disks
/dev/sda   No      ST3250318AS                              CC46    
/dev/sdb   No      INTEL SSDSC2BF240A4L                     LS2i    
/dev/sdc   No      ST3250318AS                              CC46  
```
That INTEL one should not say "No." Can you offer any ideas or help?
