# Database for Declaration
Contains tables, views, configuration file and input files related to personal interest declaration form, corporate interest declaration form. The forms are dynamic, each question having multiple options fetching values of options from backend tables. Any change in these tables will be reflected on forms. 

## Tables Used:
### 1) Corporate Interest Declaration Form

- **corporateinterest.DBCIFReason**
  - ***Description***: associated with Form Question "Reasons for the conflict"
  - ***Fields***: CIFReasonId, CIFReasonDescInput, CIFReasonDescOutput
  - ***Configuration File***: load/configuration/piciui/coi.hdbtabledata
  - ***Input File***: load/configuration/piciui/Reason.csv
  - ![image](https://github.deutsche-boerse.de/storage/user/3147/files/f0aa2b80-ac1b-11ea-9ab4-bbfeb0331438)
  
- **corporateinterest.CorporateInterest**
  - ***Description***: to store user inputs from CI form
  - ***Fields***: ReferenceId, RequestorFirstName, RequestorLastName, DBCIFInvolvement, DBCIFParty, DBCIFPartyOther,  DBCIFOtherParty, DBCIFReason, DBCIFReason, DBCIFTopic, DBCIFPStartDate, DBCIFPEndDate, DBCIFPAddInfos, DBPIFAttachment,                           DBPIFConfirmation, SubmissionDate.
             
- **corporateinterest.COI_CorporateInterest**
  - ***Description***: additional table for future requirements
  - ***Fields***: ReferenceId
  
### 2) Personal Interest Declaration Form

- **PersonalInterestForm.CompanyDetails**
  - ***Description***: associated with Form Question related "Companies"
  - ***Section***: General
  - ***Fields***: CompanyId, CompanyDescInput, CompanyDescOutput
  - ***Configuration File***: load/configuration/PersonalInterestForm/declaration.hdbtabledata
  - ***Input File***: load/configuration/PersonalInterestForm/CompanyDetails.csv
  - ![image](https://github.deutsche-boerse.de/storage/user/3147/files/061f5580-ac1c-11ea-9c29-ff504f53bc14)
  
- **PersonalInterestForm.KindOfInterestTT**
  - ***Description***: associated with Form Question related "Kind of Personal Interest"
  - ***Section***: General
  - ***Fields***: KindOfPIId, KindOfDescription, KindOfDescriptionOutput
  - ***Configuration File***: load/configuration/PersonalInterestForm/declaration.hdbtabledata
  - ***Input File***: load/configuration/PersonalInterestForm/KindOfInterestTT.csv
  - ![image](https://github.deutsche-boerse.de/storage/user/3147/files/294a0500-ac1c-11ea-8f95-46788aff9175)

- **PersonalInterestForm.Dormant**
  - ***Description***: associated with Form Question related "Dormant Organization"
  - ***Section***: Section 2(PI - Board Members)
  - ***Fields***: DormantId, DormantDescriptionInput, DormantDescriptionOutput
  - ***Configuration File***: load/configuration/PersonalInterestForm/declaration.hdbtabledata
  - ***Input File***: load/configuration/PersonalInterestForm/Dormant.csv
  - ![image](https://github.deutsche-boerse.de/storage/user/3147/files/4383e300-ac1c-11ea-9dcf-e0239ee47483)
  
 - **PersonalInterestForm.PersonalPositionDetails**
   - ***Description***: associated with Form Question related "Position / function / title / role"
   - ***Section***: Section 3(PI - Board Members)
   - ***Fields***: PersonalPositionDetId, PersonalPositionDescInput, PersonalPositionDescOutput
   - ***Configuration File***: load/configuration/PersonalInterestForm/declaration.hdbtabledata
   - ***Input File***: load/configuration/PersonalInterestForm/PersonalPositionDetails.csv
   - ![image](https://github.deutsche-boerse.de/storage/user/3147/files/f999fd80-ac19-11ea-9acd-a922079fa57e)
  
  - **PersonalInterestForm.PersonalPositionDetailsOther**
    - ***Description***: associated with Form Question related "Position / function / title / role"
    - ***Section***: Section 3(PI - Employee)
    - ***Fields***: PersonalPositionDetId, PersonalPositionDescInput, PersonalPositionDescOutput
    - ***Configuration File***: load/configuration/PersonalInterestForm/declaration.hdbtabledata
    - ***Input File***: load/configuration/PersonalInterestForm/PositionDetailsOther.csv
    - ![image](https://github.deutsche-boerse.de/storage/user/3147/files/f999fd80-ac19-11ea-9acd-a922079fa57e)
  
- **PersonalInterestForm.Membership**
    - ***Description***: associated with Form Question related "Membership"
    - ***Section***: Section 3(PI - Board Member)
    - ***Fields***: MembershipId, MembershipDescriptionInput, MembershipDescriptionOutput
    - ***Configuration File***: load/configuration/PersonalInterestForm/declaration.hdbtabledata
    - ***Input File***: load/configuration/PersonalInterestForm/Membership.csv
    - ![image](https://github.deutsche-boerse.de/storage/user/3147/files/416c5500-ac19-11ea-97ce-8f0f4026f794)

- **PersonalInterestForm.TypeOfPersonalInterest**
    - ***Description***: associated with Form Question related "Type of Personal Interest"
    - ***Section***: Section 3(PI - Employee, Student)
    - ***Fields***: TypePersonalInterestId, TypePersonalInterestDescriptionInput, TypePersonalInterestDescriptionOutput
    - ***Configuration File***: load/configuration/PersonalInterestForm/declaration.hdbtabledata
    - ***Input File***: load/configuration/PersonalInterestForm/TypeOfPersonalInterest.csv
    - ![image](https://github.deutsche-boerse.de/storage/user/3147/files/52699600-ac1a-11ea-9de1-7b5104ec3a0e)
    
- **PersonalInterestForm.TypeOfPersonalInterestBoard**
   - ***Description***: associated with Form Question related "Type of Personal Interest"
   - ***Section***: Section 3(PI - Board Member)
   - ***Fields***: TypePersonalInterestId, TypePersonalInterestDescriptionInput, TypePersonalInterestDescriptionOutput
   - ***Configuration File***: load/configuration/PersonalInterestForm/declaration.hdbtabledata
   - ***Input File***: load/configuration/PersonalInterestForm/TypeOfPersonalInterestBoard.csv
   - ![image](https://github.deutsche-boerse.de/storage/user/3147/files/52699600-ac1a-11ea-9de1-7b5104ec3a0e)
    
- **PersonalInterestForm.PurposePI**
    - ***Description***: associated with Form Question related "Purpose"
    - ***Section***: Section 3(PI - Board Member)
    - ***Fields***: PurposePIId, PurposePIDescInput, PurposePIDescOutput
    - ***Configuration File***: load/configuration/PersonalInterestForm/declaration.hdbtabledata
    - ***Input File***: load/configuration/PersonalInterestForm/PurposePI.csv
    - ![image](https://github.deutsche-boerse.de/storage/user/3147/files/ab85f980-ac1b-11ea-8d2d-a748a4b8114d)
    
 - **PersonalInterestForm.LinkPI**
    - ***Description***: associated with Form Question related "Link between PI and interest of DBG"
    - ***Section***: Section 4(PI - Board Member, Employee)
    - ***Fields***: LinkPIId, LinkPIDescriptionInput, LinkPIDescriptionOutput
    - ***Configuration File***: load/configuration/PersonalInterestForm/declaration.hdbtabledata
    - ***Input File***: load/configuration/PersonalInterestForm/LinkPI.csv
    - ![image](https://github.deutsche-boerse.de/storage/user/3147/files/3dd9cd80-ac1b-11ea-8084-2c6d4ad4eed6)
    
 
 - **PersonalInterestForm.ExistingContract**
    - ***Description***: associated with Form Question related "Existing contract or any pending negotiation"
    - ***Section***: Section 4(PI - Board Member, Employee)
    - ***Fields***: ExistingContractId, ExistingContractDescriptionInput, ExistingContractDescriptionOutput
    - ***Configuration File***: load/configuration/PersonalInterestForm/declaration.hdbtabledata
    - ***Input File***: load/configuration/PersonalInterestForm/ExistingContract.csv
    - ![image](https://github.deutsche-boerse.de/storage/user/3147/files/e119f980-ac92-11ea-90c7-89e4cb9c2587)

 - **PersonalInterestForm.ExistingContractYes**
    - ***Description***: associated with Form Question related "Existing contract or any pending negotiation details"
    - ***Section***: Section 4(PI - Board Member)
    - ***Fields***: ExistingContractYesId, ExistingContractYesDescriptionInput, ExistingContractYesDescriptionOutput
    - ***Configuration File***: load/configuration/PersonalInterestForm/declaration.hdbtabledata
    - ***Input File***: load/configuration/PersonalInterestForm/ExistingContractYes.csv
    - ![image](https://github.deutsche-boerse.de/storage/user/3147/files/fe4ec800-ac92-11ea-95a1-385bb22d8d0a)
 
  - **PersonalInterestForm.WorkAffected**
    - ***Description***: associated with Form Question related "Work affected by Personal Interest"
    - ***Section***: Section 4(PI - Board Member)
    - ***Fields***: WorkAffectedId, WorkAffectedDescriptionInput, WorkAffectedDescriptionOutput
    - ***Configuration File***: load/configuration/PersonalInterestForm/declaration.hdbtabledata
    - ***Input File***: load/configuration/PersonalInterestForm/WorkAffected.csv
    - ![image](https://github.deutsche-boerse.de/storage/user/3147/files/1a069e00-ac94-11ea-9637-b26afc6ebd4c)
    
 
 - **PersonalInterestForm.FICoIFI**
    - ***Description***: associated with Form Question related "Financial Interest in Third Party"
    - ***Section***: Section 2(FI - Board Member, Employee, Student)
    - ***Fields***: FICoIFIId, FICoIFIDescriptionInput, FICoIFIDescriptionOutput
    - ***Configuration File***: load/configuration/PersonalInterestForm/declaration.hdbtabledata
    - ***Input File***: load/configuration/PersonalInterestForm/FICoIFI.csv
    - ![image](https://github.deutsche-boerse.de/storage/user/3147/files/723da000-ac94-11ea-8998-d6b0022c5a57)

 - **PersonalInterestForm.InterestDBGFI**
    - ***Description***: associated with Form Question related "Financial Interest in DBG company/entity"
    - ***Section***: Section 2(FI - Board Member, Employee, Student)
    - ***Fields***: InterestDBGFIId, InterestDBGFIDescriptionInput, InterestDBGFIDescriptionOutput
    - ***Configuration File***: load/configuration/PersonalInterestForm/declaration.hdbtabledata
    - ***Input File***: load/configuration/PersonalInterestForm/InterestDBGFI.csv
    - ![image](https://github.deutsche-boerse.de/storage/user/3147/files/06a80280-ac95-11ea-9963-61fe04120791)
    
  - **PersonalInterestForm.FinanceInterestDetails**
    - ***Description***: associated with Form Question related "Kind of Financial Interest in Third Party"
    - ***Section***: Section 3(FI - Board Member, Employee, Student)
    - ***Fields***: FinanceInterestId, FinanceInterestDescInput, FinanceInterestDescOutput
    - ***Configuration File***: load/configuration/PersonalInterestForm/declaration.hdbtabledata
    - ***Input File***: load/configuration/PersonalInterestForm/FinanceInterestDetails.csv
    - ![image](https://github.deutsche-boerse.de/storage/user/3147/files/a9f91780-ac95-11ea-93f2-20b6fa30d138)

 - **PersonalInterestForm.KindParticipation**
    - ***Description***: associated with Form Question related "Amount of the ownership in the affected company/ entity"
    - ***Section***: Section 3(FI - Board Member, Employee, Student)
    - ***Fields***: KindParticipationId, KindParticipationDescInput, KindParticipationDescOutput
    - ***Configuration File***: load/configuration/PersonalInterestForm/declaration.hdbtabledata
    - ***Input File***: load/configuration/PersonalInterestForm/KindParticipation.csv
    - ![image](https://github.deutsche-boerse.de/storage/user/3147/files/402d3d80-ac96-11ea-869b-ecea9cbda8c2)
    
  - **PersonalInterestForm.InvestmentClubInfluenceFI**
    - ***Description***: associated with Form Question related "Influence in the investment club or similar association
    - ***Section***: Section 3(FI - Board Member, Employee, Student)
    - ***Fields***: InvestmentClubInfluenceFIId, InvestmentClubInfluenceFIDescInput, InvestmentClubInfluenceFIDescOutput
    - ***Configuration File***: load/configuration/PersonalInterestForm/declaration.hdbtabledata
    - ***Input File***: load/configuration/PersonalInterestForm/InvestmentClubInfluenceFI.csv
    - ![image](https://github.deutsche-boerse.de/storage/user/3147/files/7c609e00-ac96-11ea-9f3b-0dfec0788b7c)

 - **PersonalInterestForm.AssociatedPersonDetails**
    - ***Description***: associated with Form Question related "Person associated with you"
    - ***Section***: Section 2(PIPCA - Board Member, Employee, Student)
    - ***Fields***: AssociatedPersonId, AssociatedPersonDescInput, AssociatedPersonDescOutput
    - ***Configuration File***: load/configuration/PersonalInterestForm/declaration.hdbtabledata
    - ***Input File***: load/configuration/PersonalInterestForm/AssociatedPersonDetails.csv
    - ![image](https://github.deutsche-boerse.de/storage/user/3147/files/e711d980-ac96-11ea-897a-8c53610def70)
