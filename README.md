ats-invocable-sds
===========================

Abstract Test Suite for "Invocable Spatial Data Services"
as defined in the Technical Guidance for INSPIRE Spatial Data Services and services allowing spatial data services to be invoked.

*Note*: This ATS is in Ready for review stage, none of the tests have an official INSPIRE MIG approval.

## External document references

| Abbreviation | Document name                       |
| ------------ | ----------------------------------- |
| INSPIRE <a name="ref_INSPIRE"></a> | [Directive 2007/2/EC of the European Parliament and of the Council of 14 March 2007 establishing an Infrastructure for Spatial Information in the European Community (INSPIRE)](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32007L0002&from=EN)
| INT SDS <a name="ref_INT_SDS"></a> | [Commission Regulation (EU) No 1089/2010 of 23 November 2010 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards interoperability of spatial data sets and services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=OJ:L:2010:323:FULL&from=EN)
| INT SDS AMD <a name="ref_INT_SDS_AMD"></a> | [Commission Regulation (EU) No 1312/2014 of 10 December 2014 amending Regulation (EU) No 1089/2010 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards interoperability of spatial data services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32014R1312&from=EN)
| IR NS <a name="ref_IR_NS"></a>   | [Commission Regulation (EC) No 976/2009 of 19 October 2009 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards the Network Services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32009R0976&from=EN)
| IR NS AMD <a name="ref_IR_NS_AMD"></a> | [Commission Regulation (EU) No 1311/2014 of 10 December 2014 amending Regulation (EC) No 976/2009 as regards the definition of an INSPIRE metadata element](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32014R1311&from=EN)
| TG SDS <a name="ref_TG_SDS"></a> | [Technical Guidance for INSPIRE Spatial Data Services and services allowing spatial data services to be invoked](http://inspire.jrc.ec.europa.eu/documents/Spatial_Data_Services/TG_for_INSPIRE_SDS_3_1.pdf)
| SDS ALT <a name="ref_SDS_alt"></a> | Alternative approaches to implement Metadata for Spatial data services (not published?)

## TG Requirement coverage

Based on requirement numbering in [TG SDS](#ref_TG_SDS).

| Req#   | Description                          | Covered by test(s)                 | IR reference(s)                  |
| ------ | ------------------------------------ | ---------------------------------- | -------------------------------- |
| 1      | Use the category element for classification | [A.01.IR01.SDS.SV_ServiceIdentification](A.01.IR01.SDS.SV_ServiceIdentification.md) OR [A.04.IR01.DQ_DomainConsistency.report.for.classification](A.04.IR01.DQ_DomainConsistency.report.for.classification.md)| |
| 2      | All access points via Resource Locator | [A.02.IR02.IR03.at.least.one.recource.locator](A.02.IR02.at.least.one.recource.locator.md) | |
| 3      | CI_OnlineFunctionCode to identify access points | [A.02.IR02.IR03.at.least.one.recource.locator](A.02.IR02.at.least.one.recource.locator.md)| |
| 4      | Specification as human and/or machine readable | not automatically testable | |
| 5      | Specification citing SDS must be given | [A.03.IR05.SDS.specification.cited](A.03.IR05.SDS.specification.cited.md) | |


## Tests

The ATS for the "TG Conformance Class 1: Implementation of Invocable Spatial Data Services" contains the following tests:

| Identifier                                                        | Status   |
| ----------------------------------------------------------------- | -------- |
| [A.01.IR01.SDS.SV_ServiceIdentification](A.01.IR01.SDS.SV_ServiceIdentification.md) | ready for review |
| [A.02.IR02.IR03.at.least.one.recource.locator](A.02.IR02.at.least.one.recource.locator.md) | ready for review |
| [A.03.IR05.SDS.specification.cited](A.03.IR05.SDS.specification.cited.md) | ready for review |

## Tests (MIWP-8 alternative)

The ATS for the "TG Conformance Class 1: Implementation of Invocable Spatial Data Services" according to the
alternative option for SDS classification proposed by MIWP-8, contains the following tests:

| Identifier                                                        | Status   |
| ----------------------------------------------------------------- | -------- |
| [A.04.IR01.DQ_DomainConsistency.report.for.classification](A.04.IR01.DQ_DomainConsistency.report.for.classification.md) | ready for review |
| [A.02.IR02.IR03.at.least.one.recource.locator](A.02.IR02.at.least.one.recource.locator.md) | ready for review |
| [A.03.IR05.SDS.specification.cited](A.03.IR05.SDS.specification.cited.md) | ready for review |

## Open issues

* The XML Schema for the inspire_sds_gmd has not been published yet, so the XML Schema validation is not possible.
* The codelist URL ```http://inspire.ec.europa.eu/draft-schemas/resources/Codelist/gmxCodelist.xml#INSPIRE_CI_OnLineFunctionCode``` does not look like a final one (refers to a non-existing resource under draft-schemas).The codelists and their value should point to the INSPIRE registry.
* The test [A.03.IR05.SDS.specification.cited](A.03.IR05.SDS.specification.cited.md) cannot be automated unless either
  * the IR 5 is changed into requiring a ```xlink:href``` attribute to be used in ```gmd:specification``` to refer to specific version of [TG SDS](#ref_TG_SDS), or
  * the acceptable (localized) ```gco:CharacterString``` contents of the ```gmd:title``` pointing to the [TG SDS](#ref_TG_SDS) are explicitly defined.

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
gmd | http://www.isotc211.org/2005/gmd
srv | http://www.isotc211.org/2005/srv
inspire\_sds_gmd | [missing]
xlink          | http://www.w3.org/1999/xlink
