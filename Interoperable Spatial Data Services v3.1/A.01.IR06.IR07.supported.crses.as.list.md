# A.01.IR06.IR07.supported.crses.as.list

**Purpose**: For interoperability reasons, if appropriate for the offered datasets, the INSPIRE SDS should provide their data using a subset of the well-known
2D and 3D coordinate reference systems listed in Annex II.1 of [INT SDS](#README.md#ref_INT SDS). The list of the
supported CRSes for a service shall be given as a list in the service metadata record to make it easier to discover them.

**Prerequisites**

* The metadata record for the service needs to pass as a valid ISO 19139 metadata record (schema validation) including both ```gmd``` and the ```srv``` schemas (see [namespaces](README.md#namespaces)).

**Test method**

* Check that [RS codes](#rs_codes) is not empty. If so, pass the test. Otherwise fail the test.

**Reference(s)**

* [TG SDS](README.md#ref_TG_SDS), 4.6.1
* [INT SDS](README.md#ref_INT_SDS), Annex II, 1. Coordinate reference systems
* [DS CRS](README.md#ref_DS_CRS)
* [IR MD](README.md#ref_IR_MD), Annex II, 1.3.4 Other Coordinate Systems

**Test type**: Automated

**Notes**

* The list of the allowed INSPIRE CRS identifiers is only given as a recommendation, so it's not possible to automatically validate if the CRSes provided fulfill the INSPIRE CRS criteria (ETRS89 based for data inside Europe, ITRS based otherwise).
* There is no test for the CRS codeSpace element, as there are no requirements or guidance in for using it in [TG SDS](README.md#ref_TG_SDS).

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
RS codes <a name="rs_codes"></a> | /gmd:MD_Metadata/gmd:referenceSystemInfo/gmd:MD_ReferenceSystem/gmd:referenceSystemIdentifier/gmd:RS_Identifier/gmd:code/(gmx:Anchor/@xlink:href&#124;gco:CharacterString)
