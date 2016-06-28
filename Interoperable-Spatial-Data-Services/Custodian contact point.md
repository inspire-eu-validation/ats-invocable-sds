# Custodian contact point

**Purpose**: The party responsible for the care and maintenance of the service needs to be discoverable both for evaluating the reliability of the service and for reporting the possible technical or interoperability issues.

**Prerequisites**

* The metadata record for the service needs to pass as a valid ISO 19139 metadata record (schema validation) including both ```gmd``` and the ```srv``` schemas (see [namespaces](README.md#namespaces)).

**Test method**

Check that the [Custodian pointOfContact](#custodian) is given. If so, pass the test. Otherwise fail the test.

**Reference(s)**

* [TG SDS](README.md#ref_TG_SDS), 4.6.3 Point of contact for the care and maintenance

**Test type**: Automated

**Notes**
* The XPath test also requires non-empty ```organisationName``` and ```electronicMailAddress``` for the pointOfContact, even though this is not explicitly required in [TG SDS](README.md#ref_TG_SDS) text. This is inline with the other INSPIRE ```pointOfContact``` metadata requirements.
* The Xpath expression requires the use on ```gco:CharacterString``` for both ```organisationName``` and ```electronicMailAddress```, even though it would be valid XML Schema wise to use ```gmx:Anchor``` elements in their place.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Custodian pointOfContact <a name="custodian"></a>   | /gmd:MD_Metadata/gmd:identificationInfo/srv:SV_ServiceIdentification/gmd:pointOfContact/gmd:CI_ResponsibleParty[child::gmd:role/gmd:CI_RoleCode/@codeList ='http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml#CI_RoleCode' and child::gmd:role/gmd:CI_RoleCode/@codeListValue='custodian' and not(child::gmd:organisationName/gco:CharacterString='') and not(child::gmd:contactInfo/gmd:CI_Contact/gmd:address/gmd:CI_Address/gmd:electronicMailAddress/gco:CharacterString='')]
