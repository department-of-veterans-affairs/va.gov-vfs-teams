---
title: Obtaining Authority To Operate
label: ATO
---
<span style="color: red">
This needs to be further discussed as a group and refined for scalability, but here are some initial thoughts:
<br><br>Ad Hoc / DSVA probably shouldn’t handle or check for ATO. Anyone building things should probably be responsible for going through that whole process themselves and making sure they’re covered. All teams could build under one overarching ATO for the platform, but ensuring all products have appropriate ATO requirements met will be the responsibility of those building the products and an ATO Lead at VA.
</span>


### Contacts:
- **System Owner:** Angela Gant-Curtis, Deputy Portfolio Director, Office Phone: (540)760-7222, angela.gant-curtis@va.gov
- **ISO:** Griselda Gallegos, NDC AITC Information Security Officer (ISO), Office:(512) 326-6037, griselda.gallegos@va.gov
- **Privacy Officer:** Rita Grewal, Rita.Grewal@va.gov

## Steps for Obtaining a New Connection
1. Create new GitHub issue with [THIS TEMPLATE](https://github.com/department-of-veterans-affairs/vets.gov-ato/blob/master/assets/VetsGov%20ISAMOUs/NewConnectionTemplate.md)
2. Determine if you need an ISA MOU between Vets.gov and the New System.
  - You do not need a MOU if the AO for the system Vets.gov is connecting to is the same AO as Vets.gov - check [THIS](https://github.com/department-of-veterans-affairs/vets.gov-ato/blob/master/assets/Support%20Documents/System%20Names%20and%20AOs%20June%208%202017.xlsx) list
  - You do not need an MOU if the existing ISA/MOU covers all systems hosted within the VA accreditation boundary.  
  - [Create ISA MOU](https://github.com/department-of-veterans-affairs/vets.gov-ato/tree/master/assets/VetsGov%20ISAMOUs)
3. Determine if you need to update the PTA/PIA due to the data being transfered in the new connection.
  - If you need to update PTA/PIA, continue to [Update PTA/PIA](https://github.com/department-of-veterans-affairs/vets.gov-ato/tree/master/assets/PTA_PIA)
  - If you don't need to update the PTA/PIA, continue to [Submit ESCCB Request](https://github.com/department-of-veterans-affairs/vets.gov-ato/tree/master/assets/ESCCB)
4. Determine if you need to submit an ESCCB Request or a S2S Request
  - ESCCB requests are for creating new VPN connections and/or new or modifying port traffic.
  - S2S requests are for new connections back to VA Services over already approved ports.
  - [Submit ESCCB Request](https://github.com/department-of-veterans-affairs/vets.gov-ato/tree/master/assets/ESCCB)
  - [Submit S2S Request](https://github.com/department-of-veterans-affairs/vets.gov-ato/blob/master/assets/s2s/readme.md)
5. Uploade Signed Documents
   - Collect the above documents (ISA MOU, PTA, PIA, ESCCB Response) and upload to RiskVision
6. Provide approval and close ticket
   - Inform all parties involved of system and ISO approval to move to production
7. Close GitHub Issue created in [Step 1](https://github.com/department-of-veterans-affairs/vets.gov-ato/blob/master/assets/VetsGov%20ISAMOUs/README.md)
8. Update RiskVision if any controls need to be updated with any new information.

## Steps for Modifying an Existing Connection
Existing ISA MOUs should be modified, as-needed, when additional functionality/data is utilized from the system or IPs/URLs change.  For example, the current scope of MyHealtheVet is Secure Messaging and Prescription Refill -- beyond that you’ll likely need to update the ISA MOU. Run the draft by the existing system ISO before submitting for signatures.

- Existing editable and signed ISA MOUs should be [HERE](https://github.com/department-of-veterans-affairs/vets.gov-ato/tree/master/assets/VetsGov%20ISAMOUs) and final signed documents in RiskVision.
- Steps for updating existing MOU's can be found [HERE](https://github.com/department-of-veterans-affairs/vets.gov-ato/tree/master/assets/VetsGov%20ISAMOUs#modifying-existing-isa-mou)

## Steps for Making a Change in the System Description
- [System Description](https://github.com/department-of-veterans-affairs/vets.gov-ato/blob/master/System%20Description.md) can be updated when new connections have been made to back-end VA services.
- New data elements being added, used, stored? Ensure [Data.md](https://github.com/department-of-veterans-affairs/vets.gov-ato/blob/master/Data.md) is up to date.

## Steps for Updating Privacy Documentation
- Each time something new is added, especially data, the [Privacy Threat Analysis (PTA)](https://github.com/department-of-veterans-affairs/vets.gov-ato/tree/master/assets/PTA_PIA) and [Privacy Impact Analysis (PIA)](https://github.com/department-of-veterans-affairs/vets.gov-ato/tree/master/assets/PTA_PIA) need to be updated and approved by the Privacy Office (PIASupport@va.gov)
- Update the [vets.gov Privacy Statement](https://www.vets.gov/privacy/) according to steps [HERE](https://github.com/department-of-veterans-affairs/vets.gov-ato/tree/master/assets/PTA_PIA#updating-privacy-statement)

## Steps for Performing a Web Application Security Assessment (WASA)
- Each time major functionality is rolled out, a NEW WASA should be requested.  
- Steps for completing the WASA are found [HERE](https://github.com/department-of-veterans-affairs/vets.gov-ato/tree/master/assets/WASA)

## Steps for Creating the NESSUS Report
- NESSUS: Each month, the NESSUS report (devops team has access to this) needs to be uploaded to RiskVision, along with a remediation plan)
  - [Nessus Montly Scan Proceedures](https://github.com/department-of-veterans-affairs/vets.gov-ato/blob/master/assets/Nessus%20Scan%20Results/README.md)

## Steps for Updating RiskVision Findings
- RiskVision needs to be updated each time additional components are being rolled out.  Once you complete a section you submit it.  ISO can view them as they are submitted, but it can’t be moved through the workflow until all sections are submitted.
*`TO-DO: More details to be provided`*
- If you are experiencing an issue with RiskVision (aka GRC) send email to the helpdesk: vaGRCservicedesk@va.gov
- If you get jammed up on RiskVision/ATO items and ISO can’t help, reach out to Sandra Hedtke (Sandra.Hedtke@va.gov), she’s awesome.
