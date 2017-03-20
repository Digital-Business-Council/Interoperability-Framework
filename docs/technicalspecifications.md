#4. Technical Specifications 

##4.1 Summary of Services 

This chapter provides more information on the technical specifications underpinning the Interoperability Framework components. The approach employed by the Framework is to promote the use of existing technical specifications and standards rather than to define new ones. The profiling work of Superstream, the European e-SENS project, CEN TC434 and BII Workshop as well as the OpenPEPPOL community have been evaluated as part of the Council’s implementation of these services. 

Service | Component | Key Specifications
--- | --- | ---
**Message Delivery** | Access Point | A Council profile of the [OASIS version 1.0 of the Applicability Statement 4 (AS4) Profile of the ebXML Messaging Services (ebMS) 3.0 standard – ebMS3 AS4](http://docs.oasis-open.org/ebxml-msg/ebms/v3.0/profiles/AS4-profile/v1.0/os/AS4-profile-v1.0-os.html)
**Business Discovery**  | Digital Capability Locator (DCL) | Council profile of the [OASIS Business Document Metadata Service Location Version 1.0 (SML) Version 1.0 committee specification](http://docs.oasis-open.org/bdxr/BDX-Location/v1.0/cs01/BDX-Location-v1.0-cs01.html)
| Digital Capability Publisher (DCP) | Council profile of the [OASIS Service Metadata Publishing (SMP) Version 1.0 committee specification](http://docs.oasis-open.org/bdxr/bdx-smp/v1.0/cs01/bdx-smp-v1.0-cs01.html) 
| Business Identifiers | Council policy on the use of business identifiers               
**eInvoicing** | Semantic model | Council semantic model of the core elements of an electronic invoice  |     
| Data Format | Council profile for [OASIS UBL 2.1](http://docs.oasis-open.org/ubl/os-UBL-2.1/UBL-2.1.html) 

*Table 1 - Summary of Technical Specifications* 

The above specifications are all further described in the documents outlined in Section 5 and can be implemented using commercial or Open Source software.

##4.2 Service Details 

###4.2.1 Message Delivery – Access Point 

To achieve interoperability between participants in an electronic messaging network, the sending and receiving Access Points must use the same messaging protocol. A published profile for electronic messaging provides a common specification for solution providers. This ensures compatibility between implementations and increases the market for solutions providers. 

The profile for Message Delivery is based on the AS4 Conformance Profile of the OASIS ebMS 3.0 standard and is a subset of the ebHandler profile. As such this profile: 

1. Does not require implementation of any unnecessary features of ebMS3/AS4. For example, only the basic store and forward                 functionality should be required; and 
2. Does not implement advanced ebMS3/AS4 features (such as security and reliability), which may be more effectively addressed at the 
    payload level through the use of a standardised business document envelope structure. 

ebMS3/AS4 has emerged as the strategic standard for a number of initiatives around the world including: 

- e-Justice Communication via Online data exchange (e-codex), now evolved into e-SENS; 
 - Electronic Exchange of Social Security Information (EESSI); 
 - European Network of Transmission System Operators for Gas (ENTSOG); 
 - European test bed for the maritime common information sharing environment in the 2020 perspective (EUCISE); 
 - International Air Transport Association (IATA); and 
 - The Australian standard for processing superannuation data and payments electronically (SuperStream). 
 
Implementations of the ebMS3/AS4 are available in both Open and Closed Source format and products can be certified to ensure strict adherence to the specification.

###4.2.2 Business Discovery – Digital Capability Publisher 

A Digital Capability Publisher (DCP) identifies a business’ capabilities for receiving digital documents (such as eInvoices). These capabilities include what processes and data formats they support and the digital address for delivering documents. Additional metadata information may be required to facilitate establishing mutual trust between businesses. 

The OASIS Service Metadata Publishing (SMP) specification describes a solution that is fit for purpose and specifically addresses the concerns for a business' metadata registry. SMP has been published as an OASIS Committee Specification and has been proven in established European environments (such as PEPPOL). This standard has also been adopted by e-SENS as one of their e-Delivery building blocks. Open source components are available4 and there are over 35 implementations within the PEPPOL and e-SENS communities. 

It is expected that the DCP profile will be implemented by number of DCP providers. Having multiple providers will allow the network to scale as the number of registered businesses and capabilities increases. DCP providers will need to make their own decisions on whether to implement the specification independently or use an open source component. DCP providers and the businesses they register are responsible for the privacy and integrity of their own capability information. 

###4.2.3 Business Discovery – Digital Capability Locator 

As it is expected that there will be many DCPs another service is required to establish which DCP is used by which business identifier. The Digital Capability Locator (DCL) is a master index that associates a business identifier with the DCP containing the relevant digital capabilities of the business. There is only one DCL in the eDelivery framework. Access Points query this DCL to find which DCP they subsequently query to obtain the correct digital address for the document to be sent. 

Business Discovery uses the OASIS Business Document Metadata Service Location Committee Specification (referred to as Service Metadata Locator or SML). The SML specification defines service discovery method values for use in Domain Name System (DNS) resource records. It is an application of the more generic Dynamic Delegation Discovery Services (DDDS) as defined in multiple RFCs. DNS is critical to internet and telephony services, which need a readily available, highly reliable and a proven, lightweight and distributed solution. 

As SML uses standard DNS, several implementation options are available including open source. SML was developed as part of PEPPOL transport infrastructure service and has subsequently been published by OASIS as a Committee Specification. The OASIS specification has now been adopted by e-SENS as part of their e-Delivery building block. 

To ensure availability, accuracy, efficiency and adherence to the specification, the eDelivery DCL requires a separate, formalised governance model with associated testing and certification. 

###4.2.4 Business Discovery – Business Identifiers 

A key consideration is that parties exchanging eInvoices (businesses) need to be uniquely identified within the Interoperability Framework. The Council’s Business Identifier policy establishes a scheme for uniquely identifying parties where a business identifier is a combination of: 

1. An issuing agency code from a controlled set for identification schemes, using [International Code Designators (ISO/IEC 6523)](http://www.cyber-identity.com/iso6523); and 
2. A value provided by the issuing agency 

To ensure global uniqueness the business identifier value needs to be valid with respect to the authoritative source of the relevant International Code Designator. The Framework does not proscribe a specific identification schema and businesses may choose the most appropriate for their environment that satisfies the Council’s Business Identifier policy. 

If the receiving business is registered in Australia the business identifier would most likely be their Australian Business Number (ABN) and the issuing agency will be the ABR. 

The use of ABN for the Australian business identifier will benefit the business-to-business community because: 

 - All eligible businesses are entitled to register for an ABN at no charge; 
 - The ABN is recognised as the legal business identifier in Australia; 
 - The ABN is currently required in Australian tax invoices; 
 - There exists a centralised, trusted registrar for ABNs that has implemented the necessary governance to protect the integrity of the registration process; and 
 - The Australian Business Register has a registered International Code Designator. 

However, there are at least two scenarios where the ABN may not suffice: 

 1. Australian business that operating separate business units (under the same ABN) and may require different digital addresses for  different eInvoices; or 
 2. If the receiving business is not registered in Australia. 

In these scenarios the issuing agency can be chosen from [the ICD set of ISO/IEC 6523](http://www.cyber-identity.com/iso6523) and the identifier can be a member of that identification scheme (such as a GLN, DUNS, etc.). 

###4.2.5 eInvoicing – Semantic Model 

The semantic model of the core elements of an eInvoice defines the information elements and business rules for the taxation, verification, matching and payment requirements for eInvoicing. 

It follows a proven approach based on the European standardisation work undertaken by the CEN BII Workshop and CEN Technical Committee 434 in their publication ‘Electronic invoicing - Semantic data model of the core elements of an electronic invoice’ [(prEN 16931)](http://standards.cen.eu/dyn/www/f?p=204:110:0::::FSP_PROJECT,FSP_LANG_ID:60602,25&cs=1EDAF8ACA5277C7EF32DC6EFAEF077D41). Following the same approach will also aid in aligning Australian and European implementations. 
The European model has been adapted for Australian requirements. 

###4.2.6 eInvoicing – Data Format 

Adopting a common eInvoice data format will simplify the effort and minimise the cost of establishing Access Points. This is because if all eInvoices have the same data format when exchanged between Access Points only one interface needs to be supported. 

The complexity (and cost and therefore barriers to entry) rises exponentially with every additional data format used. The use of one common format between Access Points (regardless of the business applications involved) is a significant factor in the Council’s Interoperability Framework that separates it from being just another eInvoice solution. 

The eInvoicing data format is based on the international, royalty free, open standard known as the [OASIS UBL 2.1 Invoice](http://docs.oasis-open.org/ubl/os-UBL-2.1/UBL-2.1.html#T-INVOICE). UBL 2.1 is also a joint publication of ISO and IEC known as ISO/IEC 19845:2015 ‘Information technology - Universal business language version 2.1 (UBL v2.1)’. 

UBL Invoice has been implemented by 15 governments in Europe (and also between EU member states) as well as the governments of Turkey, Peru, Colombia and Panama. CEN TC 434 has also prepared bindings (mappings) of their semantic model to the UBL 2.1 Invoice data format. In many cases UBL 2.1 Invoice data format has been use in conjunction with legacy EDI formats (such as UN/EDIFACT). In these scenarios EDIFACT data formats are supported by customising the UBL Extension structure. 

A large amount of XML software is available that can be configured for use with UBL 2.1. A partial list of UBL applications is published at: http://ubl.xml.org/products. 

The eInvoice Profile of the UBL 2.1 Invoice has been customised to support common Australian business requirements. However, instances of these eInvoices are all conformant to the common UBL 2.1 standard as used in other parts of the world. 

####Payments Interface

UBL 2.1 is also designed to support basic trade financing practices (invoice financing, factoring, pre-shipment/ order financing, letter of credit, etc.). The UBL standard covers the full procure to pay lifecycle and the UBL Remittance Advice is used to transmit the details of complex remittance information associated with the finance transactions such as the ISO 20022 payment initiation process. UBL is not intended to address any multi-stage payment events such as those planned in the New Payments Platform (NPP). To address the interface between the commercial procure-to-pay and the financial payment processes, UBL 2.1 has been enhanced to support the financial information required for downstream processing of Invoices within financial services. 

By aligning information models, business vocabularies such as UBL for eInvoicing and ISO 20022 for the NPP can enable Straight Through Processing (STP) and paperless trading along the entire Financial Supply Chain. For example, the UBL Invoice and Remittance Advice can be used together with financial messages to ensure end-to-end transport of reconciliation identifiers (invoicing party references). In particular, UBL provides a solution for advanced external remittance, where the UBL Remittance Advice is used to transmit the details of complex remittance information associated with the ISO 20022 payment initiation process. 
