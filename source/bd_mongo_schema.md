# Database Analysis: bd

Last Updated: 2025/3/4 上午10:10:39

## Database Statistics
- Database Size: 88.10 MB
- Collections: 12
- Total Documents: 1278983
- Total Data Size: 371.24 MB

## Collections Overview
- tasks: 5523 documents, 0.99 MB
- eminutes: 133 documents, 0.03 MB
- submissions: 0 documents, 0.00 MB
- applications: 381 documents, 0.36 MB
- notifications: 1837 documents, 0.24 MB
- bsblocks: 98397 documents, 6.40 MB
- cases: 451 documents, 1.17 MB
- oauthtokens: 3019 documents, 2.29 MB
- sysfilerefs: 601808 documents, 204.70 MB
- attachments: 370 documents, 0.13 MB
- users: 116 documents, 0.04 MB
- adrblkfilerefs: 566948 documents, 154.89 MB


## Collection: tasks
----------------------------------------
### Collection Statistics
- Document Count: 5523
- Size: 0.99 MB
- Average Document Size: 0.18 KB

### Field Analysis
#### __v
- Types: objectId, int
- Occurrences: 1000
----------------
#### _id
- Types: objectId
- Occurrences: 1000
----------------
#### application
- Types: objectId
- Occurrences: 998
----------------
#### createdAt
- Types: date
- Occurrences: 1000
----------------
#### status
- Types: string
- Occurrences: 1000
----------------
#### submissionCase
- Types: objectId
- Occurrences: 998
----------------
#### taskType
- Types: string
- Occurrences: 998
----------------
#### team
- Types: string
- Occurrences: 835
----------------
#### user
- Types: string, objectId
- Occurrences: 713
----------------
## Collection: eminutes
----------------------------------------
### Collection Statistics
- Document Count: 133
- Size: 0.03 MB
- Average Document Size: 0.24 KB

### Field Analysis
#### __v
- Types: int
- Occurrences: 133
----------------
#### _id
- Types: objectId
- Occurrences: 133
----------------
#### comment
- Types: string
- Occurrences: 64
----------------
#### content
- Types: string
- Occurrences: 133
----------------
#### createdAt
- Types: date
- Occurrences: 133
----------------
#### efolio
- Types: string
- Occurrences: 100
----------------
#### eminuteId
- Types: string
- Occurrences: 133
----------------
#### from
- Types: objectId, string
- Occurrences: 133
----------------
#### status
- Types: string
- Occurrences: 133
----------------
#### subject
- Types: string
- Occurrences: 133
----------------
#### submissionCase
- Types: objectId
- Occurrences: 133
----------------
#### sysFileRefId
- Types: string
- Occurrences: 65
----------------
#### to
- Types: objectId, string
- Occurrences: 129
----------------
## Collection: submissions
----------------------------------------
### Collection Statistics
- Document Count: 0
- Size: 0.00 MB
- Average Document Size: 0.00 KB

### Field Analysis
## Collection: applications
----------------------------------------
### Collection Statistics
- Document Count: 381
- Size: 0.36 MB
- Average Document Size: 0.96 KB

### Field Analysis
#### APP13
- Types: object, array
- Occurrences: 172
----------------
#### AddressOfPremiseCN
- Types: string
- Occurrences: 267
----------------
#### AddressOfPremiseCNFloor
- Types: string
- Occurrences: 147
----------------
#### AddressOfPremiseCNUnit
- Types: string
- Occurrences: 147
----------------
#### AddressOfPremiseEN
- Types: string
- Occurrences: 271
----------------
#### AddressOfPremiseENFloor
- Types: string
- Occurrences: 155
----------------
#### AddressOfPremiseENUnit
- Types: string
- Occurrences: 154
----------------
#### AgeOfStudent
- Types: null, string
- Occurrences: 328
----------------
#### ApplicantAddress
- Types: string
- Occurrences: 335
----------------
#### ApplicantEmail
- Types: string
- Occurrences: 289
----------------
#### ApplicantFax
- Types: string
- Occurrences: 21
----------------
#### ApplicantMobile
- Types: string
- Occurrences: 288
----------------
#### ApplicantName
- Types: string
- Occurrences: 189
----------------
#### ApplicantNameCN
- Types: string
- Occurrences: 28
----------------
#### ApplicantNameEN
- Types: null, string
- Occurrences: 148
----------------
#### ApplicantTel
- Types: null, string
- Occurrences: 307
----------------
#### ApplicationNo
- Types: null, string
- Occurrences: 381
----------------
#### ApplicationType
- Types: string
- Occurrences: 356
----------------
#### Area
- Types: string
- Occurrences: 28
----------------
#### BlockID
- Types: string
- Occurrences: 178
----------------
#### ContactPerson
- Types: string
- Occurrences: 95
----------------
#### ContactPersonCN
- Types: string
- Occurrences: 6
----------------
#### ContactPersonEN
- Types: string
- Occurrences: 6
----------------
#### ContactPersonEmail
- Types: string
- Occurrences: 6
----------------
#### ContactPersonTel
- Types: string
- Occurrences: 6
----------------
#### DescriptionOfSchool
- Types: string, null
- Occurrences: 329
----------------
#### District
- Types: string
- Occurrences: 33
----------------
#### EstimatedNoOfStudent
- Types: int, null
- Occurrences: 328
----------------
#### FileReference
- Types: string
- Occurrences: 35
----------------
#### NameOfSchoolCN
- Types: string
- Occurrences: 323
----------------
#### NameOfSchoolEN
- Types: string
- Occurrences: 350
----------------
#### Region
- Types: string
- Occurrences: 29
----------------
#### RelatedPremise
- Types: string
- Occurrences: 62
----------------
#### RelatedPremises
- Types: array
- Occurrences: 381
----------------
#### SelfCertification
- Types: object, null
- Occurrences: 65
----------------
#### StructuralCalculation
- Types: object
- Occurrences: 18
----------------
#### SubmissionType
- Types: string
- Occurrences: 187
----------------
#### __v
- Types: int
- Occurrences: 381
----------------
#### _id
- Types: objectId
- Occurrences: 381
----------------
#### address
- Types: object
- Occurrences: 69
----------------
#### assignedBS
- Types: objectId, string, null
- Occurrences: 364
----------------
#### assignedGR
- Types: objectId, null
- Occurrences: 64
----------------
#### assignedSBS
- Types: string, null
- Occurrences: 53
----------------
#### createdAt
- Types: date
- Occurrences: 381
----------------
#### updatedAt
- Types: date
- Occurrences: 194
----------------
## Collection: notifications
----------------------------------------
### Collection Statistics
- Document Count: 1837
- Size: 0.24 MB
- Average Document Size: 0.13 KB

### Field Analysis
#### __v
- Types: int
- Occurrences: 1000
----------------
#### _id
- Types: objectId
- Occurrences: 1000
----------------
#### createdAt
- Types: date
- Occurrences: 1000
----------------
#### eminute
- Types: objectId
- Occurrences: 58
----------------
#### notificationType
- Types: string
- Occurrences: 1000
----------------
#### requireSendEmail
- Types: bool
- Occurrences: 1000
----------------
#### task
- Types: objectId
- Occurrences: 942
----------------
#### user
- Types: string
- Occurrences: 991
----------------
## Collection: bsblocks
----------------------------------------
### Collection Statistics
- Document Count: 98397
- Size: 6.40 MB
- Average Document Size: 0.07 KB

### Field Analysis
#### __v
- Types: int
- Occurrences: 1000
----------------
#### _id
- Types: objectId
- Occurrences: 1000
----------------
#### bdgis
- Types: string
- Occurrences: 1000
----------------
#### blockId
- Types: string
- Occurrences: 1000
----------------
## Collection: cases
----------------------------------------
### Collection Statistics
- Document Count: 451
- Size: 1.17 MB
- Average Document Size: 2.65 KB

### Field Analysis
#### ActualReplyDate
- Types: null, date
- Occurrences: 39
----------------
#### Area
- Types: string
- Occurrences: 26
----------------
#### AuditResult
- Types: string
- Occurrences: 11
----------------
#### CaseOfficer
- Types: string
- Occurrences: 108
----------------
#### Category
- Types: string
- Occurrences: 384
----------------
#### District
- Types: string
- Occurrences: 37
----------------
#### FileReference
- Types: string
- Occurrences: 60
----------------
#### LAFileReference
- Types: object
- Occurrences: 17
----------------
#### Nature
- Types: null, string
- Occurrences: 382
----------------
#### ObjectiontoLR
- Types: string
- Occurrences: 12
----------------
#### ReceivedDate
- Types: date, null
- Occurrences: 375
----------------
#### Referrer
- Types: object
- Occurrences: 43
----------------
#### Region
- Types: string
- Occurrences: 32
----------------
#### Remarks
- Types: string
- Occurrences: 7
----------------
#### Reminders
- Types: array
- Occurrences: 55
----------------
#### SubmissionType
- Types: string
- Occurrences: 8
----------------
#### SubstantialReplyDate
- Types: null, date
- Occurrences: 42
----------------
#### TargetReplyDate
- Types: date, null
- Occurrences: 111
----------------
#### ThreeTierReqt
- Types: string
- Occurrences: 12
----------------
#### ViaSCS
- Types: bool
- Occurrences: 17
----------------
#### __v
- Types: int
- Occurrences: 451
----------------
#### _id
- Types: objectId
- Occurrences: 451
----------------
#### application
- Types: objectId
- Occurrences: 450
----------------
#### assignedBS
- Types: objectId
- Occurrences: 274
----------------
#### assignedGR
- Types: objectId
- Occurrences: 137
----------------
#### building_information
- Types: object
- Occurrences: 14
----------------
#### caseDescription
- Types: object
- Occurrences: 9
----------------
#### caseOfficerReceive
- Types: string
- Occurrences: 172
----------------
#### caseOfficerReply
- Types: string
- Occurrences: 72
----------------
#### createdAt
- Types: date
- Occurrences: 451
----------------
#### deck_study
- Types: object
- Occurrences: 451
----------------
#### documentChecklist
- Types: object
- Occurrences: 2
----------------
#### dv
- Types: object
- Occurrences: 197
----------------
#### frc
- Types: object
- Occurrences: 451
----------------
#### misc
- Types: object
- Occurrences: 451
----------------
#### moe
- Types: object
- Occurrences: 451
----------------
#### seniorCaseOfficerReceive
- Types: string
- Occurrences: 54
----------------
#### seniorCaseOfficerReply
- Types: string
- Occurrences: 41
----------------
#### site_inspection
- Types: object
- Occurrences: 7
----------------
#### structural_ccc_bs
- Types: object
- Occurrences: 451
----------------
#### structural_schnlh
- Types: object
- Occurrences: 152
----------------
#### structural_schnlhkinds
- Types: object
- Occurrences: 301
----------------
#### team
- Types: string
- Occurrences: 374
----------------
#### ubw
- Types: object
- Occurrences: 451
----------------
#### updatedAt
- Types: date
- Occurrences: 16
----------------
## Collection: oauthtokens
----------------------------------------
### Collection Statistics
- Document Count: 3019
- Size: 2.29 MB
- Average Document Size: 0.78 KB

### Field Analysis
#### __v
- Types: int
- Occurrences: 1000
----------------
#### _id
- Types: objectId
- Occurrences: 1000
----------------
#### accessToken
- Types: string
- Occurrences: 1000
----------------
#### accessTokenExpiresAt
- Types: date
- Occurrences: 1000
----------------
#### client
- Types: object
- Occurrences: 1000
----------------
#### refreshToken
- Types: string
- Occurrences: 1000
----------------
#### refreshTokenExpiresAt
- Types: date
- Occurrences: 1000
----------------
#### user
- Types: objectId
- Occurrences: 1000
----------------
## Collection: sysfilerefs
----------------------------------------
### Collection Statistics
- Document Count: 601808
- Size: 204.70 MB
- Average Document Size: 0.35 KB

### Field Analysis
#### __v
- Types: int
- Occurrences: 1000
----------------
#### _id
- Types: objectId
- Occurrences: 1000
----------------
#### createdDt
- Types: date
- Occurrences: 1000
----------------
#### createdName
- Types: null, string
- Occurrences: 1000
----------------
#### createdPost
- Types: null, string
- Occurrences: 1000
----------------
#### createdSection
- Types: null, string
- Occurrences: 1000
----------------
#### display
- Types: string
- Occurrences: 1000
----------------
#### dvExceed
- Types: null, string
- Occurrences: 1000
----------------
#### dvStatusDt
- Types: null, date
- Occurrences: 1000
----------------
#### frefPref
- Types: string, null
- Occurrences: 1000
----------------
#### frefSeq
- Types: null, string
- Occurrences: 1000
----------------
#### frefSuf
- Types: null, string
- Occurrences: 1000
----------------
#### frefYr
- Types: null, string
- Occurrences: 1000
----------------
#### lastModifiedDt
- Types: date
- Occurrences: 1000
----------------
#### lastModifiedName
- Types: null, string
- Occurrences: 1000
----------------
#### lastModifiedPost
- Types: null, string
- Occurrences: 1000
----------------
#### lastModifiedSection
- Types: null
- Occurrences: 1000
----------------
#### sysFileRefId
- Types: string
- Occurrences: 1000
----------------
## Collection: attachments
----------------------------------------
### Collection Statistics
- Document Count: 370
- Size: 0.13 MB
- Average Document Size: 0.37 KB

### Field Analysis
#### __v
- Types: int
- Occurrences: 370
----------------
#### _id
- Types: objectId
- Occurrences: 370
----------------
#### application
- Types: objectId
- Occurrences: 364
----------------
#### createdAt
- Types: date
- Occurrences: 370
----------------
#### efolio
- Types: null, string
- Occurrences: 351
----------------
#### file
- Types: object, string
- Occurrences: 247
----------------
#### filePartNo
- Types: string
- Occurrences: 216
----------------
#### receivedDate
- Types: date
- Occurrences: 352
----------------
#### remarks
- Types: string
- Occurrences: 216
----------------
#### subType
- Types: string
- Occurrences: 203
----------------
#### submissionCase
- Types: objectId
- Occurrences: 350
----------------
#### sysFileRefId
- Types: string
- Occurrences: 67
----------------
#### type
- Types: string
- Occurrences: 348
----------------
#### updatedAt
- Types: date
- Occurrences: 3
----------------
## Collection: users
----------------------------------------
### Collection Statistics
- Document Count: 116
- Size: 0.04 MB
- Average Document Size: 0.39 KB

### Field Analysis
#### __v
- Types: int
- Occurrences: 116
----------------
#### _id
- Types: objectId
- Occurrences: 116
----------------
#### bdgis
- Types: string
- Occurrences: 29
----------------
#### begis
- Types: string
- Occurrences: 1
----------------
#### delegateTo
- Types: string
- Occurrences: 8
----------------
#### department
- Types: string
- Occurrences: 116
----------------
#### email
- Types: string
- Occurrences: 109
----------------
#### group
- Types: string
- Occurrences: 17
----------------
#### lastLoginAt
- Types: date
- Occurrences: 41
----------------
#### letterLongPosition
- Types: string
- Occurrences: 11
----------------
#### letterLongPositionCn
- Types: string
- Occurrences: 12
----------------
#### letterName
- Types: string
- Occurrences: 76
----------------
#### letterNameCn
- Types: string
- Occurrences: 75
----------------
#### letterPosition
- Types: string
- Occurrences: 79
----------------
#### letterPositionCn
- Types: string
- Occurrences: 1
----------------
#### lock
- Types: bool
- Occurrences: 116
----------------
#### luPostName
- Types: string
- Occurrences: 78
----------------
#### name
- Types: string
- Occurrences: 80
----------------
#### notificationEmail
- Types: string
- Occurrences: 23
----------------
#### osdpEmail
- Types: string
- Occurrences: 62
----------------
#### osdpLoginId
- Types: string
- Occurrences: 102
----------------
#### password
- Types: string
- Occurrences: 108
----------------
#### phoneNumber
- Types: string
- Occurrences: 65
----------------
#### position
- Types: string
- Occurrences: 85
----------------
#### role
- Types: string
- Occurrences: 112
----------------
#### team
- Types: string
- Occurrences: 52
----------------
#### userType
- Types: string
- Occurrences: 116
----------------
## Collection: adrblkfilerefs
----------------------------------------
### Collection Statistics
- Document Count: 566948
- Size: 154.89 MB
- Average Document Size: 0.28 KB

### Field Analysis
#### __v
- Types: int
- Occurrences: 1000
----------------
#### _id
- Types: objectId
- Occurrences: 1000
----------------
#### adrBlkFileRefId
- Types: string
- Occurrences: 1000
----------------
#### adrBlkId
- Types: string
- Occurrences: 1000
----------------
#### createdDt
- Types: date
- Occurrences: 1000
----------------
#### createdName
- Types: null, string
- Occurrences: 1000
----------------
#### createdPost
- Types: string
- Occurrences: 1000
----------------
#### createdSection
- Types: null, string
- Occurrences: 1000
----------------
#### lastModifiedDt
- Types: date
- Occurrences: 1000
----------------
#### lastModifiedName
- Types: null, string
- Occurrences: 1000
----------------
#### lastModifiedPost
- Types: string
- Occurrences: 1000
----------------
#### lastModifiedSection
- Types: string, null
- Occurrences: 1000
----------------
#### sysFileRefId
- Types: string
- Occurrences: 1000
----------------
