**1.  Safety-relevant Use Cases**
The ADT is not intended for safety-relevant use cases. We have not performed a tool evaluation according to ISO 26262-8.13.

If you are interested in this use case, please feel free to get in contact with us.

**2. Supported File Types**
2.1. Input Files
2.1.1 MDF Generation

The ADT only supports MDF 4.x and we keep on updating it, if new updates are published.

Please be aware that older MDF generations e.g. MDF 3.x might work, but we not actively support and test them. 

2.1.2 MDF Provider

The ADT only supports MDF files from ETAS and Vector.

We continuously work on extending support, but because all providers use the MDF standard slightly different, we cannot guarantee error-free functioning for all of them. 

2.2. Output
The ADT supports export of:
metadata into JSON
signals into Parquet or CSV 

**3. Signal Exporting**
3.1. File Type
Currently ADT is limited to timeseries data, meaning that images and video e.g. ADTF cannot be processed. 
