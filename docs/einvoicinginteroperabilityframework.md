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


![Fourcornermodel-Logo] (/images/Four-corner-model.PNG)

The actors involved in eInvoicing are: 

**Buyers:** The Buyer is the legal person or organisation who purchases goods or services;

**Suppliers:** The Supplier is the legal person or organisation who provides a good or service;

**Access Point:** A service (in-house or outsourced) that sends and receives eInvoices and passes them on to the respective participants;

**Digital Capability Locator:** A service for looking up the location of the Digital Capability Publisher for a Buyer or Supplier; and

**Digital Capability Publishers:** Providers of a service for Buyers and Suppliers to store details of their capabilities, and includes what scenarios they can process, the data formats they support and the delivery address for their eInvoices.

eInvoicing using the Framework means that the business applications of the Suppliers and Buyers (corners one and four) do not exchange invoices directly with each other but via Access Points (corners two and three). Any organisation (such as a Buyer or Supplier) has the choice of using a third party service provider to provide an Access Point or to implement their own.

Finally, the meaning of the information in eInvoices needs to be understood by all Buyers and Suppliers regardless of the natural business systems they use, so an agreed set of information elements in a standardised data format is required for exchanges between Access Points. 



## 3.2 How does it work

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

![Procuretopay-Logo](/images/Procure-to-pay.PNG)

It is also recognised that procure to pay forms one part of an overall set of supply chain processes, such as the financial supply chain (dealing with banking/payment) and the logistical supply chain (dealing with receipt/delivery of the purchased items). Information flows into and out of these processes and so suitable interfaces will also be required. 

#### Business scenarios

The business processes introduced in this document are industry neutral and depict a generic cross-industry set of scenarios. 

**Scenario One: Invoicing (and Adjustment invoices)**

1. **Supplier's business application to Supplier's Access Point (CORNERS ONE to TWO)**
   The Supplier’s business application (for example, an accounts receivable system) creates an invoice detailing purchase(s) made by the    Buyer. The Supplier sends this invoice data to their Access Point.

2. **Supplier's Access Point to Buyer's Access Point (CORNERS TWO to THREE)**
   The Supplier’s Access Point transforms the Supplier’s invoice data to the standardised eInvoice data format (if it is not already in    that format). The Supplier’s Access Point then uses the Business Discovery service (defined later in this document) to determine the    address of the Buyer’s Access Point before forwarding the eInvoice to that Access Point. 

3. **Buyer's Access Point to Buyer's business application (CORNERS THREE to FOUR)**
   The Buyer’s Access Point transforms the eInvoice data format to the Buyer’s required format (if they differ) and delivers this to the    Buyer’s business application (for example, their accounts payable system). 

4. **[Optional] Buyer’s business application to Supplier’s business application (CORNERS FOUR to ONE)** 
   The Buyer may acknowledge when the invoice has been received. In which case: 
   - The Buyer’s business application verifies the invoice and sends some form of acknowledgement to their Access Point (CORNER THREE);
   - Buyer’s Access Point to Supplier’s Access Point (CORNERS THREE to TWO)
   The Buyer’s Access Point transforms the Buyer’s acknowledgement into a standardised response message (if they differ), uses the
   Business Discovery service to discover the location of the Supplier’s Access Point and forwards the response message; and
   - Supplier’s Access Point to Supplier’s business application (CORNERS TWO to ONE)
   The Supplier’s Access Point transforms the response message into an acknowledgement format suitable for the Suppler (if required) and    forwards the acknowledgement to the Supplier. 
   
**Scenario Two: Recipient Created Tax Invoice (RCTI)**

With RCTIs a Tax Invoice is issued by the Party receiving the goods or services rather than the Supplier. For example, a sugar cane farmer and a mill, have entered into an agreement that the Buyer will Invoice and provide payment for a delivery of cane based on the quality of the cane. On a delivery of cane to the mill, the Buyer creates a Recipient Created Tax Invoice. 

1. **Buyer’s business application to Access Point (CORNERS ONE to TWO)**
   The Buyer’s business application creates a Recipient Created Tax Invoice detailing the purchase(s) made by the Buyer. The Buyer sends    the invoice to their Access Point. 
   
2. **Buyer's Access Point to Supplier's Access Point (CORNERS TWO to THREE)**
   The Buyer’s Access Point transforms the Buyer’s Invoice data to the standardised eInvoice data format (if they differ). The Buyer’s      Access Point then uses the Business Discovery service to discover the address of the Supplier’s Access Point before forwarding the    eInvoice to that Access Point. 

3. **Access Point to Supplier's business application (CORNERS THREE to FOUR)**
   The Supplier’s Access Point transforms the eInvoice data format to the Supplier’s required format (if they differ) and delivers this    to the Supplier’s business application (for example, their accounts receivable system). 

### 3.4.2 Business Identifier

A key consideration in the Framework is that all parties who may receive eInvoices (or Responses) need to be uniquely identified.

Business Identifiers are information elements that are used to establish the unique identity of businesses (organisations, agencies, branches within organisations, etc.) within the Framework. They are used to identify the parties (sender or receiver) for both business discovery and messaging exchanges. Business identifiers also appear within eInvoices themselves to identify parties such as the Supplier and Buyer. While it is common that the parties sending and receiving an eInvoice are also the Supplier and Buyer, it is not a requirement that they be so and different Business Identifiers may be used for these roles. 

### Framework Business Identifiers;
- Identify any Australian or international private and public sector recipient of digital documents (for example a Buyer) in a  standardised and platform independent way; 
- Allows multiple established identification schemes and scheme registries; and 
- Are encoded in a standardised and machine process-able data format. 

### 3.4.3 Business Discovery

Digital capability is the ability of an organisation to send and receive digital documents. The target for this digital capability is known as the digital address. For example, a Buyer will have a digital address if they are capable of receiving eInvoices. Delivering an eInvoice to their digital address will result in the Buyer be able to receive and process the eInvoice. 

The Business Discovery service is a means of determining a business’s digital address for a given type of document within a given process. For example, by supplying a Buyer’s business identifier, the type of document (eInvoice) and the process involved (eInvoicing), the Business Discovery service will determine the Buyer’s digital address for eInvoices. 

However the digital capabilities registered for a business will change as their services develop and migrate over time. For example, a recipient’s Access Point provider may allocate their digital addresses. A benefit of the open Framework is the freedom for businesses to connect with any Access Point provider, or even establish their own Access Points. And so these addresses may change if the Access Point changes and this impacts the registered digital capability of the recipient. 

Because of these continually changing details it is necessary to dynamically discover the current digital addresses of recipients. The finer details of the Business Discovery service are discussed later the Technical Interoperability section. 

## 3.5 Semantic Interoperability
### 3.5.1 How does semantic interoperability help eInvoicing

Semantic interoperability is the ability for different business applications (in this case those of Buyers and Suppliers) to recognise and process the information they exchange. 

However businesses operate in different industry, geopolitical, and regulatory contexts that may necessitate different rules and requirements for the information exchanged in an invoice. Consequently, most trading communities and businesses use differing forms of invoices. Transforming the data to suit different contexts is usually required when two parties using different invoice models or formats (for example, between two different communities) need to trade. Such transformations may be a complex and expensive process prone to misinterpretations. As many Suppliers (and Buyers) trade with many different communities this complexity is common and yet another barrier to eInvoicing. 

One proven approach to enabling greater interoperability is to agree upon a collection of terms with well-defined meanings that are consistent across all contexts of use. This is called the semantic model of the core elements. 

A semantic model is based on the idea that common pieces of information used in an invoice may have many names, use different terminology and be expressed in different ways, but the meanings are constant and commonly understood. Semantic models help us identify what the common pieces of information mean without the distraction of how we express this. This is similar to how drawing pictures helps people who don’t speak a common language to communicate.

The semantic model is an attempt to remove the language/syntax/grammar/format from information to enable us to compare one thing with another and see if they are describing the same thing. In the software world this is very useful because: 

- Technology is constantly evolving and standardising on the semantics ensures the invoice information that is standardised does not need  
- When transforming an invoice between various formats the mappint of information is easier for software developers if there is a common semantic model to ference.

### 3.5.2 The Core eInvoice Semantic Model

The Core eInvoice Semantic Model consists of a dictionary of terms, concepts used, the minimal content of a document, the rules validating the content, the use of identifiers, and code lists. Adopting a single common semantic model promotes reliable information exchange and ensures technology neutrality. It is also easier and cheaper for enterprises to subscribe to a single model as compared to several. 

### The Semantic Model:

 - Incorporates invoice requirements for regulatory e.g. tax, commercial, technical, financial, and industry extensions; 
 - Will be aligned with the Australian Reporting Dictionary (through incorporation); 
 - Identifies the common case model; 
 - Consistent reuse of standardised definitions and meanings pro
 - Makes use of a proven methodology; and 
 - The semantic model has been defined and elaborated in a consultative manner – reusing an existing international standard. 
 
### 3.5.3 Digital Data Format

The Core eInvoice Semantic Model in itself does not enable software developers to create the necessary eInvoice data files to exchange. The semantic model needs to be expressed in a standardised digital data format. The term data format is used to mean the software expression of the information described by the semantic model (also called the message syntax or markup language). In the data format all the data elements, concepts and validation rules defined in the semantic model are expressed in ways computer applications can process. 

It may help to remember that the semantic model is for business people to understand while the digital data format is for software developers to understand and computer programs to process. 

**The eInvoicing data format:**

 - Is based on an international standard; 
 - Is aligned with relevant and established international standards. Australian standards and practices will only be adopted where international standards are not applicable; 
 - Encompasses procure to pay documents: 
 - Will not inhibit the future extension to other elements of the procure to pay process; 
 - Has a published semantic model; 
 - Will not impose a particular design on internal solutions for stakeholders; 
 - Has an established user base; 
 - Has open participation and governance; 
 - Is open, royalty free and vendor agnostic; 
 - Allows development of tools that are easily available; 
 - Has interfaces with common business applications; and 
 - Enables business to business (B2B) connectivity irrespective of platform or solution to exchange electronic business transactions.
 
## 3.6 Technical Interoperability
### 3.6.1 eDelivery

Technical interoperability facilitates an open trading partner network where: 
 - Any Buyer and Supplier will be able to: 
  - Send recognised digital documents to any registered trading partner through a network of approved Access Points; and
 - All Access Points will:
  - Conform to the same sets of standards and business service rules; 
  - Be secured, by conforming to the trust mechanism between Access Points; 
  - Exchange digital documents with other Access Points using the Council approved Data Format; 
  - Provide interoperability of data exchanged by supporting a common semantic model, that can be used to transform different formats as required; 
  - Derive the digital address of the eInvoice recipient through the Business Discovery service; and 
  - Access the Business Discovery service independent of the document exchange protocol to ensure other protocols may be supported in future. 
  
eDelivery will create a community of federated Access Points that are all conformant to the same technical requirements and therefore capable of interacting with each other. As a result, businesses that have developed business systems independently from each other or implemented commercially-off-the-shelf (COTS) solutions/services can reliably and securely exchange digital business documents.

A greater return on investment is possible as eDelivery is document agnostic, meaning users can potentially transfer any Council endorsed structured or unstructured documents between Access Points. 

The components of eDelivery include business discovery, message delivery and trust enablement. 

### 3.6.2 Business Discovery

Two services are provided to achieve dynamic and adaptable business discovery: 
 - Digital Capability Locator (DCL)
   
   DCL lookup enables a sending Access Point to dynamically discover the digital address of the recipient's Digital Capability Publisher (using their business identifier); and
   
 - Digital Capability Publishers (DCP)
 
   The sending Access Point will then use the DCP's address to discover the digital capabilities (such as digital address, document types, processes and message protocals supported) of the reicpient.
   
### Business discovery will:
 - Achieve interoperability and accessibility – as information about participants (delivery addresses and transactions supported) will be easily discoverable and accessible to all parties in the framework; 
 - Support the expansion of the eDelivery network by allowing new businesses to join in a flexible manner; and 
 - Provide the ability to switch or change recipient addressing information when required. 

### 3.6.3 Message Delivery

Message Delivery enables the exchange of any digital documents (such as eInvoices) between two Access Points in an interoperable, secure, reliable and trusted way.

Access Points implement the Message Delivery profile and ensure that data is sent and received reliably and securely. 

The Message Delivery profile has the following features:
 - Interoperability:
  - Is based on an established international standard;
  - Will support the four-corner model;
  - Will also support a three-corner model (two businesses using the same third party access point);
  - Is not dependent on the format or content of the document delivered; and
  - Allows interaction to occur asynchronously, i.e. the receieving party can be offline;
 - Security:
  - Ensures the integrity of transmissions is preserved, such that a transmission cannot be tampered with;
  - Supports the encryption to preserve confidentiality; and
  - Ensures the origin and destination Access Points are trusted;
 - Reliability:
  - Guarantees the data and documents are delivered once and only once;
  - Provides certainty that the data and documents are delivered; and
  - Ensures non-redpudiation of receipt and origin of every exchange; and
 - Scalability and Performance:
  - Adapts to an increasing number of Access Points;
  - Allows for large documents to be transmitted; and
  - Supports high throughputs
  
### 3.6.4 Trust Enablement

The current Framework establishes a trusted environment between accredited Access Points3 (corners 2 and 3). Future development may also include creating a trust domain for end-to-end authentication if required. 

The trust model:
 - Leverages the strength of Public Key Infrastructure for security and confidentiality; 
 - Overcomes the complexity and scalability issues with traditional digital certificate based public key infrastructure; 
 - Provides freedom of choice to Access Points to maximise use of current investments; and 
 - Provides a viable solution until there is a national digital credential initiative, which may take time to develop and implement. 
 
The approach taken is to leverage the experiences and successes of both local and international networks (for example, services such as PEPPOL, e-SENS and Superstream) to:
 - Establish strong governance under the auspices of the Council. This would include Digital Capability Publisher and Access Point provider interoperability agreements, binding implementation practices, testing and certification arrangements; 
 - Ensure Business Discovery only supplies details of accredited Digital Capability Publishers and Access Point providers;
 - Use digital certificates to ensure confidentiality between Access Points and to validate that messages are only received from accredited Access Points. It should be noted the mutual exchange of certificates is a widely used simple implementation of the Direct Trust Model. Due to the limited scalability of mutual certificate exchange, the approach of recording public keys with the Council’s centralised register of accredited service providers (updated during the accreditation process) is prescribed. To cater for business application level trust a similar model could potentially be used, with the storage of a business certificate in its Digital Capability Publisher; and 
 - Allow businesses to have a choice of accredited Digital Capability Publishers and Access Points, with businesses also being able to choose to implement their own accredited Access Points and Digital Capability Publishers. 
