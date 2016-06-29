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
 
 * special lists for benefits, components and features; specialization of ul, allowed everywhere where ul is allowed
 * special element for quotes; specialization of fig, allowed everywhere where fig is allowed

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



