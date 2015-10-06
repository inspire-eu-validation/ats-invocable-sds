# A.01.IR01.SDS.SV_ServiceIdentification

**Purpose**: To find services fit to be consumed by given client applications, it's necessary to be able to
discover if a Spatial Data Service is classified as ```invocable```, ```interoperable``` or ```harmonised```.

**Prerequisites**

* The metadata record for the service needs to pass as a valid ISO 19139 metadata record (schema validation) including both ```gmd``` and the ```srv``` schemas (see [namespaces](README.md#namespaces)).

**Test method**

* Check that at least one [category element](#sds_category) exists. If it does, pass the test. Otherwise fail the test.

*Note*: this test method relies on the XML Schema validation of the metadata record, including the SDS metadata extension schema (inspire\_sds\_gmd), see [namespaces](README.md#namespaces), and the fact that the category element type is
an enumeration, so that only the valid enumeration values pass the validation. If the schema validation is not done against
the SDS metadata extension schema, an additional step of checking that the category element value is one of ```invocable```, ```interoperable``` or ```harmonised``` needs to be added.


**Reference(s)**

* [TG SDS](README.md#ref_TG_SDS), section 4.5.1

**Test type**: Automated

**Notes**

* For the invocable SDS CC, the value of the category can be any of the ```invocable```, ```interoperable``` or ```harmonised```.
* It's assumed that for ```interoperable``` and ```harmonised``` SDSes, additional category elements are used, so that all the "super class" categories are also included. If they are not, the test for the "super class" CCs will not pass.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
category element <a name="sds\_category"></a> | /gmd:MD_Metadata/gmd:identificationInfo/inspire\_sds\_gmd:SV_ServiceIdentification/inspire\_sds\_gmd:category
