# A.03.IR05.SDS.specification.cited

**Purpose**:

**Prerequisites**

* The metadata record for the service needs to pass as a valid ISO 19139 metadata record (schema validation) including both ```gmd``` and the ```srv``` schemas (see [namespaces](README.md#namespaces)).

**Test method**

Check that at least one [Access point URL](#access_point_url) is found in the service metadata record. If so, pass the test. Otherwise fail the test.

**Reference(s)**

* [TG SDS](README.md#ref_TG_SDS), section 4.5.2

**Test type**: Automated

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Access point URL <a name="access_point_url"></a> | /gmd:MD\_Metadata/gmd:distributionInfo/gmd:MD\_Distribution/gmd:transferOptions/gmd:MD\_DigitalTransferOptions/gmd:onLine/gmd:CI\_OnlineResource[child::gmd:linkage/gmd:URL and child::gmd:function/gmd:CI\_OnLineFunctionCode[@codeList='http://inspire.ec.europa.eu/draft-schemas/resources/Codelist/gmxCodelist.xml#INSPIRE_CI_OnLineFunctionCode' and (@codeListValue='accessPoint-selfDescribing' or @codeListValue='accessPoint')]]/gmd:linkage/gmd:URL