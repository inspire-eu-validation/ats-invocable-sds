Interoperable Spatial Data Services v3.1
========================================

Conformance Class for "Interoperable Spatial Data Services"
as defined in the Technical Guidance for INSPIRE Spatial Data Services and services allowing spatial data services to be invoked.

*Note*: This CC is in ready-for-review stage, none of the tests have an official INSPIRE MIG approval.

## External document references

| Abbreviation | Document name                       |
| ------------ | ----------------------------------- |
| INSPIRE <a name="ref_INSPIRE"></a> | [Directive 2007/2/EC of the European Parliament and of the Council of 14 March 2007 establishing an Infrastructure for Spatial Information in the European Community (INSPIRE)](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32007L0002&from=EN)
| INT SDS <a name="ref_INT_SDS"></a> | [Commission Regulation (EU) No 1089/2010 of 23 November 2010 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards interoperability of spatial data sets and services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=OJ:L:2010:323:FULL&from=EN)
| INT SDS AMD <a name="ref_INT_SDS_AMD"></a> | [Commission Regulation (EU) No 1312/2014 of 10 December 2014 amending Regulation (EU) No 1089/2010 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards interoperability of spatial data services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32014R1312&from=EN)
| IR MD <a name="ref_IR_MD"></a> | [Commission Regulation (EC) No 1205/2008 of 3 December 2008 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards metadata (Text with EEA relevance)](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32008R1205&from=EN)
| IR NS <a name="ref_IR_NS"></a>   | [Commission Regulation (EC) No 976/2009 of 19 October 2009 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards the Network Services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32009R0976&from=EN)
| IR NS AMD <a name="ref_IR_NS_AMD"></a> | [Commission Regulation (EU) No 1311/2014 of 10 December 2014 amending Regulation (EC) No 976/2009 as regards the definition of an INSPIRE metadata element](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32014R1311&from=EN)
| TG SDS <a name="ref_TG_SDS"></a> | [Technical Guidance for INSPIRE Spatial Data Services and services allowing spatial data services to be invoked](http://inspire.jrc.ec.europa.eu/documents/Spatial_Data_Services/TG_for_INSPIRE_SDS_3_1.pdf)
| SDS ALT <a name="ref_SDS_alt"></a> | Alternative approaches to implement Metadata for Spatial data services (not published?)
| DS CRS <a name="ref_DS_CRS"></a> | [D2.8.I.1 Data Specification on Coordinate Reference Systems – Technical Guidelines](http://inspire.ec.europa.eu/documents/Data_Specifications/INSPIRE_DataSpecification_RS_v3.2.pdf)

## TG Requirement coverage

Based on requirement numbering in [TG SDS](#ref_TG_SDS).

| Req#   | Description                          | Covered by test(s)                 | IR reference(s)                  |
| ------ | ------------------------------------ | ---------------------------------- | -------------------------------- |
| 6      | Supported CRSes as a list | [Supported CRSes as list](supported-crses-as-list.md)| |
| 7      | CRS identifiers | [Supported CRSes as list](supported-crses-as-list.md) | |
| 8      | Indicate QoS for availability | [Extension for QoS declared availability](extension-for-qos-declared-availability.md) or [dq conceptualconsistency for qos declared availability](dq-conceptualconsistency-for-qos-declared-availability.md) | |
| 9      | Indicate QoS for performance | [Extension for QoS declared performance](extension-for-qos-declared-performance.md) or [dq conceptualconsistency for qos declared.performance](dq conceptualconsistency for qos declared.performance.md) | |
| 10     | Indicate QoS for capacity |[Extension for QoS declared capacity](extension-for-qos-declared-capacity.md) or [dq conceptualconsistency for qos declared capacity](dq-conceptualconsistency-for-qos-declared-capacity.md) | |
| 11     | Provide "custodian" contact point | [Custodian contact point](custodian-contact-point.md) | |
| 12     | Constraints for access and use | not automatically testable |  |

## Tests

The CC for the "TG Conformance Class 2:Spatial data services compliant with interoperability arrangements"
includes all the tests in the [CC Invocable SDS](http://inspire.ec.europa.eu/id/ats/spatial-data-services/3.1/Invocable-Spatial-Data-Services), and additionally
the following tests:

| Identifier                                                        | Status   |
| ----------------------------------------------------------------- | -------- |
| [Supported crses as list](supported-crses-as-list.md) | ready for review |
| [Extension for QoS declared availability](extension-for-qos-declared-availability.md) | ready for review |
| [Extension for QoS declared performance](extension-for-qos-declared-performance.md) | ready for review |
| [Extension for QoS declared capacity](extension-for-qos-declared-capacity.md) | ready for review |
| [Custodian contact point](custodian-contact-point.md) | ready for review |
| [SDS SV ServiceIdentification](sds-sv-serviceidentification.md) | ready for review |

## Tests (MIWP-8 alternative)

The CC for the "TG Conformance Class 2:Spatial data services compliant with interoperability arrangements"
according to the alternative option for the QoS reporting proposed by MIWP-8, includes all the tests
in the [CC Invocable SDS](http://inspire.ec.europa.eu/id/ats/spatial-data-services/3.1/Invocable-Spatial-Data-Services), and additionally
the following tests:

| Identifier                                                        | Status   |
| ----------------------------------------------------------------- | -------- |
| [Supported crses as list](supported-crses-as-list.md) | ready for review |
| [DQ ConceptualConsistency for QoS declared availability](dq-conceptualconsistency-for-qos-declared-availability.md) | ready for review |
| [DQ ConceptualConsistency for QoS declared.performance](dq conceptualconsistency for qos declared.performance.md) |ready for review |
| [DQ ConceptualConsistency for QoS declared capacity](dq-conceptualconsistency-for-qos-declared-capacity.md) | ready for review |
| [Custodian contact point](custodian-contact-point.md) | ready for review |
| [DQ DomainConsistency report for classification](dq-domainconsistency-report-for-classification.md) | ready for review |

## Open issues
* The extension to the ISO 19119 metadata class ```SV_ServiceIdentification``` is defined twice in [TG SDS](#ref_TG_SDS): in Annex A just the ```category``` as a mandatory property is added, and in Annex C just the ```qualityOfService``` mandatory property is added. This means that the neither of these extended classes can be used to fulfill both the requirements IR 1 and IR 8, IR 9 or IR 10 at the same time.
* The XML Schema for the inspire_sds_gmd has not been published yet, so the XML Schema validation is not possible.

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
gmd | http://www.isotc211.org/2005/gmd
gml | http://www.opengis.net/gml/3.2
srv | http://www.isotc211.org/2005/srv
inspire\_sds\_gmd | [missing]
xlink          | http://www.w3.org/1999/xlink
