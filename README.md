# lwditamarketing

Defines a DITA-OT plugin containing LW DITA specializations for marketing material.


## Installation

* Checkout this repository in ```{DITA_OT_PATH}/plugins/lwditamarketing```
* Require plugin="lwditabaseschema"
* From ```{DITA_OT_PATH}``` run ```ant -f integrator.xml```


## Author information

The lwditamarketing has been developed by Eva de Haas (FontoXML), Birgit Strackenbrock (XStructuring) and others.


## Revision history

* 0.1 Initial version


## Base choices

* Marketing use case 'product sheet' - different examples

* LW DITA - Generated LW DITA XSD's with Oxygen, stored in ```{DITA_OT_PATH}/plugins/lwditabaseschema```

* Using XML schema - lwmarketing specialization XSD's

* Topic approach - Definition of different topic types for special information within a product sheet


## Schema documentation topic approach

### Marketing topic types (based on topic/topic)

* benefittopic - Describes one or more benefits of a product

* contacttopic - Contains the contact information of the product vendor

* highlighttopic - Describes one or more highlights of a product

* legatopic - Contains all legal information e.g. the disclaimer or copyright

* overviewtopic - Gives a short overview over the product

* specificationtopic - Contains the infotrmation about one or more features and/or other specific information about the product.

* titletopic - Contains the main title of the product sheet and other title page and/or frontmatter information

* vendottopic - Contains information about the vendor of the product

### Special section elements (based on topic/section)

* benefitsection - Special section for one benefit
 
* contactsection - Special section for contact information, contains special elements for e.g. company, address, phone number or website

* disclaimer - Special section for the disclaimer

* legalsection - Special setion for other legal information than the disclaimer e.g. copyright

* specificaationsection - Special section which contains more special information abput the product or a product feature

* frontmattersection - Special sesection which contains other frontmatter information than publication date or revision number

### Other specialized elements

* highlight - Contains one highlight, not a rich benefit or feature; (based on topic/p)

* copyright - Container for the copyright information; (based on topic/p)

* copyrightyear - Date since protection is active; (based on topic/ph)

* copyrightholder - Holder of the copyright; (based on topic/ph)

* components - Container for components with name and short description (based on topic/dl)

* component - Container for name and short description of a component (based on topic/dlentry)

* componentterm - Name/term of a component (based on topic/dt)

* componentdef - Short description/definition of a component (based on topic/dd)

* contactcompany, contactname, contactaddress, contactnumber, contactemail, contactwebsite, contactadditionalinfo - Special elements for the contact information  (all based on topic/p)

* featurelist - Special list for/overview of features (based on topic/ul)

* featurefig - Container for assets specific for one feature or a featuretable (based on topic/fig)

* featuretable - Special table for features (based on topic/simpletable)

* subtitle - Subtitle of the product sheet (based on topic/shortdesc)

* revision - Information about the product sheet, revision number (based on topic/p)

* pubdate - Date when product sheet is publicated (based on topic/p)

* productfig - Special figure which contains a figure of the product (based on topic/fig)

## Schema documentation domain approach

The following domains are added to the schema. Plus a outputclass attribute domain that adds a outputclass attribute to each element.

### Marketing domain

* actionitem - is a call to action element. Use the href attribute to link a action (based on topic/p)
* features - a list of features (based on topic/ul)
  * featureitem - contains the feature itself and possible a description (based on topic/li)
    * feature - contains the feature name (based on topic/p)
* highlights - a list of highlights (based on topic/fig)
  * highlight - a short description of this highlight (based on topic/p) 
* specifications - a list of specifications (based on topic/ul)
  * specificationitem - contains the specification itself and possible a description (based on topic/li)
    * specification - contains the specification name (or component name)(based on topic/p)
    
### Inline marketing domain

* brand - a inline element to tag a brand (based on topic/xref)
* category - a inline element to tag a category (based on topic/xref)
* company - a inline element to tag a company (based on topic/xref)
* product - a inline element to tag a product name (based on topic/xref)

### Metadata attribute domain

The following attributes are added to all elements.

* productapplicability
* lineofbusinessapplicability
* audience
* applications
* context

### Quote domain

* longquote - is used to quote on block level from a external document, the source of this external quote is contained by quotesource (based on topic/fig)
  * longquotesource - is used to contain the source of the quote. Some parts of the quote can be tagged by following elements and/or some source information can be contained by attributes with corresponding names as the following elements (based on topic/p)
    * sourcename (based on topic/ph)
    * sourcerole (based on topic/ph)
    * sourcecompany (based on topic/ph)
    * sourcepublication (based on topic/ph)
    * sourceyear (based on topic/ph)
    * sourceother - is used to contain other source information. With the type attribute you can specify what type of other source information this is (based on topic/ph)
* pullquote - is used to quote on block level from the current document (based on topic/fig)
* quote - is a inline quote from a external docuement, the source of this external quote is contained by quotesource (based on topic/ph)
  * quotesource - the source of a quote is contained by this element. Other information about the source of the quote, can be contained by the attribues: name, role, company, publication, year, other (based on topic/data)

## License

Copyright 2016 Eva de Haas (FontoXML), Birgit Strackenbrock (XStructuring), and contributors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at
[http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)
Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.


## Open Questions

* Choice to use a map-topic approach. Would be an approach with nested topics e.g. product sheet topics in which the special topics can appear more desirable? Or an product sheet topic with special sections? 

* Do we also need DTD's and/or RELAX NG schema's?


## To do

* Develope DITA OT stylesheets

* Compare/align with case study specialization of IBM for DITA

* Compare with schema.org/product and make mapping between both schema's

* Create more examples > everybody is welcome to do so



