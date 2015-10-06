# A.02.IR02.at.least.one.recource.locator

**Purpose**: It should be possible to automatically discover the access points of an invocable SDS using it's metadata record.

**Prerequisites**

* The metadata record for the service needs to pass as a valid ISO 19139 metadata record (schema validation) including both ```gmd``` and the ```srv``` schemas (see [namespaces](README.md#namespaces)).

**Test method**

Check that at least one [distribution online resource](#dist_online_resource) exists in the service metadata record. If so, pass the test. Otherwise fail the test.

**Reference(s)**

* [TG SDS](README.md#ref_TG_SDS), section 4.5.2

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
distribution online resource <a name="dist_online_resource"></a> | /gmd:MD\_Metadata/gmd:distributionInfo/gmd:MD\_Distribution/gmd:transferOptions/gmd:MD\_DigitalTransferOptions/gmd:onLine/gmd:CI\_OnlineResource/gmd:linkage/gmd:URL
