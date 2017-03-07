#4. Technical Specifications 

##4.1 Summary of Services 

This chapter provides more information on the technical specifications underpinning the Interoperability Framework components. The approach employed by the Framework is to promote the use of existing technical specifications and standards rather than to define new ones. The profiling work of Superstream, the European e-SENS project, CEN TC434 and BII Workshop as well as the OpenPEPPOL community have been evaluated as part of the Council’s implementation of these services. 

| | | |
| --- |------- |--------------- |
| Service |Component |Key Specifications |
**Message Delivery** | Access Point | A Council profile of the [OASIS version 1.0 of the Applicability Statement 4 (AS4) Profile of the ebXML Messaging Services (ebMS) 3.0 standard – ebMS3 AS4](http://docs.oasis-open.org/ebxml-msg/ebms/v3.0/profiles/AS4-profile/v1.0/os/AS4-profile-v1.0-os.html)|
**Business Discovery**  | Digital Capability Locator (DCL) | Council profile of the [OASIS Business Document Metadata Service Location Version 1.0 (SML) Version 1.0 committee specification](http://docs.oasis-open.org/bdxr/BDX-Location/v1.0/cs01/BDX-Location-v1.0-cs01.html)| 
 |Digital Capability Publisher (DCP)| Council profile of the [OASIS Service Metadata Publishing (SMP) Version 1.0 committee specification](http://docs.oasis-open.org/bdxr/bdx-smp/v1.0/cs01/bdx-smp-v1.0-cs01.html) |
                      | Business Identifiers| Council policy on the use of business identifiers |                    
**eInvoicing** | Semantic model | Council semantic model of the core elements of an electronic invoice  |     
               | Data Format | Council profile for [OASIS UBL 2.1](http://docs.oasis-open.org/ubl/os-UBL-2.1/UBL-2.1.html) |     
Table 1 - Summary of Technical Specifications 

The above specifications are all further described in the documents outlined in Section 5 and can be implemented using commercial or Open Source software. ##4.2 Service Details 

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

