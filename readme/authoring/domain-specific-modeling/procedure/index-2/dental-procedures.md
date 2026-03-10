# Dental procedures

### Multi-step Procedures

While many dental procedures are performed by completing a series of individual steps, the descriptions and modeling of the complete or comprehensive procedure should simply outline the core steps. These are steps that are necessarily true in order to describe the concept. Steps that are part of a protocol, but not necessary, should not be included. Multi-step procedures may be performed in one clinical session or split over several sessions. Where possible, a definition should be added to new concepts of this type.

* For example,&#x20;
  * In the following concept 1381619006 |Preparation and obturation of root canal of tooth using root canal filling material (procedure)|, _preparation_ and _obturation_ describe the core steps. Irrigation, which often is part of the protocol, is not included.

<figure><img src="../../../../../.gitbook/assets/Prep and obturation.png" alt=""><figcaption></figcaption></figure>

Individual procedural steps can be modeled as separate concepts when required by a use case, for example, 234707000 |Root canal preparation (procedure)|.

### Restorative Procedures

For restorative procedures, descriptions should follow the format: Restoration of tooth by insertion of \[substance or device].&#x20;

* For example,&#x20;
  * 1381884009 |Direct restoration of tooth by insertion of composite dental material (procedure)|

<figure><img src="../../../../../.gitbook/assets/Direct restoration.png" alt=""><figcaption></figcaption></figure>

### Tooth vs Teeth

Procedures on a tooth should be modeled with 38199008 |Tooth structure (body structure)| and state _tooth_ in descriptions.&#x20;

* For example,&#x20;
  * 1259948005 |Repair of fissure sealant on tooth (procedure)|

Where a procedure acts on multiple teeth, these concepts should be modeled with 245543004 |Structure of dentition (body structure)| and state _teeth_ in descriptions.&#x20;

* For example,&#x20;
  * 1260193009 |Removal of accretion from teeth using dental scaler (procedure)|

<br>
