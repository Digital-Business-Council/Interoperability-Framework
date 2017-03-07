# 3. The eInvoicing Interoperability framework

The Framework aims is to provide certainty on how a prescribed set of established open standards can be used to extend eInvoicing to all Australian businesses, minimise the cost of implementation for software providers and enhance business interactions (especially for micro to small businesses) by making invoicing an automatic digital interaction. 




## 3.1 What is it

The Council’s Interoperability Framework is based on the concept of standardising interconnections around what is called a ‘four corner model’. Similar models have emerged from the financial sector (for inter-bank interoperability), telecommunications sector (for global roaming) and are already being used in many countries for eInvoicing. In Australia, the superannuation sector (via Superstream) also uses a standardised form of the ‘four corner model’. 

Under this logical model, businesses can send messages : 
 - directly to each other by implementing their own Access Points (without intermediaries); 
 - via a mutual 3rd party Access Point (3-corners); or 
 - via two independent external service providers (4-corners). 

As the digital economy grows, the trend is toward the increased use of 4-corner models. However, as with rail networks, telephony systems and other communication technologies, unless standards are introduced, complex and expensive interconnections are required to connect all existing participants. The DBC Framework has proposed standards for the creation of an ‘open’ 4-corner model. 

A key requirement for the eInvoicing Interoperability Framework is that a Buyer’s or Supplier’s digital address and digital capabilities may change over time. The associated challenge with using an ‘open’ 4-corner model is finding out what businesses are reachable and what their digital capabilities are. The Framework resolves this by establishing a business discovery service. The idea of using the 4-corner model with business discovery is a well-established and an internationally accepted solution, and an extension to the existing Superstream model. 

Figure 1: The Four Corner model with Business Discovery applied to eInvoicing 

The actors involved in eInvoicing are: 

**Buyers:** The Buyer is the legal person or organisation who purchases goods or services;

**Suppliers:** The Supplier is the legal person or organisation who provides a good or service;

**Access Point:** A service (in-house or outsourced) that sends and receives eInvoices and passes them on to the respective participants;

**Digital Capability Locator:** A service for looking up the location of the Digital Capability Publisher for a Buyer or Supplier; and

**Digital Capability Publishers:** Providers of a service for Buyers and Suppliers to store details of their capabilities, and includes what scenarios they can process, the data formats they support and the delivery address for their eInvoices.

eInvoicing using the Framework means that the business applications of the Suppliers and Buyers (corners one and four) do not exchange invoices directly with each other but via Access Points (corners two and three). Any organisation (such as a Buyer or Supplier) has the choice of using a third party service provider to provide an Access Point or to implement their own.

Finally, the meaning of the information in eInvoices needs to be understood by all Buyers and Suppliers regardless of the natural business systems they use, so an agreed set of information elements in a standardised data format is required for exchanges between Access Points. 



## How does it work

Interoperability means working together – a collaboration of systems, services and people with common understanding. An interoperability framework can be defined as the overarching set of policies, standards and guidelines that describes how organisations have agreed, or should agree, to do business with each other.

There are four components to the Framework: 

**Legislation and policy:** Reducing legal or policy reasons why paper is preferred to digital. This includes recommending refinements to legislation and policy, if any, to remove impediments or barriers to adoption; 

**Organisational interoperability:** Describing business process scenarios and standardising how businesses discover each other’s digital capabilities for these scenarios;

**Semantic interoperability:** Standardising the data exchanged so the information is commonly understood by the parties involved; and

**Technical interoperability:** Technical standards and protocols to ensure information is exchanged securely and reliably between parties (directly or via service providers). 



## 3.3 Legislation and Policy
### 3.3.1 Legislation

The federal, state and local governments are reviewing legislation to identify and recommend opportunities to remove impediments or barriers to adoption. Any relevant changes are expected to be published by the respective Government. 

### 3.3.2 Policy

This Framework provides an opt-in solution and does not impact current elnvoicing solutions unless businesses choose to adopt it. This means new participants are not excluded from using or providing eInvoice services and existing eInvoice users or service providers are not excluded from future growth and development.

Within the public sector there is ongoing work within the three levels of government to introduce policies to encourage the use of digital technologies for eInvoicing. Any relevant policy changes for the public sector are expected to be published by the Government.

### 3.3.3 Agreements and charges

As part of the work to provide implementation guidance and ongoing governance of the framework the Council is expected to provide interoperability agreements for service providers so that: 
 - There is an appropriate approach to accreditation and service levels for service providers with periodic reviews; 
 -  There will be no charges for exchanging documents between Access Points; and 
 - There will be an open market for providing Access Points. 
 
## 3.4 Organisational Interoperability
### 3.4.1 Business Processes

The procurement, accounts payable, accounts receivable and sales processes of any buyers and suppliers are inextricably linked. Figure 2 shows that invoicing is one sub-process of this broader process. 

While there are significant benefits in digitising the whole end to end process, overseas evidence suggests it will be more effective and achieve broader market adoption by focussing on the invoice process as the first step. Eventually, as the ecosystem matures, the entire procure-to-pay process will be digitised (Penttinen, 2008). 

Figure 2 - Abbreviated procure to pay process

It is also recognised that procure to pay forms one part of an overall set of supply chain processes, such as the financial supply chain (dealing with banking/payment) and the logistical supply chain (dealing with receipt/delivery of the purchased items). Information flows into and out of these processes and so suitable interfaces will also be required. 

**Business scenarios**

The business processes introduced in this document are industry neutral and depict a generic cross-industry set of scenarios. 

**Scenario One: Invoicing (and Adjustment invoices)**

1.Supplier's business application to Supplier's Access Point (CORNERS ONE to TWO)
 
The Supplier’s business application (for example, an accounts receivable system) creates an invoice detailing purchase(s) made by the Buyer. The Supplier sends this invoice data to their Access Point.

2.Supplier's Access Point to Buyer's Access Point (CORNERS TWO to THREE)
 
The Supplier’s Access Point transforms the Supplier’s invoice data to the standardised eInvoice data format (if it is not already in that format). The Supplier’s Access Point then uses the Business Discovery service (defined later in this document) to determine the address of the Buyer’s Access Point before forwarding the eInvoice to that Access Point. 

3.Buyer's Access Point to Buyer's business application (CORNERS THREE to FOUR)
 
The Buyer’s Access Point transforms the eInvoice data format to the Buyer’s required format (if they differ) and delivers this to the Buyer’s business application (for example, their accounts payable system). 

4.[Optional] Buyer’s business application to Supplier’s business application (CORNERS FOUR to ONE) 
 
The Buyer may acknowledge when the invoice has been received. In which case: 

 - The Buyer’s business application verifies the invoice and sends some form of acknowledgement to their Access Point (CORNER THREE);
 - Buyer’s Access Point to Supplier’s Access Point (CORNERS THREE to TWO) 
   The Buyer’s Access Point transforms the Buyer’s acknowledgement into a standardised response message (if they differ), uses the
   Business Discovery service to discover the location of the Supplier’s Access Point and forwards the response message; and 
