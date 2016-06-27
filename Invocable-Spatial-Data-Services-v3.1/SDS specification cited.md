# SDS specification cited

**Purpose**: The TG SDS needs to be cited as the specification that the compliant SDS declares to be compliant with.

**Prerequisites**

* The metadata record for the service needs to pass as a valid ISO 19139 metadata record (schema validation) including both ```gmd``` and the ```srv``` schemas (see [namespaces](README.md#namespaces)).

**Test method**

Check if at least one of the [specification citation elements](#specification_citation) refer to the INSPIRE TG SDS. If yes, pass the test. Otherwise fail the test.

**Reference(s)**

* [TG SDS](README.md#ref_TG_SDS), section 4.5.3.1

**Test type**: Manual (for now)

**Notes**
* This requirements would be much easier to validate if the ```gmd:specification``` would be mandated to contain a link to the specific TG SDS version, like in test [A.04.IR01.DQ_DomainConsistency.report.for.classification](A.04.IR01.DQ_DomainConsistency.report.for.classification.md). The current IR 5 in TG SDS does not explicate the acceptable values for the ```gmd:title``` element, and thus automatic testing becomes impossible.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
specification citation elements <a name="specification_citation"></a> | /gmd:MD_Metadata/gmd:dataQualityInfo/gmd:DQ_DataQuality/gmd:report/gmd:DQ_DomainConsistency/gmd:result/gmd:DQ_ConformanceResult/gmd:specification/gmd:CI_Citation/gmd:title/gco:CharacterString
