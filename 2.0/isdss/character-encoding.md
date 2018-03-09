# Data Encoding 'dataset' or 'series'

**Purpose**: Evaluate encoding and the storage or transmission format of the provided data sets or data set series.

**Prerequisites**

* [resource-type](http://inspire.ec.europa.eu/id/ats/metadata/2.0/datasets-and-series/resource-type)

**Test method**
The coding (s) of characters in the data sets and data sets using non UTF-8 based 
encodings are checked from the element [Distribution Format](#distributionFormat).

The multiplicity of this element is one or more.

**Reference(s)**	 
* [TG MD](http://inspire.ec.europa.eu/id/ats/metadata/2.0/isdss/README#ref_TG_MD) 3.2.2.2, Req 2.5
* [ISO 10646](http://standards.iso.org/ittf/PubliclyAvailableStandards/index.html)
**Test type**: Automated

**Notes**
This element is mandatory only if an encoding is used that is not based on UTF-8.
If more than one character encoding is used within the described data set or data sets series, all used character 
encodings, including UTF-8 (code list value "utf8"), shall be given using this element.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://github.com/inspire-eu-validation/metadata/tree/2.0/2.0/isdss/README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| ------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="distributionFormat"></a> distributionFormat  | gmd:distributionInfo/\*/gmd:distributionFormat/gmd:MD_Format/text()