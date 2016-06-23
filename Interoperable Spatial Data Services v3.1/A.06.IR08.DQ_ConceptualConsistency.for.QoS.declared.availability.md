# A.06.IR08.DQ_ConceptualConsistency.for.QoS.declared.availability

**Purpose**: Declared Quality of Service level helps the users to rule out services tha do not fulfill their required QoS criteria.

**Prerequisites**

* The metadata record for the service needs to pass as a valid ISO 19139 metadata record (schema validation) including both ```gmd``` and the ```srv``` schemas (see [namespaces](README.md#namespaces)).

**Test method**

Check that the [availability statement](#availability_statement) for availability is given. If so, pass the test. Otherwise fail the test.

**Reference(s)**

* [TG SDS](README.md#ref_TG_SDS), 4.6.2 Quality of Service

**Test type**: Automated

**Notes**

* Identifying the INSPIRE QoS indicator just be a specific ```gco:CharacterString``` value ```Availability``` is not sufficient, as there may be other conceptual consistency reports with measures with the same name. There should be reference to the definition of this indicator in the INSPIRE context.
* The units of the measure must be identified in order to avoid misinterpretations, like whether the availability number should be interpreted as a percentage (0-100) or fraction (0 - 1).
* The type of the ```gco:Record``` is not defined in GML. There should be clear guidance on the content for this element in [TG SDS](README.md#ref_TG_SDS) in order to harmonize it's use.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
availability statement <a name="availability_statement"></a> | /gmd:MD_Metadata/gmd:dataQualityInfo/gmd:DQ_DataQuality/gmd:report/gmd:DQ_ConceptualConsistency[child::gmd:nameOfMeasure/gco:CharacterString='Availability' and child::gmd:result/gmd:DQ_QualitativeResult/gmd:value/gco:Record]
