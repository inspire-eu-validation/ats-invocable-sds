# extension for QoS declared capacity

**Purpose**: Declared Quality of Service level helps the users to rule out services tha do not fulfill their required QoS criteria.

**Prerequisites**

* The metadata record for the service needs to pass as a valid ISO 19139 metadata record (schema validation) including both ```gmd``` and the ```srv``` schemas (see [namespaces](README.md#namespaces)).
* The metadata record for the service needs to pass as a valid XML document against the INSPIRE SDS extended metadata XML Schema (inspire\_sds\_gmd).

**Test method**

Check that the [availability statement](#availability_statement) for capacity is given. If so, pass the test. Otherwise fail the test.

**Reference(s)**

* [TG SDS](README.md#ref_TG_SDS), 4.6.2 Quality of Service

**Test type**: Automated

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
availability statement <a name="availability_statement"></a> | /gmd:MD_Metadata/gmd:identificationInfo/inspire\_sds\_gmd:SV_ServiceIdentification/inspire\_sds\_gmd:qualityOfService/inspire\_sds\_gmd:SV_QualityOfService[child::inspire\_sds\_gmd:criterion/inspire\_sds\_gmd:SV_QualityOfServiceCriteria='capacity' and child::inspire\_sds\_gmd:unit and child::inspire\_sds\_gmd:value]
