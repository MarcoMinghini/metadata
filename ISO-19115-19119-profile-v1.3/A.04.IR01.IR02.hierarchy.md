#A.04.IR01.IR02.hierarchy

**Purpose**: Checks that a resource type is provided

**Prerequisites**
* [A.01.validate](A.01.validate.md) must be passed

**Test method**

Checks if a resource type ([hierarchyLevel](#hierarchyLevel)) is provided and is taken from the list of [valid values](#validvalues), i.e. 'dataset', 'series' or 'service'.

# Context

**Reference(s)**	 

* [IR MD](./README.md#ref_IR_MD), Part B 1.3, Part D 1
* [TG MD](./README.md#ref_TG_MD),2.2.3, Req 1 & 2
* [ISO 19115](./README.md#ref_ISO_19115) table B.5.25 MD_ScopeCode 

**Test type:** Automated

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="validvalues"></a> valid values | doc(http://standards.iso.org/ittf/PubliclyAvailableStandards/ISO_19139_Schemas/resources/codelist/gmxCodelists.xml)//gmx:CodeListDictionary[@gml:id='MD_ScopeCode']//gml:identifier/text()