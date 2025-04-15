Function in SEN Spec

 

+---+---+---+----+----------------------------------------------------+----+
| M | P | I | S  | Feature Detail                                     | In |
| o | a | n | um |                                                    | S  |
| d | g | d | ma |                                                    | co |
| u | e | e | ry |                                                    | pe |
| l |   | x |    |                                                    | /  |
| e |   |   |    |                                                    |    |
|   |   |   |    |                                                    | O  |
|   |   |   |    |                                                    | ut |
|   |   |   |    |                                                    | S  |
|   |   |   |    |                                                    | co |
|   |   |   |    |                                                    | pe |
+===+===+===+====+====================================================+====+
| I | 5 | 1 | S  | 1.  Invigilator's EP number/Application number     | >  |
| n |   | 3 | EN |     shall be used to recognize the specific exam   |  O |
| v |   | . | I  |     session of the exam centre that he/she is      | ut |
| i |   | 1 | nv |     responsible for.                               | >  |
| A |   | . | ig |                                                    |  S |
| p |   | 1 | il | 2.  Users shall be able to login the App with or   | co |
| p |   |   | at |     without the EP number / Application number.    | pe |
|   |   |   | or |                                                    |    |
|   |   |   | L  | 3.  For ad hoc invigilators without EP /           |    |
|   |   |   | og |     Application number, CS shall enter their       |    |
|   |   |   | in |     english name / HKID no. and select the school  |    |
|   |   |   |    |     name and code they come from in the drop-down  |    |
|   |   |   |    |     list to create a unique QR code for the        |    |
|   |   |   |    |     invigilator to login.                          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  Invigilator shall scan the QR code provided by |    |
|   |   |   |    |     the SEN CS to login 'i-Invigilation (HKDSE)'   |    |
|   |   |   |    |     (Invigilator App)                              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 5.  Under certain circumstances (e.g. a single     |    |
|   |   |   |    |     candidate classroom centre which may not have  |    |
|   |   |   |    |     the formal invigilator), the CS shall be able  |    |
|   |   |   |    |     to scan and login themselves as the classroom  |    |
|   |   |   |    |     invigilator to perform invigilation besides    |    |
|   |   |   |    |     performing the duties of CS at the same time.  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 6.  After login, the App shall show:               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Invigilator information:                   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Name                                   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   EP number/Application number           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Assigned duties:                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Exam date                              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Exam centre code (for Classroom        |    |
|   |   |   |    |             Invigilators, it shall be displayed    |    |
|   |   |   |    |             after assignment created by the        |    |
|   |   |   |    |             Classroom CS)                          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Exam centre location                   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   For Hall Invigilators, a dashboard of      |    |
|   |   |   |    |         basic functions shall be displayed.        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Take attendance / Verify identity      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Check-in/Out (Toilet Request)          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Script Counting                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   For Classroom Invigilators, an empty       |    |
|   |   |   |    |         dashboard shall be shown.                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   The dashboard shall be updated after the   |    |
|   |   |   |    |         invigilator assignment created by the Hall |    |
|   |   |   |    |         or Classroom CS.                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | >                                                  |    |
+---+---+---+----+----------------------------------------------------+----+
| I | 6 | 1 | S  | 1.  Users shall be able to login the App without   | >  |
| n |   | 3 | EN |     the presence of CS to provide the login code   |  O |
| v |   | . | In |     if they are assigned to take over the duties   | ut |
| i |   | 1 | vi |     of existing invigilators (e.g. A PM            | >  |
| A |   | . | gi |     invigilator takes over the duties of an AM     |  S |
| p |   | 2 | la |     invigilator during 12:00pm - 12:30pm for an    | co |
| p |   |   | to |     exam session to end after 2:00pm, Early leave  | pe |
|   |   |   | rs |     of the existing invigilator) by one of the     |    |
|   |   |   | s  |     following methods:                             |    |
|   |   |   | hi |                                                    |    |
|   |   |   | ft |     -   For the invigilators who bring their own   |    |
|   |   |   | du |         devices for invigilation (i.e. BYOD), the  |    |
|   |   |   | ty |         App shall allow the existing invigilator   |    |
|   |   |   | w  |         to trigger the inheritance of assignment   |    |
|   |   |   | it |         by tapping the 'Shift duty' button at the  |    |
|   |   |   | ho |         side menu. Then, a QR code shall be shown  |    |
|   |   |   | ut |         on the 'Shift Duty' page. The new          |    |
|   |   |   | t  |         invigilator shall tap the 'Login' button   |    |
|   |   |   | he |         on his / her own device, scan the QR code, |    |
|   |   |   | pr |         and enter the login credential to login    |    |
|   |   |   | es |         and check-in in order to take over the     |    |
|   |   |   | en |         assignment.                                |    |
|   |   |   | ce |                                                    |    |
|   |   |   | of |     -   For both the existing and new invigilators |    |
|   |   |   | CS |         who share the same device provided by the  |    |
|   |   |   |    |         HKEAA, the App shall allow the existing    |    |
|   |   |   |    |         invigilator to trigger the inheritance of  |    |
|   |   |   |    |         assignment by tapping the 'Shift duty'     |    |
|   |   |   |    |         button at the side menu and then tapping   |    |
|   |   |   |    |         the 'Shift duty' button on the 'Shift      |    |
|   |   |   |    |         Duty' page. The new invigilator shall      |    |
|   |   |   |    |         enter the login credential to login and    |    |
|   |   |   |    |         check-in in order to take over the         |    |
|   |   |   |    |         assignment.                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 2.  For the invigilators to login, EP /            |    |
|   |   |   |    |     Application Number shall be entered.           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 3.  For the ad hoc invigilators without EP /       |    |
|   |   |   |    |     Application Number to login, English Name / ID |    |
|   |   |   |    |     Number shall be entered. School Name and Code  |    |
|   |   |   |    |     of the schools where they come from shall be   |    |
|   |   |   |    |     mandatorily selected from the drop-down list:  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   The drop-down list with all school names   |    |
|   |   |   |    |         and codes shall be displayed at the field  |    |
|   |   |   |    |         for users to select if no character(s) is  |    |
|   |   |   |    |         inputted.                                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   By inputting character(s), corresponding   |    |
|   |   |   |    |         school name(s) and code(s) shall be        |    |
|   |   |   |    |         displayed in the drop-down list at the     |    |
|   |   |   |    |         field for users to select.                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  Once the new invigilator has logged in the     |    |
|   |   |   |    |     module, the system shall force to logout the   |    |
|   |   |   |    |     existing invigilator who has logged in the     |    |
|   |   |   |    |     same exam session and a message \"Do you want  |    |
|   |   |   |    |     to replace the existing invigilator?" shall be |    |
|   |   |   |    |     displayed to confirm the forced logout.        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 5.  Once the new invigilator has logged in the     |    |
|   |   |   |    |     module and the existing invigilator has been   |    |
|   |   |   |    |     forced to log out, the states of assignment    |    |
|   |   |   |    |     and tasks of the existing invigilator shall be |    |
|   |   |   |    |     inherited by the new invigilator.              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 6.  The system shall record the actions which      |    |
|   |   |   |    |     shall be able to be found at the 'Event Log'   |    |
|   |   |   |    |     of Exam Support Backend (SEAD) module.         |    |
+---+---+---+----+----------------------------------------------------+----+
| I | 8 | 1 | As | 1.  Users shall be assigned to manage the zone(s)  | >  |
| n |   | 3 | si |     consisting of the candidates that are arranged |  O |
| v |   | . | gn |     according to their exam time.                  | ut |
| i |   | 1 | me |                                                    | >  |
| A |   | . | nt |     -   Single invigilator shall be able to be     |  S |
| p |   | 3 | R  |         assigned to manage multiple zones.         | co |
| p |   |   | et |                                                    | pe |
|   |   |   | ri |     -   Multiple invigilators shall be allowed to  |    |
|   |   |   | ev |         be assigned to a single zone (i.e.         |    |
|   |   |   | al |         applicable to Classroom Invigilator).      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Users shall view & work with the           |    |
|   |   |   |    |         candidates in those zone(s) assigned to    |    |
|   |   |   |    |         them.                                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 2.  Users shall be able to view the updated        |    |
|   |   |   |    |     dashboard with:                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Take attendance/verify identity with alert |    |
|   |   |   |    |         if missing attendance records found        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Present count including:               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |             -   Verified self check-in with the    |    |
|   |   |   |    |                 format of x (y) where x is number  |    |
|   |   |   |    |                 of self checked-in candidates      |    |
|   |   |   |    |                 verified by the invigilator and y  |    |
|   |   |   |    |                 is the number of candidates who    |    |
|   |   |   |    |                 have self checked-in.              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |             -   Verified and attendance taken by   |    |
|   |   |   |    |                 invigilator                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |             -   Attendance involved SR1            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Special Case (i.e. wrong centre        |    |
|   |   |   |    |             candidate, applicable to the Classroom |    |
|   |   |   |    |             Invigilator)                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Absent count                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Total count of candidates assigned to  |    |
|   |   |   |    |             the invigilator                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Check-in/out (Toilet Request) with alert   |    |
|   |   |   |    |         if candidate not yet back after check-out  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Script Counting with number of scripts     |    |
|   |   |   |    |         collected, with alert if there is missing  |    |
|   |   |   |    |         script                                     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Report with alerts if discrepancy is       |    |
|   |   |   |    |         found, sessional report is not completed   |    |
|   |   |   |    |         and no seating plan is uploaded            |    |
|   |   |   |    |         (applicable to Classroom Invigilator)      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Summary Report                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Discrepancy Report with alert if there |    |
|   |   |   |    |             is a discrepancy                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Sessional Report with alert if not     |    |
|   |   |   |    |             completed                              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | > [Seating Pla]{.mark}n with alert if not provided |    |
+---+---+---+----+----------------------------------------------------+----+
| I | 1 | 1 | At | 1.  A list of zones with the corresponding zone    | >  |
| n | 1 | 3 | te |     name(s) shall be displayed under 'Assign Zone' | On |
| v |   | . | nd |     after tapping the 'Take attendance / Verify    | ly |
| i |   | 1 | an |     identity' section. Candidates of different     | >  |
| A |   | . | ce |     subjects having the same timetable shall be    |  p |
| p |   | 4 | Ta |     grouped under the same zone.                   | oi |
| p |   |   | ki |                                                    | nt |
|   |   |   | ng | 2.  For each assigned zone, the exam time and the  | >  |
|   |   |   | /  |     supervised break(s) shall be listed.           | 13 |
|   |   |   | Ve |                                                    | >  |
|   |   |   | ri | 3.  By tapping into each zone, a list shall be     | is |
|   |   |   | fy |     able to separate the candidates with different | >  |
|   |   |   | Id |     attendance status: Pending, Present, Absent    | in |
|   |   |   | en |     (and Special Cases for the Classroom           | -s |
|   |   |   | ti |     Invigilator). Number of candidates involved in | co |
|   |   |   | ty |     different status shall also be displayed.      | pe |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  The candidate list shall be displayed for the  |    |
|   |   |   |    |     selected attendance status with the following  |    |
|   |   |   |    |     fields:                                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   (Seat number of allocated candidate or '-  |    |
|   |   |   |    |         -' for wrong centre candidate) Candidate   |    |
|   |   |   |    |         number                                     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Candidate name                             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Subject/Paper name                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Case number (the length ranges from 11 to  |    |
|   |   |   |    |         12 characters depends on the trailing      |    |
|   |   |   |    |         numbers followed by the disabilities code, |    |
|   |   |   |    |         e.g. DSE2021A001 and DSE2021A0001).        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 5.  There is a right arrow at the right side of    |    |
|   |   |   |    |     the case number to indicate that the candidate |    |
|   |   |   |    |     carries remarks.                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 6.  Users shall be able to view the SEN Remarks of |    |
|   |   |   |    |     the candidate by clicking the right arrow      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 7.  There shall be no need to set the validation   |    |
|   |   |   |    |     of preventing invigilators from updating       |    |
|   |   |   |    |     attendance records after the exam ends.        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 8.  Users shall confirm the candidates' identity   |    |
|   |   |   |    |     verification if the candidates have self       |    |
|   |   |   |    |     checked-in.                                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 9.  Users shall scan the candidates' personalized  |    |
|   |   |   |    |     barcode and confirm their identity             |    |
|   |   |   |    |     verification if the candidates have not self   |    |
|   |   |   |    |     checked-in.                                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 10. Users shall be able to input remarks when      |    |
|   |   |   |    |     flagging a candidate.                          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 11. SR1 shall be able to be chosen when at least   |    |
|   |   |   |    |     one of the following conditions exist (i.e.    |    |
|   |   |   |    |     shall be updated after the SR Forms Module is  |    |
|   |   |   |    |     applied):                                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Produce Admission Form - Yes / No          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Produce Identity Card (or valid            |    |
|   |   |   |    |         identification document with a             |    |
|   |   |   |    |         photograph) - Yes / No                     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Photograph resembles candidate - Yes / No  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 12. Users shall be able to mark the candidate's    |    |
|   |   |   |    |     attendance record as Absent by swiping a       |    |
|   |   |   |    |     candidate record to the left and clicking the  |    |
|   |   |   |    |     red 'abs' button.                              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 13. Seating rearrangement (without changing the    |    |
|   |   |   |    |     original seat no.) is allowed in the SEN exam  |    |
|   |   |   |    |     centre.                                        |    |
+---+---+---+----+----------------------------------------------------+----+
| I | 1 | 1 | Ma | 1.  By tapping into each zone, select Special Case | >  |
| n | 5 | 3 | in |     for filtering, a list of special case          |  O |
| v |   | . | ta |     candidates shall be displayed with following   | ut |
| i |   | 1 | in |     information.                                   | >  |
| A |   | . | At |                                                    |  S |
| p |   | 5 | te |     -   (Seat number) Candidate number             | co |
| p |   |   | nd |                                                    | pe |
|   |   |   | an |     -   Candidate name                             |    |
|   |   |   | ce |                                                    |    |
|   |   |   | a  | 2.  Users shall be able to swipe a candidate       |    |
|   |   |   | nd |     record to the left and click the green         |    |
|   |   |   | Sc |     'Details' button. Then, they shall be able to  |    |
|   |   |   | ri |     edit the spare barcode number and script       |    |
|   |   |   | pt |     collected.                                     |    |
|   |   |   | R  |                                                    |    |
|   |   |   | ec |                                                    |    |
|   |   |   | or |                                                    |    |
|   |   |   | ds |                                                    |    |
|   |   |   | of |                                                    |    |
|   |   |   | S  |                                                    |    |
|   |   |   | pe |                                                    |    |
|   |   |   | ci |                                                    |    |
|   |   |   | al |                                                    |    |
|   |   |   | Ca |                                                    |    |
|   |   |   | se |                                                    |    |
|   |   |   | (  |                                                    |    |
|   |   |   | ap |                                                    |    |
|   |   |   | pl |                                                    |    |
|   |   |   | ic |                                                    |    |
|   |   |   | ab |                                                    |    |
|   |   |   | le |                                                    |    |
|   |   |   | to |                                                    |    |
|   |   |   | C  |                                                    |    |
|   |   |   | la |                                                    |    |
|   |   |   | ss |                                                    |    |
|   |   |   | ro |                                                    |    |
|   |   |   | om |                                                    |    |
|   |   |   | In |                                                    |    |
|   |   |   | vi |                                                    |    |
|   |   |   | gi |                                                    |    |
|   |   |   | la |                                                    |    |
|   |   |   | to |                                                    |    |
|   |   |   | r) |                                                    |    |
+---+---+---+----+----------------------------------------------------+----+
| I | 1 | 1 | C  | 1.  Users shall be able to record the toilet       | >  |
| n | 7 | 3 | an |     request of candidates right after they have    |  O |
| v |   | . | di |     checked-in the exam sessions in order to       | ut |
| i |   | 1 | da |     handle the toilet requests before exam start.  | >  |
| A |   | . | te |                                                    |  S |
| p |   | 6 | Ch | 2.  An alert icon shall be shown if the candidate  | co |
| p |   |   | ec |     is not yet back after check-out a specified    | pe |
|   |   |   | k- |     period of time (e.g. 15 minutes, which shall   |    |
|   |   |   | in |     be maintained as the parameter by HKEAA in the |    |
|   |   |   | /o |     Exam Support Backend (SEAD) module).           |    |
|   |   |   | ut |                                                    |    |
|   |   |   | (  | 3.  By tapping the 'Check-in/out (Toilet Request)' |    |
|   |   |   | To |     section under the Dashboard, the invigilator   |    |
|   |   |   | il |     shall scan the candidate's personalized        |    |
|   |   |   | et |     barcode or admission form to record the        |    |
|   |   |   | Re |     request. Then, the personal information (i.e.  |    |
|   |   |   | qu |     document number, candidate number and seat     |    |
|   |   |   | es |     number) of the candidate and the status of     |    |
|   |   |   | t) |     toilet request (i.e. check-in/out and current  |    |
|   |   |   |    |     timestamp by default) shall be shown for       |    |
|   |   |   |    |     user's confirmation. The notification signal   |    |
|   |   |   |    |     for those candidates who take over specific    |    |
|   |   |   |    |     time should be sent to the relevant            |    |
|   |   |   |    |     Invigilator or CS.                             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  The default check-in/out timestamp shall be    |    |
|   |   |   |    |     able to be edited by clicking the pencil icon. |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 5.  By tapping the 'Toilet Request Record(s)'      |    |
|   |   |   |    |     button of the scanner page, the users shall be |    |
|   |   |   |    |     able to view the list of candidates involving  |    |
|   |   |   |    |     the toilet requests. The following information |    |
|   |   |   |    |     shall be shown in each record:                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Candidate Number                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Seat Number                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Candidate Name                             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Check-in and/or check-out                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   The timestamp of check-in and /or          |    |
|   |   |   |    |         check-out                                  |    |
+---+---+---+----+----------------------------------------------------+----+
| I | 1 | 1 | Sc | 1.  Users shall be able to scan the personalised   | >  |
| n | 9 | 3 | ri |     barcodes / spare barcodes on the scripts to    |  O |
| v |   | . | pt |     count the number of scripts collected.         | ut |
| i |   | 1 | Co |                                                    | >  |
| A |   | . | un | 2.  Users shall be able to view the number of      |  S |
| p |   | 7 | ti |     scripts collected by their own accounts in the | co |
| p |   |   | ng |     Dashboard.                                     | pe |
|   |   |   |    |                                                    |    |
|   |   |   |    | 3.  Users shall be allowed to collect the number   |    |
|   |   |   |    |     of scripts more or less than the predefined    |    |
|   |   |   |    |     number of scripts to be collected for each     |    |
|   |   |   |    |     candidate, 'Zero' script is not allowed.       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  [Users shall be allowed to collect scripts at  |    |
|   |   |   |    |     different times even after the end of the      |    |
|   |   |   |    |     exam.]{.mark}                                  |    |
+---+---+---+----+----------------------------------------------------+----+
| I | 2 | 1 | I  | 1.  Dashboard shall have the Report section which  | >  |
| n | 0 | 3 | nv |     includes the following functions. It shall     |  O |
| v |   | . | ig |     display alerts if discrepancy found, not       | ut |
| i |   | 1 | il |     completed sessional report and seating plan    | >  |
| A |   | . | at |     uploaded.                                      |  S |
| p |   | 8 | or |                                                    | co |
| p |   |   | Re |     -   Summary Report                             | pe |
|   |   |   | po |                                                    |    |
|   |   |   | rt |     -   Discrepancy Report                         |    |
|   |   |   | (  |                                                    |    |
|   |   |   | ap |     -   Sessional Report                           |    |
|   |   |   | pl |                                                    |    |
|   |   |   | ic |     -   Seating Plan                               |    |
|   |   |   | ab |                                                    |    |
|   |   |   | le | 2.  Summary Report                                 |    |
|   |   |   | to |                                                    |    |
|   |   |   | C  |     -   Users shall be able to view the following  |    |
|   |   |   | la |         information.                               |    |
|   |   |   | ss |                                                    |    |
|   |   |   | ro | > For Allocated Candidate                          |    |
|   |   |   | om |                                                    |    |
|   |   |   | In | -   Number of candidates in exam centre            |    |
|   |   |   | vi |                                                    |    |
|   |   |   | gi | -   Number of candidates who are present           |    |
|   |   |   | la |                                                    |    |
|   |   |   | to | -   Number of candidates who are absent            |    |
|   |   |   | r) |                                                    |    |
|   |   |   |    | -   Missing attendance record(s)                   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   Number of answer scripts collected             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | <!-- -->                                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   For Special Case                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Number of candidates of special case       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Number of answer scripts collected from    |    |
|   |   |   |    |         special case                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 3.  Discrepancy Report                             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Users shall be able to view the full list  |    |
|   |   |   |    |         of candidates having discrepancy records   |    |
|   |   |   |    |         with the types of discrepancies.           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Users shall be able to filter a specific   |    |
|   |   |   |    |         list of candidates involved in the         |    |
|   |   |   |    |         corresponding nature. Number of candidates |    |
|   |   |   |    |         involved in different nature shall also be |    |
|   |   |   |    |         displayed.                                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Missing attendance record(s)           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Missing attendance but with script     |    |
|   |   |   |    |             collected                              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Missing script record(s)               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Absent but with script(s) collected    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Special case without script collected  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Users shall be able to edit the attendance |    |
|   |   |   |    |         status, spare barcode assigned (if         |    |
|   |   |   |    |         applicable) and the number of scripts      |    |
|   |   |   |    |         collected by clicking on the candidate     |    |
|   |   |   |    |         records for the both allocated and special |    |
|   |   |   |    |         case candidates.                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   For those candidates involved in script    |    |
|   |   |   |    |         discrepancy, users shall be required to    |    |
|   |   |   |    |         input reason by selecting one of the       |    |
|   |   |   |    |         following options through the radio        |    |
|   |   |   |    |         buttons and then input the corresponding   |    |
|   |   |   |    |         information:                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Option 1: Candidate has been approved  |    |
|   |   |   |    |             to use other answering methods.        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Option 2: Others: (Please input the    |    |
|   |   |   |    |             special situation in remarks), a text  |    |
|   |   |   |    |             box shall be provided for the user to  |    |
|   |   |   |    |             input.                                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | <!-- -->                                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 0.  Sessional Report                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Users shall be able to edit, save,         |    |
|   |   |   |    |         preview, confirm, submit and re-submit the |    |
|   |   |   |    |         Sessional Report to the CS before the CS   |    |
|   |   |   |    |         first confirms the exam data to VCC. The   |    |
|   |   |   |    |         fields shall include:                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Actual Starting Time and Finishing     |    |
|   |   |   |    |             Time under each zone name which are    |    |
|   |   |   |    |             retrieved from the system              |    |
|   |   |   |    |             automatically, users shall be able to  |    |
|   |   |   |    |             adjust in necessary                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Packages of question paper received    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Exam Irregularities for candidates     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Exam Irregularities for invigilators   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Different subject papers of the           |    |
|   |   |   |    |         candidates shall be listed under each zone |    |
|   |   |   |    |         in the Sessional Report.]{.mark}           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   \'Not yet recorded' shall be displayed if  |    |
|   |   |   |    |         there is no record in Packages of question |    |
|   |   |   |    |         paper received, Exam Irregularities        |    |
|   |   |   |    |         (Candidates) and Exam Irregularities       |    |
|   |   |   |    |         (Invigilators).                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   System shall display the Discrepancy       |    |
|   |   |   |    |         Report with types of discrepancies and     |    |
|   |   |   |    |         candidate information if there is any      |    |
|   |   |   |    |         discrepancy when users clicked the 'Submit |    |
|   |   |   |    |         to Classroom CS' button in the preview     |    |
|   |   |   |    |         page of the Sessional Report.              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Users shall be able to correct the         |    |
|   |   |   |    |         attendance status, spare barcode used and  |    |
|   |   |   |    |         the number of scripts collected by         |    |
|   |   |   |    |         clicking on the records shown in the       |    |
|   |   |   |    |         discrepancy report.                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   For those reasons of script discrepancy,   |    |
|   |   |   |    |         it shall be preloaded to the remarks.      |    |
|   |   |   |    |         Besides, users shall be able to input      |    |
|   |   |   |    |         additional remarks in free text format if  |    |
|   |   |   |    |         there is a discrepancy when submitting the |    |
|   |   |   |    |         Sessional Report to the CS.                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Users shall be able to edit and submit the |    |
|   |   |   |    |         Sessional Report iteratively before the CS |    |
|   |   |   |    |         first confirms the exam data to VCC.       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   The App shall prompt an alert to remind    |    |
|   |   |   |    |         users to submit Sessional Report again if  |    |
|   |   |   |    |         the attendance / script data was changed   |    |
|   |   |   |    |         after previous submission. Related alerts  |    |
|   |   |   |    |         shall also be prompted at the CS Module.   |    |
+---+---+---+----+----------------------------------------------------+----+
| I | 2 | 1 | S  | 1.  [Users shall be able to take the photo from    | >  |
| n | 6 | 3 | ea |     hardcopy of the candidate seating plan form    |  O |
| v |   | . | ti |     and]{.mark} upload the image through the App   | ut |
| i |   | 1 | ng |     [at any time.]{.mark}                          | >  |
| A |   | . | Pl |                                                    |  S |
| p |   | 9 | an | 2.  [Users shall be able to]{.mark} preview the    | co |
| p |   |   | (  |     candidate seating [at any time after the       | pe |
|   |   |   | ap |     seating plan was uploaded.]{.mark}             |    |
|   |   |   | pl |                                                    |    |
|   |   |   | ic | 3.  [Users shall be able to use the function by    |    |
|   |   |   | ab |     tapping the 'Seating Plan' section under the   |    |
|   |   |   | le |     'Reports'. The system shall display an alert   |    |
|   |   |   | to |     if no seating plan is uploaded.]{.mark}        |    |
|   |   |   | C  |                                                    |    |
|   |   |   | la |                                                    |    |
|   |   |   | ss |                                                    |    |
|   |   |   | ro |                                                    |    |
|   |   |   | om |                                                    |    |
|   |   |   | In |                                                    |    |
|   |   |   | vi |                                                    |    |
|   |   |   | gi |                                                    |    |
|   |   |   | la |                                                    |    |
|   |   |   | to |                                                    |    |
|   |   |   | r) |                                                    |    |
+---+---+---+----+----------------------------------------------------+----+
| I | 2 | 1 | T  | 1.  Under each zone listed on the 'Assign Zone'    | >  |
| n | 7 | 3 | im |     page, the scheduled exam time (with start time |  O |
| v |   | . | er |     and end time) and supervised break(s) (with    | ut |
| i |   | 1 |    |     start time and end time) in accordance with    | >  |
| A |   | . |    |     the timetable of candidates shall be displayed |  S |
| p |   | 1 |    |     to the invigilators automatically and          | co |
| p |   | 0 |    |     initially.                                     | pe |
|   |   |   |    |                                                    |    |
|   |   |   |    | 2.  Timetable information of each candidate such   |    |
|   |   |   |    |     as case number, break information, special     |    |
|   |   |   |    |     needs in remarks, etc. shall be provided by    |    |
|   |   |   |    |     the SEN system of HKEAA.                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 3.  Hall Invigilator:                              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [The system shall update and display the   |    |
|   |   |   |    |         actual start and end times of the exam as  |    |
|   |   |   |    |         well as those of the supervised break(s)   |    |
|   |   |   |    |         under each zone automatically after the    |    |
|   |   |   |    |         CS]{.mark} edited [the actual exam start   |    |
|   |   |   |    |         time on the CS panel(see CS                |    |
|   |   |   |    |         Module).]{.mark}                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  Classroom Invigilator:                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Users shall only be able to edit [the      |    |
|   |   |   |    |         actual exam start time of each zone. The   |    |
|   |   |   |    |         system shall then update and display the   |    |
|   |   |   |    |         start and end times of the exam session as |    |
|   |   |   |    |         well as those of the supervised break(s)   |    |
|   |   |   |    |         under each zone accordingly.]{.mark}       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Users shall not be able to edit the       |    |
|   |   |   |    |         actual exam start time of Paper 1 earlier  |    |
|   |   |   |    |         than the regular designated time (i.e.     |    |
|   |   |   |    |         8:30am).]{.mark}                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [The adjustment of time(s) in Paper 1      |    |
|   |   |   |    |         shall not affect the scheduled exam start  |    |
|   |   |   |    |         time of Paper 2 which is provided by the   |    |
|   |   |   |    |         system in default. On the other hand, the  |    |
|   |   |   |    |         users shall be allowed to edit the actual  |    |
|   |   |   |    |         exam start time of Paper 2.]{.mark}        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [The actual exam start time of Paper 1 and |    |
|   |   |   |    |         Paper 2 in the SEN exam centre shall not   |    |
|   |   |   |    |         be earlier than those in the normal        |    |
|   |   |   |    |         centre.]{.mark}                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   The actual exam start time and end time    |    |
|   |   |   |    |         fields of each zone in the sessional       |    |
|   |   |   |    |         report shall be updated based on the timer |    |
|   |   |   |    |         set.                                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Users shall be able to check the exam end |    |
|   |   |   |    |         time in the routine page, see UF-SEN-011   |    |
|   |   |   |    |         Routine.]{.mark}                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [By tapping the 'Rem]{.mark}ove all        |    |
|   |   |   |    |         supervised break(s)' and a 'Confirm to     |    |
|   |   |   |    |         remove all supervised break(s)' button on  |    |
|   |   |   |    |         the page of the candidate list within the  |    |
|   |   |   |    |         zone for a single candidate room, users    |    |
|   |   |   |    |         shall be able to remove the time settings  |    |
|   |   |   |    |         of all scheduled supervised break(s) at    |    |
|   |   |   |    |         once. Validation shall be set to ensure    |    |
|   |   |   |    |         that it is a single candidate room before  |    |
|   |   |   |    |         removal. The system shall then update and  |    |
|   |   |   |    |         display the start and end times of the     |    |
|   |   |   |    |         exam (including the routine)               |    |
|   |   |   |    |         automatically. A message about the removal |    |
|   |   |   |    |         of supervised break(s) shall also be       |    |
|   |   |   |    |         highlighted.                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Provide the no. of candidate to be         |    |
|   |   |   |    |         allocated by zones under the \'Assign      |    |
|   |   |   |    |         Zone\' page \> Zone A (5 candidates)       |    |
+---+---+---+----+----------------------------------------------------+----+
| I | 2 | 1 | R  | 1.  Users shall be able to read the routine of the | >  |
| n | 8 | 3 | ou |     exam session by tapping the \[Routine\] button |  O |
| v |   | . | ti |     in the page of the Assign Zone.                | ut |
| i |   | 1 | ne |                                                    | >  |
| A |   | . |    | 2.  Each action occurring within the exam timeline |  S |
| p |   | 1 |    |     of each assigned zone shall be listed by time  | co |
| p |   | 1 |    |     sequence.                                      | pe |
|   |   |   |    |                                                    |    |
|   |   |   |    |     a.  The start and end time of the exam paper   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     b.  The start and end time of all supervised   |    |
|   |   |   |    |         breaks                                     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     c.  The last 15 minutes and 5 minutes before   |    |
|   |   |   |    |         exam end                                   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | <!-- -->                                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 1.  The actions of the new zone created for the    |    |
|   |   |   |    |     special case (wrong centre candidate) shall be |    |
|   |   |   |    |     included in the exam timeline as well.         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 2.  The system shall be able to display the        |    |
|   |   |   |    |     effective times of the exam automatically if   |    |
|   |   |   |    |     the CS/invigilator adjusted the exam start     |    |
|   |   |   |    |     time and/or the supervised break(s) is/are     |    |
|   |   |   |    |     removed for a single candidate room.           |    |
+---+---+---+----+----------------------------------------------------+----+
| I | 3 | 1 | M  | 1.  Users shall be able to communicate with and    | >  |
| n | 1 | 3 | es |     receive notification from the CS through the   |  O |
| v |   | . | sa |     Message Board.                                 | ut |
| i |   | 1 | ge |                                                    | >  |
| A |   | . | B  | 2.  Users shall be able to receive, be notified    |  S |
| p |   | 1 | oa |     and read one-way messages / information        | co |
| p |   | 2 | rd |     disseminated from HKEAA.                       | pe |
|   |   |   |    |                                                    |    |
|   |   |   |    | 3.  Users shall be able to send/receive messages   |    |
|   |   |   |    |     and [images / audios / videos]{.mark} to/from  |    |
|   |   |   |    |     the CS of the checked-in exam sessions.        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  VCC Manager and Officer role users shall be    |    |
|   |   |   |    |     able to extract the conversation logs.         |    |
+---+---+---+----+----------------------------------------------------+----+
| C | 3 | 1 | S  | 1.  By selecting the Examination Date and SEN      | >  |
| S | 1 | 3 | EN |     Centres, choosing the exam centre, entering    |  O |
|   |   | . | CS |     the EP Number, and Password, the assigned CS   | ut |
|   |   | 2 | L  |     shall be able to login to the SEN CS Module.   | >  |
|   |   | . | og |                                                    |  S |
|   |   | 1 | in | 2.  CS's EP No. shall be used to recognize the     | co |
|   |   |   |    |     specific exam session of the SEN exam centre   | pe |
|   |   |   |    |     that the CS is responsible for.                |    |
+---+---+---+----+----------------------------------------------------+----+
| C | 3 | 1 | Na | 1.  For Hall centres                               | >  |
| S | 2 | 3 | vi |                                                    |  O |
|   |   | . | ga |     -   Users shall be able to click the 'green QR | ut |
|   |   | 2 | ti |         code' icon to prompt a window that shows   | >  |
|   |   | . | on |         the QR code for invigilator to login       |  S |
|   |   | 2 | B  |         'i-Invigilation (HKDSE)' (Invigilator      | co |
|   |   |   | ar |         App).                                      | pe |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   'Pending Confirmation' button shall be     |    |
|   |   |   |    |         used for confirmation or reconfirmation of |    |
|   |   |   |    |         the exam data sent to VCC (applicable to   |    |
|   |   |   |    |         Hall CS).                                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 2.  Users shall be able to click the               |    |
|   |   |   |    |     \[中文\]/\[ENG\] button to switch the language |    |
|   |   |   |    |     to either English or Chinese.                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 3.  Users shall be able to click the 'Selection of |    |
|   |   |   |    |     Subject/Paper' button to switch to another     |    |
|   |   |   |    |     exam session, a message shall be displayed to  |    |
|   |   |   |    |     remind the users to confirm the exam data      |    |
|   |   |   |    |     before switching to another exam session.      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  Users shall be able to click the 'Reports'     |    |
|   |   |   |    |     button to select the shortcut link to          |    |
|   |   |   |    |     Sessional Report, Discrepancy Report and       |    |
|   |   |   |    |     Summary Report.                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 5.  Users shall click the 'Logout' button to       |    |
|   |   |   |    |     logout the SEN CS Module, a message shall be   |    |
|   |   |   |    |     displayed to reminder the users to confirm the |    |
|   |   |   |    |     exam data before log out                       |    |
+---+---+---+----+----------------------------------------------------+----+
| C | 3 | 1 | Ex | 1.  [On every page of the App, users shall be able | >  |
| S | 3 | 3 | am |     to view the basic examination information      |  O |
|   |   | . | I  |     which are retrieved from HKEAA system by       | ut |
|   |   | 2 | nf |     scheduled synchronized job:]{.mark}            | >  |
|   |   | . | or |                                                    |  S |
|   |   | 3 | ma |     -   [Exam name(e.g. DSE 2023)]{.mark}          | co |
|   |   |   | ti |                                                    | pe |
|   |   |   | on |     -   [Exam centre code with the centre          |    |
|   |   |   |    |         name]{.mark}                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Exam date]{.mark}                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [The step instructions to remind the CS to |    |
|   |   |   |    |         submit the Sessional Report(s) and confirm |    |
|   |   |   |    |         the exam data.]{.mark}                     |    |
+---+---+---+----+----------------------------------------------------+----+
| C | 3 | 1 | Ex | 1.  [On every page of the App,]{.mark}             | >  |
| S | 3 | 3 | am |                                                    |  O |
|   |   | . | Ti | 2.  [The system shall display the scheduled exam   | ut |
|   |   | 2 | me |     time of both Paper 1 and 2 of the normal       | >  |
|   |   | . |    |     centre which is retrieved from the HKEAA       |  S |
|   |   | 4 |    |     system.]{.mark}                                | co |
|   |   |   |    |                                                    | pe |
|   |   |   |    | 3.  [The start time of Paper 2 of different        |    |
|   |   |   |    |     subjects on the exam date at the normal centre |    |
|   |   |   |    |     within the message shown as below (i.e. "( )"  |    |
|   |   |   |    |     refers to scheduled start time of Paper 2 in   |    |
|   |   |   |    |     the normal centre), e.g.:]{.mark}              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Note: All candidates of SEN Centres       |    |
|   |   |   |    |         should return to exam rooms before the     |    |
|   |   |   |    |         exam start time of Paper 2 (i.e. *11:15* ) |    |
|   |   |   |    |         in normal exam centres.]{.mark}            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -                                              |    |
|   |   |   |    |  [注意：所有特別試場考生必須於一般試場卷二開考時間 |    |
|   |   |   |    |         (即 *11:15*) 前返回考室。]{.mark}          |    |
+---+---+---+----+----------------------------------------------------+----+
| C | 3 | 1 | L  | 1.  For the hall invigilators who have been        | >  |
| S | 4 | 3 | og |     assigned to the exam session, they shall be    |  O |
|   |   | . | in |     able to login the Invigilator App by scanning  | ut |
|   |   | 2 | Co |     the QR code of the exam session provided by    | >  |
|   |   | . | de |     the hall CS.                                   |  S |
|   |   | 5 | f  |                                                    | co |
|   |   |   | or | 2.  For ad hoc invigilators who have not been      | pe |
|   |   |   | U  |     assigned to any exam session yet, CS shall be  |    |
|   |   |   | si |     able to generate a specific QR code for the    |    |
|   |   |   | ng |     invigilator by entering invigilator's English  |    |
|   |   |   | I  |     name. School Name and Code of the schools      |    |
|   |   |   | nv |     where the invigilators come from shall be      |    |
|   |   |   | ig |     mandatorily selected from the drop-down list:  |    |
|   |   |   | il |                                                    |    |
|   |   |   | at |     -   The drop-down list with all school names   |    |
|   |   |   | or |         and codes shall be displayed at the field  |    |
|   |   |   | A  |         for users to select if no character(s) is  |    |
|   |   |   | pp |         inputted.                                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   By inputting character(s), corresponding   |    |
|   |   |   |    |         school name(s) and code(s) shall be        |    |
|   |   |   |    |         displayed in the drop-down list at the     |    |
|   |   |   |    |         field for users to select.                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   The system shall create a unique account   |    |
|   |   |   |    |         number for the invigilator.                |    |
+---+---+---+----+----------------------------------------------------+----+
| C | 3 | 1 | CS | 1.  [Users shall have an overview of the real-time | >  |
| S | 5 | 3 | D  |     information of the assigned exam centre(s) via |  O |
|   |   | . | as |     the Dashboard page.]{.mark}                    | ut |
|   |   | 2 | hb |                                                    | >  |
|   |   | . | oa | 2.  [Hall CS Dashboard:]{.mark}                    |  S |
|   |   | 6 | rd |                                                    | co |
|   |   |   |    | -   [A summary of attendance records ('Attendance  | pe |
|   |   |   |    |     Record') shall display the following number of |    |
|   |   |   |    |     candidates:]{.mark}                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Present]{.mark}                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Absent]{.mark}                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Wrong Centre / Version                    |    |
|   |   |   |    |         Candidate(S)]{.mark}                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Attendance not taken]{.mark}              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   [A pie chart of an overall situation shall     |    |
|   |   |   |    |     reflect the counts relating to attendance and  |    |
|   |   |   |    |     collected script records.]{.mark}              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [By mouse hovering each sector of the      |    |
|   |   |   |    |         chart, the figure and percentage of the    |    |
|   |   |   |    |         count shall be displayed.]{.mark}          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [The figure of the counts shall be         |    |
|   |   |   |    |         displayed at the legend:]{.mark}           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [Present Candidate(s) with scripts     |    |
|   |   |   |    |             collected]{.mark}                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [Absent Candidate(s) without scripts   |    |
|   |   |   |    |             collected]{.mark}                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [Wrong Centre / Version Candidate(s)   |    |
|   |   |   |    |             with scripts collected]{.mark}         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [Discrepancies]{.mark}                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |             -   [By clicking the sector, the       |    |
|   |   |   |    |                 following counts shall be shown on |    |
|   |   |   |    |                 a dialog box:]{.mark}              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |                 -   [Attendance not taken without  |    |
|   |   |   |    |                     script(s) collected]{.mark}    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |                 -   [Attendance not taken with     |    |
|   |   |   |    |                     script(s) collected]{.mark}    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |                 -   [Present with missing          |    |
|   |   |   |    |                     script(s)]{.mark}              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |                 -   [Absent with script(s)         |    |
|   |   |   |    |                     collected]{.mark}              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |                 -   [Wrong Centre / Version        |    |
|   |   |   |    |                     candidates without script(s)   |    |
|   |   |   |    |                     collected]{.mark}              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |             -   [By clicking each count in the     |    |
|   |   |   |    |                 dialog box, the users shall be     |    |
|   |   |   |    |                 redirected to the corresponding    |    |
|   |   |   |    |                 page of 'Discrepancy               |    |
|   |   |   |    |                 Report'.]{.mark}                   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   [A pie chart of SR Form Status                 |    |
|   |   |   |    |     ('Irregularities') shall reflect the number of |    |
|   |   |   |    |     corresponding SR Form Cases.]{.mark}           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [By mouse hovering each sector of the      |    |
|   |   |   |    |         chart, the figure and percentage of the    |    |
|   |   |   |    |         count shall be displayed.]{.mark}          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [The figure of the counts shall be         |    |
|   |   |   |    |         displayed at the legend:]{.mark}           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [SR Form Cases with \<Completed\>      |    |
|   |   |   |    |             status]{.mark}                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [SR Form Cases with \<Pending to       |    |
|   |   |   |    |             Complete\> status]{.mark}              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |             -   [By clicking the pie of SR Form    |    |
|   |   |   |    |                 Cases with \<Completed\> Status,   |    |
|   |   |   |    |                 the users shall be redirected to   |    |
|   |   |   |    |                 the corresponding page of 'Special |    |
|   |   |   |    |                 Report for follow Up (Candidate)'  |    |
|   |   |   |    |                 showing the completed cases of the |    |
|   |   |   |    |                 SR Forms.]{.mark}                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |             -   [By clicking the pie of SR Form    |    |
|   |   |   |    |                 Cases with \<Pending to Complete\> |    |
|   |   |   |    |                 Status, the users shall be         |    |
|   |   |   |    |                 redirected to the corresponding    |    |
|   |   |   |    |                 page of 'Special Report for follow |    |
|   |   |   |    |                 up (Candidate)' showing the        |    |
|   |   |   |    |                 outstanding cases of the SR        |    |
|   |   |   |    |                 Forms.]{.mark}                     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 3.  [Classroom CS Dashboard:]{.mark}               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   [A bar chart of an overall situation shall     |    |
|   |   |   |    |     reflect the counts relating to attendance and  |    |
|   |   |   |    |     collected script records, at each bar which    |    |
|   |   |   |    |     represents a Classroom centre.]{.mark}         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [By mouse hovering each section of the bar |    |
|   |   |   |    |         of a classroom centre, the counts for      |    |
|   |   |   |    |         Classroom centre(s) ('Classrooms           |    |
|   |   |   |    |         Situation') shall be displayed:]{.mark}    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [Present Candidate(s) with scripts     |    |
|   |   |   |    |             collected]{.mark}                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [Absent Candidate(s) without scripts   |    |
|   |   |   |    |             collected]{.mark}                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [Wrong Centre / Version Candidate(s)   |    |
|   |   |   |    |             with scripts collected]{.mark}         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [Discrepancies]{.mark}                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |             -   [By clicking the section, the      |    |
|   |   |   |    |                 Classroom centre code and the      |    |
|   |   |   |    |                 following counts shall be shown on |    |
|   |   |   |    |                 a dialog box:]{.mark}              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |                 -   [Attendance not taken without  |    |
|   |   |   |    |                     script(s) collected]{.mark}    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |                 -   [Attendance not taken with     |    |
|   |   |   |    |                     script(s) collected]{.mark}    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |                 -   [Present with missing          |    |
|   |   |   |    |                     script(s)]{.mark}              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |                 -   [Absent with script(s)         |    |
|   |   |   |    |                     collected]{.mark}              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |                 -   [Wrong Centre / Version        |    |
|   |   |   |    |                     candidates without script(s)   |    |
|   |   |   |    |                     collected]{.mark}              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |             -   [By clicking each count in the     |    |
|   |   |   |    |                 dialog box, the users shall be     |    |
|   |   |   |    |                 redirected to the corresponding    |    |
|   |   |   |    |                 page of 'Discrepancy Report' under |    |
|   |   |   |    |                 such Classroom centre.]{.mark}     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [The following figure and the percentage   |    |
|   |   |   |    |         of the attendance records shall be         |    |
|   |   |   |    |         displayed as well:]{.mark}                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [Present]{.mark}                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [Absent]{.mark}                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [Wrong Centre/Version                  |    |
|   |   |   |    |             Candidate(s)]{.mark}                   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [Attendance not taken]{.mark}          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   [A bar chart of SR Form Status                 |    |
|   |   |   |    |     ('Irregularities') shall reflect the number of |    |
|   |   |   |    |     corresponding SR Form Cases at each bar which  |    |
|   |   |   |    |     represents a Classroom centre.]{.mark}         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [By mouse hovering each section of the     |    |
|   |   |   |    |         bar, the figure and percentage of the      |    |
|   |   |   |    |         count shall be displayed.]{.mark}          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [The counts for both Classroom             |    |
|   |   |   |    |         centre(s):]{.mark}                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [SR Form Cases with \<Completed\>      |    |
|   |   |   |    |             status]{.mark}                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [SR Form Cases with \<Pending to       |    |
|   |   |   |    |             Complete\> status]{.mark}              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |             -   [By clicking the section of SR     |    |
|   |   |   |    |                 Form Cases with \<Completed\>      |    |
|   |   |   |    |                 Status of the bar of a classroom   |    |
|   |   |   |    |                 centre, the users shall be         |    |
|   |   |   |    |                 redirected to the corresponding    |    |
|   |   |   |    |                 page of 'Special Report for follow |    |
|   |   |   |    |                 up (Candidate)' showing the        |    |
|   |   |   |    |                 completed cases of the SR          |    |
|   |   |   |    |                 Forms.]{.mark}                     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |             -   [By clicking the section of SR     |    |
|   |   |   |    |                 Form Cases with \<Pending to       |    |
|   |   |   |    |                 Complete\> Status of the bar of a  |    |
|   |   |   |    |                 classroom centre, the users shall  |    |
|   |   |   |    |                 be redirected to the corresponding |    |
|   |   |   |    |                 page of 'Special Report for follow |    |
|   |   |   |    |                 Up (Candidate)' showing the        |    |
|   |   |   |    |                 outstanding cases of the SR        |    |
|   |   |   |    |                 Forms.]{.mark}                     |    |
+---+---+---+----+----------------------------------------------------+----+
| C | 4 | 1 | At | 1.  [Users shall be able to view the candidate's   | >  |
| S | 0 | 3 | te |     attendance and script records of the SEN exam  |  O |
|   |   | . | nd |     centre.]{.mark}                                | ut |
|   |   | 2 | an |                                                    | >  |
|   |   | . | ce | 2.  [Users shall be able to filter the records by  |  S |
|   |   | 7 | a  |     selecting:]{.mark}                             | co |
|   |   |   | nd |                                                    | pe |
|   |   |   | Sc |     -   [Attendance status (i.e. present or        |    |
|   |   |   | ri |         absent)]{.mark}                            |    |
|   |   |   | pt |                                                    |    |
|   |   |   | R  |     -   [Status of script collection (i.e.         |    |
|   |   |   | ec |         collected scripts and missing              |    |
|   |   |   | or |         script)]{.mark}                            |    |
|   |   |   | ds |                                                    |    |
|   |   |   |    | 3.  Users shall be able to sort the records by     |    |
|   |   |   |    |     clicking the corresponding field names.        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  [The system shall list and group the candidate |    |
|   |   |   |    |     records under zones having different           |    |
|   |   |   |    |     timetables. Each zone shall consist of         |    |
|   |   |   |    |     candidate records of different subjects having |    |
|   |   |   |    |     the same timetable. Heading of each zone shall |    |
|   |   |   |    |     be shown with its zone name, scheduled exam    |    |
|   |   |   |    |     start and end time, exam duration(including    |    |
|   |   |   |    |     break), and supervised break(s) when mouse     |    |
|   |   |   |    |     hovering the 'View Break Time' icon.]{.mark}   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 5.  [The system shall display candidate records    |    |
|   |   |   |    |     with the following fields:]{.mark}             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Candidate number or identification        |    |
|   |   |   |    |         document number]{.mark}                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Candidate name]{.mark}                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Case number]{.mark}                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Seat number]{.mark}                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Subject name]{.mark}                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Paper code]{.mark}                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Attendance status（\'\--\' means          |    |
|   |   |   |    |         attendance not yet taken, present and      |    |
|   |   |   |    |         absent)]{.mark}                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Answer script collected / answer script   |    |
|   |   |   |    |         to be collected]{.mark}                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Remarks of individual candidate's         |    |
|   |   |   |    |         timetable (if any) provided by             |    |
|   |   |   |    |         HKEAA]{.mark}                              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 6.  [For the case number, the length ranges from   |    |
|   |   |   |    |     11 to 12 characters depending on the trailing  |    |
|   |   |   |    |     numbers followed by the disabilities code,     |    |
|   |   |   |    |     e.g. DSE2021A001 and DSE2021A0001. The format  |    |
|   |   |   |    |     shall be expressed in the following            |    |
|   |   |   |    |     examples:]{.mark}                              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [DSE2021A001. "A" means aural              |    |
|   |   |   |    |         disabilities]{.mark}                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [DSE2021V001. "V" means visual             |    |
|   |   |   |    |         disabilities]{.mark}                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [DSE2021O001. "O" means oral               |    |
|   |   |   |    |         disabilities]{.mark}                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [DSE2021L001. "L" means specific learning  |    |
|   |   |   |    |         disabilities]{.mark}                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [DSE2021P001. "P" means physical           |    |
|   |   |   |    |         disabilities]{.mark}                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [DSE2021X001. "X" means other disabilities |    |
|   |   |   |    |         (e.g. Autism Spectrum Disorder (ASD),      |    |
|   |   |   |    |         Attention-Deficit/Hyperactivity Disorder   |    |
|   |   |   |    |         (AD/HD), intellectual disabilities (ID),   |    |
|   |   |   |    |         disorder related to mental health, chronic |    |
|   |   |   |    |         medical illnesses, etc)]{.mark}            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 7.  [Users shall be able to click the 'View'       |    |
|   |   |   |    |     button to read the candidate's information.    |    |
|   |   |   |    |     Following shall be displayed:]{.mark}          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Candidate name and the candidate number   |    |
|   |   |   |    |         as the title of the popup window.]{.mark}  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Document No.]{.mark}                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Invigilator's Attendance Taking           |    |
|   |   |   |    |         Time]{.mark}                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Self Check-in Time]{.mark}                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [No. of Scripts Collected]{.mark}          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Spare Barcode]{.mark}                     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [SR1 Case Records, such as photo not       |    |
|   |   |   |    |         resemble candidate, admission form not     |    |
|   |   |   |    |         present and cannot verify identity]{.mark} |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Check-in/out (Toilet request)]{.mark}     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Candidate photo in REG]{.mark}            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Remarks of the candidate provided by      |    |
|   |   |   |    |         HKEAA that shall be able to display        |    |
|   |   |   |    |         symbols and wordings in Chinese and        |    |
|   |   |   |    |         English at the same time.]{.mark}          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 8.  [A search bar shall enable the Classroom CS to |    |
|   |   |   |    |     filter the classroom.]{.mark}                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 9.  [Users shall be able to edit the candidate's   |    |
|   |   |   |    |     attendance and scripts collected information   |    |
|   |   |   |    |     in the edit form by clicking the 'Edit'        |    |
|   |   |   |    |     button. The edit page shall display the        |    |
|   |   |   |    |     candidate no, candidate name, seat number and  |    |
|   |   |   |    |     the remarks retrieved from the timetable.      |    |
|   |   |   |    |     Users shall be able to edit the                |    |
|   |   |   |    |     followings:]{.mark}                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Attendance status (i.e. 'Yes' - present   |    |
|   |   |   |    |         or 'No' - absent)]{.mark}                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Usage of spare barcode (i.e. Yes or No)   |    |
|   |   |   |    |         and the spare barcode number if 'Yes is    |    |
|   |   |   |    |         selected', users shall be able to select   |    |
|   |   |   |    |         the subject code from a dropdown list and  |    |
|   |   |   |    |         enter the last 5 digits. A message shall   |    |
|   |   |   |    |         be popped up if the combination of the     |    |
|   |   |   |    |         subject code and the last 5 digits are     |    |
|   |   |   |    |         incorrect (applicable to Hall CS only, for |    |
|   |   |   |    |         classroom centres, assigning spare barcode |    |
|   |   |   |    |         is the duty of the Classroom               |    |
|   |   |   |    |         invigilators)]{.mark}                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Number of scripts collected, for those    |    |
|   |   |   |    |         candidates involved in script discrepancy, |    |
|   |   |   |    |         users shall be required to input reason by |    |
|   |   |   |    |         selecting one of the following options     |    |
|   |   |   |    |         through the radio buttons and then input   |    |
|   |   |   |    |         the corresponding information:]{.mark}     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [Option 1: Candidate has been approved |    |
|   |   |   |    |             to use other answering                 |    |
|   |   |   |    |             methods.]{.mark}                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [Option 2: Others: (Please input the   |    |
|   |   |   |    |             special situation in remarks), a text  |    |
|   |   |   |    |             box shall be provided for the user to  |    |
|   |   |   |    |             input.]{.mark}                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | >                                                  |    |
+---+---+---+----+----------------------------------------------------+----+
| C | 4 | 1 | T  | 1.  [Timetables of the candidates shall be         | >  |
| S | 5 | 3 | im |     retrieved from and updated to the SEN system   |  O |
|   |   | . | er |     of HKEAA.]{.mark}                              | ut |
|   |   | 2 |    |                                                    | >  |
|   |   | . |    | 2.  [Users shall be able to access the timer       |  S |
|   |   | 8 |    |     function via the 'Timer' page.]{.mark}         | co |
|   |   |   |    |                                                    | pe |
|   |   |   |    | 3.  [System shall list and group the exam times    |    |
|   |   |   |    |     under zones having different timetables.       |    |
|   |   |   |    |     Heading of each zone shall be shown with its   |    |
|   |   |   |    |     zone name, scheduled exam start and end time,  |    |
|   |   |   |    |     and exam duration(including break).]{.mark}    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  [System shall show the following times under   |    |
|   |   |   |    |     each zone by time sequence:]{.mark}            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Exam start and end time]{.mark}           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Start time(s) and end time(s) of all the  |    |
|   |   |   |    |         supervised break(s)]{.mark}                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | >                                                  |    |
|   |   |   |    | >                                                  |    |
|   |   |   |    | > [[Hall CS]{.underline}]{.mark}                   |    |
|   |   |   |    | >                                                  |    |
|   |   |   |    | >                                                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   [Users shall only be able to edit the actual   |    |
|   |   |   |    |     exam start time of each zone. Then, the system |    |
|   |   |   |    |     shall update and display the start and end     |    |
|   |   |   |    |     times of the exam session as well as those of  |    |
|   |   |   |    |     the supervised break(s) under each zone        |    |
|   |   |   |    |     automatically.]{.mark}                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   [For the zone does not have any supervised     |    |
|   |   |   |    |     break(s), 'Supervised Break : NA' shall be     |    |
|   |   |   |    |     displayed.]{.mark}                             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   [Users shall not be able to edit the actual    |    |
|   |   |   |    |     exam start time of Paper 1 earlier than the    |    |
|   |   |   |    |     regular designated time (i.e. 8:30am).]{.mark} |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   [The adjustment of time(s) in Paper 1 shall    |    |
|   |   |   |    |     not affect the scheduled exam start time of    |    |
|   |   |   |    |     Paper 2 which is provided by the system in     |    |
|   |   |   |    |     default. On the other hand, the users shall be |    |
|   |   |   |    |     allowed to edit the actual exam start time of  |    |
|   |   |   |    |     Paper 2.]{.mark}                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   [The actual exam start time of Paper 1 and     |    |
|   |   |   |    |     Paper 2 in the SEN exam centre shall not be    |    |
|   |   |   |    |     earlier than those in the normal               |    |
|   |   |   |    |     centre.]{.mark}                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   [Users shall be able to apply the actual exam  |    |
|   |   |   |    |     start time of each zone by clicking the        |    |
|   |   |   |    |     'Confirm' button.]{.mark}                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | >                                                  |    |
|   |   |   |    | >                                                  |    |
|   |   |   |    | > [[Classroom CS]{.underline}]{.mark}              |    |
|   |   |   |    | >                                                  |    |
|   |   |   |    | >                                                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   [A search bar shall enable the Classroom CS to |    |
|   |   |   |    |     filter the classroom.]{.mark}                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   [Classroom CS shall be able to view the exam   |    |
|   |   |   |    |     time of each zone in a filtered classroom,     |    |
|   |   |   |    |     with a heading showing the zone name,          |    |
|   |   |   |    |     scheduled exam start and end time and the exam |    |
|   |   |   |    |     duration(including break).]{.mark}             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   [Followings shall be shown under the zone      |    |
|   |   |   |    |     heading:]{.mark}                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Actual exam start time set by the         |    |
|   |   |   |    |         classroom invigilator]{.mark}              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Exam end time adjusted by the             |    |
|   |   |   |    |         system]{.mark}                             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Start time(s) of supervised break time(s) |    |
|   |   |   |    |         adjusted by the system]{.mark}             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [End times(s) of supervised break time(s)  |    |
|   |   |   |    |         adjusted by the system]{.mark}             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   [Single Candidate Room:]{.mark}                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Users shall be able to remove the time    |    |
|   |   |   |    |         settings of all existing supervised        |    |
|   |   |   |    |         break(s) by clicking the 'Remove All       |    |
|   |   |   |    |         Supervised Break(s)' button at once.       |    |
|   |   |   |    |         Validation shall be set to ensure that it  |    |
|   |   |   |    |         is a single candidate room before          |    |
|   |   |   |    |         removal.]{.mark}                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [A message shall be popup to get the CS's  |    |
|   |   |   |    |         confirmation to remove all supervised      |    |
|   |   |   |    |         breaks when the 'Remove All Supervised     |    |
|   |   |   |    |         Break(s)' button is clicked.]{.mark}       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [The system shall then update and display  |    |
|   |   |   |    |         the exam start and end times               |    |
|   |   |   |    |         automatically. A message about the removal |    |
|   |   |   |    |         of supervised break(s) shall also be       |    |
|   |   |   |    |         highlighted.]{.mark}                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [The adjustment of time(s) in Paper 1      |    |
|   |   |   |    |         shall not affect the scheduled exam start  |    |
|   |   |   |    |         time of Paper 2 which is provided by the   |    |
|   |   |   |    |         system in default. On the other hand, the  |    |
|   |   |   |    |         classroom invigilators shall be allowed to |    |
|   |   |   |    |         edit the actual exam start time of Paper   |    |
|   |   |   |    |         2.]{.mark}                                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [The actual exam start time of Paper 1 and |    |
|   |   |   |    |         Paper 2 in the SEN exam centre shall not   |    |
|   |   |   |    |         be earlier than those in the normal        |    |
|   |   |   |    |         centre.]{.mark}                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | >                                                  |    |
+---+---+---+----+----------------------------------------------------+----+
| C | 4 | 1 | Ma | 1.  [Users shall be able to maintain the special   | >  |
| S | 8 | 3 | in |     cases (wrong centre candidates) in the Special |  O |
|   |   | . | ta |     Case page.]{.mark}                             | ut |
|   |   | 2 | in |                                                    | >  |
|   |   | . | S  | 2.  [Users shall be able to view the Special Case  |  S |
|   |   | 9 | pe |     list with the following fields:]{.mark}        | co |
|   |   |   | ci |                                                    | pe |
|   |   |   | al |     -   [Candidate Number]{.mark}                  |    |
|   |   |   | C  |                                                    |    |
|   |   |   | as |     -   [Candidate name or identification document |    |
|   |   |   | es |         number]{.mark}                             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Classroom centre code (applicable to      |    |
|   |   |   |    |         Classroom CS)]{.mark}                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Zone name and the SEN exam time, e.g. A   |    |
|   |   |   |    |         (SEN Exam Time 8:30 - 10:15)]{.mark}       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Spare barcode number]{.mark}              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Answer script collected / answer script   |    |
|   |   |   |    |         to be collected]{.mark}                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 3.  [Users shall be able to create special case(s) |    |
|   |   |   |    |     (wrong centre candidates) by clicking the      |    |
|   |   |   |    |     'Add' button. Hall CS shall assign the case(s) |    |
|   |   |   |    |     to the existing zone by selecting from a       |    |
|   |   |   |    |     dropdown list while Classroom CS shall assign  |    |
|   |   |   |    |     the case(s) to the existing classroom centre   |    |
|   |   |   |    |     and zone.]{.mark}                              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  [By clicking the '+' icon next to the drop     |    |
|   |   |   |    |     down list of Zone,]{.mark} users shall be able |    |
|   |   |   |    |     to create new zone(s) in the existing exam     |    |
|   |   |   |    |     centre and assign the wrong centre             |    |
|   |   |   |    |     candidate(s) to it., Followings shall be       |    |
|   |   |   |    |     specified to the new zone:                     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Subject                                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Paper                                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Invigilator                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Exam start and end time                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   The time of supervised break(s) - they are |    |
|   |   |   |    |         optional and applicable to the exam        |    |
|   |   |   |    |         lasting 90 minutes or more. Users shall be |    |
|   |   |   |    |         able to add and remove the supervised      |    |
|   |   |   |    |         break time by clicking the '+' and '-'     |    |
|   |   |   |    |         icon respectively.                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 5.  [If a new zone is created and an invigilator   |    |
|   |   |   |    |     is assigned to it in an existing classroom     |    |
|   |   |   |    |     centre, the information shall be reflected on  |    |
|   |   |   |    |     the pages of the 'Invigilator Assignment', the |    |
|   |   |   |    |     'Seating Plan' and Sessional Report.]{.mark}   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | > [ ]{.mark}                                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 6.  [Hall CS shall be able to update the           |    |
|   |   |   |    |     candidate's personal information, spare        |    |
|   |   |   |    |     barcode information, the number of collected   |    |
|   |   |   |    |     scripts and the zone assigned of each special  |    |
|   |   |   |    |     case in the form by clicking the 'Edit'        |    |
|   |   |   |    |     button. Classroom CS shall be able to update   |    |
|   |   |   |    |     the classroom centre assigned                  |    |
|   |   |   |    |     additionally.]{.mark}[[\[1\]]{.underline}      |    |
|   |   |   |    | ](about:blank) [[\[2\]]{.underline}](about:blank)  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 7.  [For those candidates involved in script       |    |
|   |   |   |    |     discrepancy, users shall be required to input  |    |
|   |   |   |    |     reason by selecting one of the following       |    |
|   |   |   |    |     options through the radio buttons and then     |    |
|   |   |   |    |     input the corresponding information:]{.mark}   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Option 1: Candidate has been approved to  |    |
|   |   |   |    |         use other answering methods.]{.mark}       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Option 2: Others: (Please input the       |    |
|   |   |   |    |         special situation in remarks), a text box  |    |
|   |   |   |    |         shall be provided for the user to          |    |
|   |   |   |    |         input.]{.mark}                             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 8.  [Users shall be able to remove special case(s) |    |
|   |   |   |    |     from the list by clicking the 'Remove' button  |    |
|   |   |   |    |     and confirming the action.]{.mark}             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | >                                                  |    |
+---+---+---+----+----------------------------------------------------+----+
| C | 5 | 1 | C  | 1.  [The list shall be able to show all the        | >  |
| S | 6 | 3 | la |     classroom centres with:]{.mark}                |  O |
|   |   | . | ss |                                                    | ut |
|   |   | 2 | ro |     -   [Classroom centre code]{.mark}             | >  |
|   |   | . | om |                                                    |  S |
|   |   | 1 | Li |     -   [Number of assigned candidates]{.mark}     | co |
|   |   | 0 | st |                                                    | pe |
|   |   |   | (  |     -   Actual exam start and end time - in the    |    |
|   |   |   | ap |         format of hh:mn - hh:mn                    |    |
|   |   |   | pl |                                                    |    |
|   |   |   | ic |     -   [EP / application / account number and the |    |
|   |   |   | ab |         name of invigilator]{.mark}                |    |
|   |   |   | le |                                                    |    |
|   |   |   | f  |     -   [Present count, absent count, unverified   |    |
|   |   |   | or |         count (attendance record is not yet        |    |
|   |   |   | C  |         taken)]{.mark}                             |    |
|   |   |   | la |                                                    |    |
|   |   |   | ss |     -   [Number of absent case but with scripts    |    |
|   |   |   | ro |         collected]{.mark}                          |    |
|   |   |   | om |                                                    |    |
|   |   |   | C  |     -   Wrong centre [count]{.mark}                |    |
|   |   |   | S) |                                                    |    |
|   |   |   |    |     -   [Total number of script to be collected    |    |
|   |   |   |    |         (i.e. the total number of scripts need to  |    |
|   |   |   |    |         be collected from the present assigned     |    |
|   |   |   |    |         candidates and the wrong centre            |    |
|   |   |   |    |         candidates)]{.mark}                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Missing scripts (i.e. the total number of  |    |
|   |   |   |    |         scripts not received from the present      |    |
|   |   |   |    |         assigned candidates and the wrong centre   |    |
|   |   |   |    |         candidates)                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Scripts collected from present (i.e. the  |    |
|   |   |   |    |         total number of missing scripts of the     |    |
|   |   |   |    |         present assigned candidates and the wrong  |    |
|   |   |   |    |         centre candidates)]{.mark}                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Submission status of the sessional        |    |
|   |   |   |    |         reports by the classroom invigilators to   |    |
|   |   |   |    |         CS:]{.mark}                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Pending submission - Sessional report  |    |
|   |   |   |    |             not yet submitted                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Submitted - Sessional report submitted |    |
|   |   |   |    |             without Classroom invigilator's        |    |
|   |   |   |    |             remarks                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Submitted with a yellow 'Remark'       |    |
|   |   |   |    |             button - Sessional report submitted    |    |
|   |   |   |    |             with Classroom invigilator's remark.   |    |
|   |   |   |    |             Mouse over the button shall display    |    |
|   |   |   |    |             the remarks inputted by the CRIs.      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   After the Classroom Invigilator has        |    |
|   |   |   |    |         submitted the Sessional Report, the        |    |
|   |   |   |    |         \[View\] button of the corresponding       |    |
|   |   |   |    |         centre shall be enabled and users shall be |    |
|   |   |   |    |         able to view it.                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Submit Sessional Report - for classroom CS |    |
|   |   |   |    |         to submit the classroom's sessional report |    |
|   |   |   |    |         to VCC by selecting single / multiple /    |    |
|   |   |   |    |         all [classroom centre(s) and clicking the  |    |
|   |   |   |    |         \[Submit Sessional Report\]                |    |
|   |   |   |    |         button.]{.mark}                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Submitted time displayed after submission  |    |
|   |   |   |    |         of sessional report to VCC                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Users shall be able to confirm the exam   |    |
|   |   |   |    |         data of the classroom centres to VCC by    |    |
|   |   |   |    |         clicking the \[Confirm Exam Data\]         |    |
|   |   |   |    |         button.]{.mark}                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Confirmed time displayed after             |    |
|   |   |   |    |         confirmation of exam data to VCC           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   After confirming the exam data to VCC,     |    |
|   |   |   |    |         users shall be able to edit the Sessional  |    |
|   |   |   |    |         Report by clicking the \[Edit\] button of  |    |
|   |   |   |    |         the classroom centre.                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 2.  The number of classrooms displayed in a page   |    |
|   |   |   |    |     shall be 20.                                   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 3.  [Users shall be able to select columns         |    |
|   |   |   |    |     displayed by toggling the 'Preferences'        |    |
|   |   |   |    |     button.]{.mark}                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  Users shall be able to filter the classroom    |    |
|   |   |   |    |     centres with / without discrepancy records by  |    |
|   |   |   |    |     selecting the exam centre status.              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 5.  Users shall be able to filter the classroom    |    |
|   |   |   |    |     centres which the sessional reports have been  |    |
|   |   |   |    |     submitted or pending to submit to VCC by       |    |
|   |   |   |    |     selecting the Sessional Report Submission      |    |
|   |   |   |    |     Status.                                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 6.  Users shall be able to easily identify         |    |
|   |   |   |    |     classroom centres with problems with the       |    |
|   |   |   |    |     indicator displayed in the system after the    |    |
|   |   |   |    |     Classroom invigilator has submitted the        |    |
|   |   |   |    |     sessional report.                              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Red vertical bar shall be shown at the row |    |
|   |   |   |    |         header to indicate there is discrepancy    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Green vertical bar shall be shown if the   |    |
|   |   |   |    |         sessional report of the classroom is       |    |
|   |   |   |    |         normal, without discrepancy.               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   The indicators shall be triggered once the |    |
|   |   |   |    |         Classroom Invigilator submitted the        |    |
|   |   |   |    |         sessional report. By default, no indicator |    |
|   |   |   |    |         (colorless vertical bar) is displayed.     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 7.  After the Classroom CS submitted the Sessional |    |
|   |   |   |    |     Report to VCC but not yet confirmed the exam   |    |
|   |   |   |    |     data, if the Classroom Invigilator changes     |    |
|   |   |   |    |     exam data and resubmit the Sessional Report    |    |
|   |   |   |    |     again, Classroom CS should receive an alert to |    |
|   |   |   |    |     submit the Sessional Report to VCC again.      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 8.  Classroom CS shall only be able to confirm the |    |
|   |   |   |    |     exam data after all the sessional reports of   |    |
|   |   |   |    |     the classroom centres are submitted to VCC.    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 9.  Once the classroom CS confirmed the exam data, |    |
|   |   |   |    |     all the classroom invigilators cannot edit the |    |
|   |   |   |    |     exam data (attendance status and script        |    |
|   |   |   |    |     collected) and the sessional reports.          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 10. Classroom CS shall be able to edit the         |    |
|   |   |   |    |     sessional reports of the classroom centre      |    |
|   |   |   |    |     after first confirmation of the exam data or   |    |
|   |   |   |    |     the Classroom Invigilator of a classroom has   |    |
|   |   |   |    |     been checked out before the exam end time.     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 11. After editing the sessional reports, classroom |    |
|   |   |   |    |     CS shall be able to submit them to VCC and     |    |
|   |   |   |    |     confirm the exam data iteratively.             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 12. Users shall submit all finalized sessional     |    |
|   |   |   |    |     reports and confirm all exam data to VCC       |    |
|   |   |   |    |     within the designated period of time (i.e.     |    |
|   |   |   |    |     defined as a parameter at the Exam Support     |    |
|   |   |   |    |     Backend (SEAD) Module) after the exam end time |    |
|   |   |   |    |     of the last exam session among the classroom   |    |
|   |   |   |    |     centres on the same exam day.                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Classroom CS shall be able to input        |    |
|   |   |   |    |         remarks if there is any discrepancy when   |    |
|   |   |   |    |         confirming the exam data.                  |    |
+---+---+---+----+----------------------------------------------------+----+
| C | 6 | 1 | S  | 1.  [Candidates with the same exam time shall be   | >  |
| S | 0 | 3 | EN |     assigned to and shown in a zone with their     |  O |
|   |   | . | I  |     seat numbers, names and candidate numbers by   | ut |
|   |   | 2 | nv |     the system automatically based on their        | >  |
|   |   | . | ig |     timetables. Heading of each zone shall be      |  S |
|   |   | 1 | il |     shown with its zone name, and scheduled exam   | co |
|   |   | 1 | at |     start and end time.]{.mark}                    | pe |
|   |   |   | or |                                                    |    |
|   |   |   | As | 2.  [An exam centre shall be able to accommodate   |    |
|   |   |   | si |     more than one zone.]{.mark}                    |    |
|   |   |   | gn |                                                    |    |
|   |   |   | me | 3.  [Pre-assignment of Invigilator (applicable to  |    |
|   |   |   | nt |     hall centres only):]{.mark}                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Before the invigilators check-in the exam |    |
|   |   |   |    |         session, the CS shall also be able to      |    |
|   |   |   |    |         assign those invigilators based on the     |    |
|   |   |   |    |         invigilator list on the exam date. The     |    |
|   |   |   |    |         corresponding row in the invigilator list  |    |
|   |   |   |    |         and initial assignments shall be displayed |    |
|   |   |   |    |         font colour in 'Grey'.]{.mark}             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [After the invigilators have been          |    |
|   |   |   |    |         assigned, users shall be able to perform   |    |
|   |   |   |    |         the reassignment by clicking the 'Edit'    |    |
|   |   |   |    |         button.]{.mark}                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Once the assigned invigilators have       |    |
|   |   |   |    |         checked in, the corresponding row in the   |    |
|   |   |   |    |         invigilator list and initial assignments   |    |
|   |   |   |    |         shall be turned the font colour in         |    |
|   |   |   |    |         'Black'.]{.mark}                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  [For Hall CS:]{.mark}                          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Users shall assign invigilators to        |    |
|   |   |   |    |         individual zones with their names and EP   |    |
|   |   |   |    |         numbers/Application numbers by selecting   |    |
|   |   |   |    |         the invigilators from the dropdown         |    |
|   |   |   |    |         list.]{.mark}                              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Single invigilator shall be allowed to be |    |
|   |   |   |    |         assigned to multiple zones.]{.mark}        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 5.  [For Classroom CS:]{.mark}                     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Users shall be able to assign checked-in  |    |
|   |   |   |    |         invigilators to individual zones in a      |    |
|   |   |   |    |         classroom centre with their names and EP   |    |
|   |   |   |    |         numbers / Application numbers by selecting |    |
|   |   |   |    |         the invigilators from the dropdown         |    |
|   |   |   |    |         list.]{.mark}                              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Single invigilator shall be allowed to be |    |
|   |   |   |    |         assigned to multiple zones in a classroom  |    |
|   |   |   |    |         centre.]{.mark}                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Multiple invigilators shall be allowed to |    |
|   |   |   |    |         be assigned to a single zone in a          |    |
|   |   |   |    |         classroom centre by clicking the '+'       |    |
|   |   |   |    |         button at the invigilator list.]{.mark}    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Under certain circumstances (e.g. a       |    |
|   |   |   |    |         single candidate room which may not have   |    |
|   |   |   |    |         the formal invigilator), users shall be    |    |
|   |   |   |    |         able to assign themselves as the           |    |
|   |   |   |    |         invigilator to that classroom to perform   |    |
|   |   |   |    |         invigilation besides performing the duties |    |
|   |   |   |    |         of CS at the same time. In this case, the  |    |
|   |   |   |    |         CS shall not be forced logged out of the   |    |
|   |   |   |    |         CS Module after they have logged in the    |    |
|   |   |   |    |         Invigilator App.]{.mark}                   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [A search bar shall enable the Classroom   |    |
|   |   |   |    |         CS to filter the classroom.]{.mark}        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 6.  [Users shall be able to add additional/wrong   |    |
|   |   |   |    |     centre candidate(s) to the zone by clicking    |    |
|   |   |   |    |     the '+' button at the candidate list.]{.mark}  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 7.  [Users shall be able to view the assignment    |    |
|   |   |   |    |     result after applying the settings.]{.mark}    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 8.  [Users shall be able to edit the assignment by |    |
|   |   |   |    |     clicking the 'Edit' button after applying the  |    |
|   |   |   |    |     settings.]{.mark}                              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 9.  Users shall be directed to the 'Seating Plan'  |    |
|   |   |   |    |     page by clicking the \[Seating Plan\] button.  |    |
+---+---+---+----+----------------------------------------------------+----+
| C | 6 | 1 | Cr | 1.  [Users shall be able to take photo of the      | >  |
| S | 5 | 3 | ea |     candidate seating plan or upload the image     |  O |
|   |   | . | te |     file of the candidate seating plan to the      | ut |
|   |   | 2 | S  |     system at any time by clicking the \[Seating   | >  |
|   |   | . | EN |     Plan\] button on the 'Invigilator Assignment'  |  S |
|   |   | 1 | S  |     page, select the 'Seating Plan' or 'Sessional  | co |
|   |   | 2 | ea |     Report' under the 'Reports' at the left side   | pe |
|   |   |   | ti |     menu.]{.mark}                                  |    |
|   |   |   | ng |                                                    |    |
|   |   |   | Pl | 2.  [A message shall be displayed if the seating   |    |
|   |   |   | an |     plan has not been uploaded when users submit   |    |
|   |   |   |    |     the Sessional Report.]{.mark}                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 3.  [The exam information including exam name,     |    |
|   |   |   |    |     centre name, exam date and scheduled exam time |    |
|   |   |   |    |     shall be displayed.]{.mark}                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  [The exam time, the EP number and name of the  |    |
|   |   |   |    |     invigilators who report duty and the           |    |
|   |   |   |    |     candidates of each zone shall be               |    |
|   |   |   |    |     displayed.]{.mark}                             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 5.  [Users shall be able to upload the photo of    |    |
|   |   |   |    |     the seating plan by clicking the upload icon   |    |
|   |   |   |    |     or take a photo using the laptop/tablet camera |    |
|   |   |   |    |     by clicking the camera icon.]{.mark}           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 6.  [After uploading/taking the photo of the       |    |
|   |   |   |    |     seating plan, a thumbnail shall be displayed   |    |
|   |   |   |    |     to indicate the photo of the seating plan has  |    |
|   |   |   |    |     been uploaded to the system.]{.mark}           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 7.  [Users shall be able to enlarge the image file |    |
|   |   |   |    |     by clicking on the thumbnail.]{.mark}          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 8.  [Users shall be able to remove and             |    |
|   |   |   |    |     re-take/re-upload the photo of the seating     |    |
|   |   |   |    |     plan by clicking the \[Edit\] button.]{.mark}  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 9.  [The name and EP number of the CS who          |    |
|   |   |   |    |     takes/uploads the photo of the seating plan    |    |
|   |   |   |    |     and the date and time of photo                 |    |
|   |   |   |    |     taking/uploading shall be displayed.]{.mark}   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 10. For Classroom CS:                              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   A search bar shall enable the users to     |    |
|   |   |   |    |         filter the classroom.                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   If the Classroom Invigilators uploaded the |    |
|   |   |   |    |         seating plan of the classroom centres      |    |
|   |   |   |    |         through their Invigilator App, a           |    |
|   |   |   |    |         thumbnail, the EP number, name of the      |    |
|   |   |   |    |         Classroom Invigilator, the date and time   |    |
|   |   |   |    |         of uploading shall be displayed, Classroom |    |
|   |   |   |    |         CS shall be able to enlarge it by clicking |    |
|   |   |   |    |         on the thumbnail.                          |    |
+---+---+---+----+----------------------------------------------------+----+
| C | 6 | 1 | S  | 1.  [Lists of invigilators shall be displayed with | >  |
| S | 8 | 3 | EN |     the following fields under the 'Invigilator    |  O |
|   |   | . | I  |     Assignment and Check-in Status'                | ut |
|   |   | 2 | nv |     section:]{.mark}                               | >  |
|   |   | . | ig |                                                    |  S |
|   |   | 1 | il |     -   [Invigilator name]{.mark}                  | co |
|   |   | 3 | at |                                                    | pe |
|   |   |   | or |     -   [EP number/Application number/account      |    |
|   |   |   | Ch |         number for ad hoc invigilator]{.mark}      |    |
|   |   |   | ec |                                                    |    |
|   |   |   | k- |     -   [Check-in time]{.mark}                     |    |
|   |   |   | in |                                                    |    |
|   |   |   | St |     -   [Check-out time]{.mark}                    |    |
|   |   |   | at |                                                    |    |
|   |   |   | us | 2.  [The following lists shall be                  |    |
|   |   |   |    |     included:]{.mark}                              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [A list of invigilators who have           |    |
|   |   |   |    |         checked-in/reported for duty]{.mark}       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [A list of invigilators who have           |    |
|   |   |   |    |         checked-out]{.mark}                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [A list of invigilators who did not check  |    |
|   |   |   |    |         in]{.mark}                                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 3.  [Users shall be able to update the attendance  |    |
|   |   |   |    |     status of invigilators via a 'Check-out'       |    |
|   |   |   |    |     button.]{.mark}                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  [The check-in status and check-out time of the |    |
|   |   |   |    |     invigilators concerned shall then be updated   |    |
|   |   |   |    |     accordingly.]{.mark}                           |    |
+---+---+---+----+----------------------------------------------------+----+
| C | 6 | 1 | S  | 1.  [Users shall be able to preview, edit and      | >  |
| S | 9 | 3 | es |     submit the Sessional Report of the SEN exam    |  O |
|   |   | . | si |     centres to VCC.]{.mark}                        | ut |
|   |   | 2 | on |                                                    | >  |
|   |   | . | al | 2.  [Following fields shall be displayed in a      |  S |
|   |   | 1 | Re |     Sessional Report:]{.mark}                      | co |
|   |   | 4 | po |                                                    | pe |
|   |   |   | rt |     -   [Exam centre number]{.mark}                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Exam centre name]{.mark}                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Exam date]{.mark}                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Actual exam start time and end time of    |    |
|   |   |   |    |         each zone (editable)]{.mark}               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Different subject names and paper codes   |    |
|   |   |   |    |         shall be listed under each zone, including |    |
|   |   |   |    |         the new created zone]{.mark}               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Packet of exam paper received             |    |
|   |   |   |    |         (editable)]{.mark}                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Number of scripts collected               |    |
|   |   |   |    |         (editable)]{.mark}                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Candidates with script discrepancy - a    |    |
|   |   |   |    |         list of candidate numbers and name who     |    |
|   |   |   |    |         involves script discrepancy]{.mark}        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Invigilators number and name who involves |    |
|   |   |   |    |         Special Report on irregularity]{.mark}     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Candidate number and name who involves    |    |
|   |   |   |    |         Special Report on irregularity]{.mark}     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Reception mode - applicable to listening  |    |
|   |   |   |    |         test]{.mark}                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Reception quality - applicable to         |    |
|   |   |   |    |         listening test]{.mark}                     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [\[Seating Plan\] button - users shall be  |    |
|   |   |   |    |         directed to the Seating Plan page by       |    |
|   |   |   |    |         clicking this button.]{.mark}              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 3.  For Hall CS:                                   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Users shall send the sessional report to   |    |
|   |   |   |    |         an invigilator for confirmation.           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   A message shall be displayed if the        |    |
|   |   |   |    |         seating plan has not been uploaded when    |    |
|   |   |   |    |         submitting the Sessional Report.           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Users shall submit the finalized sessional |    |
|   |   |   |    |         report to VCC within the designated period |    |
|   |   |   |    |         of time (i.e. defined as a parameter at    |    |
|   |   |   |    |         the Exam Support Backend (SEAD) Module)    |    |
|   |   |   |    |         after the exam end time of the last exam   |    |
|   |   |   |    |         session on the same exam day.              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  [For Classroom CS:]{.mark}                     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [A search bar shall enable the Classroom   |    |
|   |   |   |    |         CS to filter the classroom.]{.mark}        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [A message shall be displayed if the       |    |
|   |   |   |    |         seating plan]{.mark} has [not been         |    |
|   |   |   |    |         uploaded in any classroom centre when      |    |
|   |   |   |    |         submitting the Sessional Reports.]{.mark}  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Users shall also be able to preview and   |    |
|   |   |   |    |         submit the Sessional Reports of all the    |    |
|   |   |   |    |         classrooms (individual selection, multiple |    |
|   |   |   |    |         selection and select all records shall be  |    |
|   |   |   |    |         enabled) to VCC through the classroom list |    |
|   |   |   |    |         additionally.]{.mark}                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Users shall be able to re-edit and         |    |
|   |   |   |    |         re-submit the sessional report after its   |    |
|   |   |   |    |         first exam data confirmation when there    |    |
|   |   |   |    |         are any exam data                          |    |
|   |   |   |    |         changes.[[\[1\]]{.underline}               |    |
|   |   |   |    | ](about:blank) [[\[2\]]{.underline}](about:blank)  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Users shall submit all finalized          |    |
|   |   |   |    |         sessional reports to VCC within the        |    |
|   |   |   |    |         designated period of time (i.e. defined as |    |
|   |   |   |    |         a parameter at the Exam Support Backend    |    |
|   |   |   |    |         (SEAD) Module) after the exam end time of  |    |
|   |   |   |    |         the last exam session among the classroom  |    |
|   |   |   |    |         centres on the same exam day.]{.mark}      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Users shall also be able to view the      |    |
|   |   |   |    |         Summary of Sessional Report for all        |    |
|   |   |   |    |         classroom centres. Searching and sorting   |    |
|   |   |   |    |         of records shall be p]{.mark}rovided. [The |    |
|   |   |   |    |         following fields of sessional report shall |    |
|   |   |   |    |         be displayed in the Summary and the users  |    |
|   |   |   |    |         shall be able to view the corresponding    |    |
|   |   |   |    |         report by clicking the 'View'              |    |
|   |   |   |    |         button:]{.mark}                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [Centre Code]{.mark}                   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [Actual Starting Time]{.mark}          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [Broadcast Finishing Time (i.e.        |    |
|   |   |   |    |             applicable to listening test)]{.mark}  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [Actual Finishing Time]{.mark}         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [Number of Packets of Question Paper   |    |
|   |   |   |    |             Received]{.mark}                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [Number of Scripts Collected of        |    |
|   |   |   |    |             Present Candidates]{.mark}             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [Number of IRR of Candidates]{.mark}   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [Number of IRR of Invigilators]{.mark} |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [Reception Mode (i.e. applicable to    |    |
|   |   |   |    |             listening test)]{.mark}                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [Reception Quality (i.e. applicable to |    |
|   |   |   |    |             listening test)]{.mark}                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | >                                                  |    |
+---+---+---+----+----------------------------------------------------+----+
| C | 7 | 1 | D  | 1.  [Users shall be able to view the discrepancy   | >  |
| S | 5 | 3 | is |     report grouped by the zones in the SEN exam    |  O |
|   |   | . | cr |     centre.]{.mark}                                | ut |
|   |   | 2 | ep |                                                    | >  |
|   |   | . | an | 2.  [Heading of each zone shall be shown with its  |  S |
|   |   | 1 | cy |     zone name, scheduled exam start and end time,  | co |
|   |   | 5 | Re |     and exam duration. Each record shall be shown  | pe |
|   |   |   | po |     with the following fields:]{.mark}             |    |
|   |   |   | rt |                                                    |    |
|   |   |   |    |     -   [Candidate Type (i.e. Allocated or Special |    |
|   |   |   |    |         Case Candidates)]{.mark}                   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Candidate number or identification        |    |
|   |   |   |    |         document number]{.mark}                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Candidate name]{.mark}                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Seat Number]{.mark}                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Subject name]{.mark}                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Paper code]{.mark}                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Spare barcode number (if any)]{.mark}     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Remarks (i.e. types of                    |    |
|   |   |   |    |         discrepancies)]{.mark}                     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 3.  [4 types of discrepancy shall be shown with    |    |
|   |   |   |    |     filtering function:]{.mark}                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Missing attendance record(s)               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Missing attendance with script collected   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Missing script record(s) - for those       |    |
|   |   |   |    |         candidates with script discrepancy but     |    |
|   |   |   |    |         with reason provided should not be counted |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Absent with script collected               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  Searching and sorting of records shall be      |    |
|   |   |   |    |     provided.                                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 5.  [For Hall CS, users shall be able to select    |    |
|   |   |   |    |     discrepancy reports on all candidates,         |    |
|   |   |   |    |     allocated candidates and special case          |    |
|   |   |   |    |     candidates in the assigned exam centre through |    |
|   |   |   |    |     the tabs.]{.mark}                              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 6.  [A search bar shall enable the Classroom CS to |    |
|   |   |   |    |     filter the classroom.]{.mark}                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 7.  [Users shall be able to edit the exam data of  |    |
|   |   |   |    |     the candidates to clear the discrepancies by   |    |
|   |   |   |    |     clicking the 'Edit' button. Candidate number,  |    |
|   |   |   |    |     candidate name shall be displayed and          |    |
|   |   |   |    |     followings shall be edited:]{.mark}            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Attendance status (i.e. 'Yes' - present   |    |
|   |   |   |    |         or 'No' - absent)]{.mark}                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Usage of spare barcode (i.e. Yes or No)   |    |
|   |   |   |    |         and the spare barcode number if 'Yes' is   |    |
|   |   |   |    |         selected. Users shall be able to select    |    |
|   |   |   |    |         the subject code from a dropdown list and  |    |
|   |   |   |    |         input the last 5 digits. A message shall   |    |
|   |   |   |    |         be popped up if the combination of the     |    |
|   |   |   |    |         subject code and the last 5 digits are     |    |
|   |   |   |    |         incorrect (applicable to Hall exam         |    |
|   |   |   |    |         Centre).]{.mark}                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Number of scripts collected, for those    |    |
|   |   |   |    |         candidates involved in script discrepancy, |    |
|   |   |   |    |         users shall be required to input reason by |    |
|   |   |   |    |         selecting one of the following options     |    |
|   |   |   |    |         through the radio buttons and then input   |    |
|   |   |   |    |         the corresponding information:]{.mark}     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [Option 1: Candidate has been approved |    |
|   |   |   |    |             to use other answering                 |    |
|   |   |   |    |             methods.]{.mark}                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   [Option 2: Others: (Please input the   |    |
|   |   |   |    |             special situation in remarks), a text  |    |
|   |   |   |    |             box shall be provided for the user to  |    |
|   |   |   |    |             input.]{.mark}                         |    |
+---+---+---+----+----------------------------------------------------+----+
| C | 7 | 1 | S  | 1.  [Users shall be able to view the summary       | >  |
| S | 8 | 3 | um |     report(s) with the total count of the          |  O |
|   |   | . | ma |     following information on allocated candidates  | ut |
|   |   | 2 | ry |     and special case candidates in an SEN exam     | >  |
|   |   | . | Re |     centre(s):]{.mark}                             |  S |
|   |   | 1 | po |                                                    | co |
|   |   | 6 | rt |     -   [Centre Code (i.e. applicable to Classroom | pe |
|   |   |   |    |         CS)]{.mark}                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Number of Allocated Candidates]{.mark}    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Present Count]{.mark}                     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Number of answer scripts collected /      |    |
|   |   |   |    |         Number of answer scripts to be collected   |    |
|   |   |   |    |         from Allocated Candidates]{.mark}          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Number of Special Case]{.mark}            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Number of answer scripts collected /      |    |
|   |   |   |    |         Number of answer scripts to be collected   |    |
|   |   |   |    |         from Special Cases]{.mark}                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 2.  [By expanding the total count record of each   |    |
|   |   |   |    |     SEN exam centre, users shall also be able to   |    |
|   |   |   |    |     view the summary report(s) on allocated        |    |
|   |   |   |    |     candidates and special case candidates that    |    |
|   |   |   |    |     are grouped by the zones of the exam centre.   |    |
|   |   |   |    |     The information shall includes the             |    |
|   |   |   |    |     followings:]{.mark}                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Zone Name]{.mark}                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Number of Allocated Candidates]{.mark}    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Present Count]{.mark}                     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Number of answer scripts collected /      |    |
|   |   |   |    |         Number of answer scripts to be collected   |    |
|   |   |   |    |         from Allocated Candidates]{.mark}          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Number of Special Case]{.mark}            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Number of answer scripts collected /      |    |
|   |   |   |    |         Number of answer scripts to be collected   |    |
|   |   |   |    |         from Special Cases]{.mark}                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 3.  [Searching and sorting of records shall be     |    |
|   |   |   |    |     provided.]{.mark}                              |    |
+---+---+---+----+----------------------------------------------------+----+
| C | 8 | 1 | Ir | 1.  [Users shall be able to handle and view the    | >  |
| S | 0 | 3 | re |     irregularities (e.g. screenshot events) of all |  O |
|   |   | . | gu |     the zones in the SEN exam centre.]{.mark}      | ut |
|   |   | 2 | la |                                                    | >  |
|   |   | . | ri | 2.  [SR Forms Module shall be applied here (see    |  S |
|   |   | 1 | ti |     details in SR Form Module).]{.mark}            | co |
|   |   | 7 | es |                                                    | pe |
|   |   |   | (  |                                                    |    |
|   |   |   | al |                                                    |    |
|   |   |   | so |                                                    |    |
|   |   |   | r  |                                                    |    |
|   |   |   | ef |                                                    |    |
|   |   |   | er |                                                    |    |
|   |   |   | to |                                                    |    |
|   |   |   | t  |                                                    |    |
|   |   |   | he |                                                    |    |
|   |   |   | fu |                                                    |    |
|   |   |   | nc |                                                    |    |
|   |   |   | ti |                                                    |    |
|   |   |   | on |                                                    |    |
|   |   |   | al |                                                    |    |
|   |   |   | sp |                                                    |    |
|   |   |   | ec |                                                    |    |
|   |   |   | if |                                                    |    |
|   |   |   | ic |                                                    |    |
|   |   |   | at |                                                    |    |
|   |   |   | io |                                                    |    |
|   |   |   | ns |                                                    |    |
|   |   |   | of |                                                    |    |
|   |   |   | SR |                                                    |    |
|   |   |   | f  |                                                    |    |
|   |   |   | or |                                                    |    |
|   |   |   | m) |                                                    |    |
+---+---+---+----+----------------------------------------------------+----+
| C | 8 | 1 | C  | 1.  [System shall display the confirmation status  | >  |
| S | 2 | 3 | on |     of an exam session as 'Pending Confirmation'   |  O |
|   |   | . | fi |     before users confirm the accuracy of the       | ut |
|   |   | 2 | rm |     attendance and collected script data of the    | >  |
|   |   | . | At |     exam session.]{.mark}                          |  S |
|   |   | 1 | te |                                                    | co |
|   |   | 8 | nd | 2.  [Users shall be able to confirm the accuracy   | pe |
|   |   |   | an |     of the attendance and collected script data of |    |
|   |   |   | ce |     the exam session by clicking the 'Pending      |    |
|   |   |   | a  |     Confirmation' button.]{.mark}                  |    |
|   |   |   | nd |                                                    |    |
|   |   |   | C  | 3.  [System shall display the reason of the        |    |
|   |   |   | ol |     discrepancy records if the user has input when |    |
|   |   |   | le |     submitting the Sessional Report which is       |    |
|   |   |   | ct |     pending for clearance, e]{.mark}ither the      |    |
|   |   |   | ed |     'Candidate has been approved to use other      |    |
|   |   |   | Sc |     answering methods. Please input the actual     |    |
|   |   |   | ri |     number of answer scripts collected.' or the    |    |
|   |   |   | pt |     'Others' with user input the special           |    |
|   |   |   | R  |     situation.                                     |    |
|   |   |   | ec |                                                    |    |
|   |   |   | or | 4.  [System shall update the confirmation status   |    |
|   |   |   | ds |     as 'Confirmed' with a timestamp after the      |    |
|   |   |   |    |     users confirm the accuracy of the attendance   |    |
|   |   |   |    |     and collected script data of the exam          |    |
|   |   |   |    |     session.]{.mark}                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 5.  [Users shall be able to re-confirm the exam    |    |
|   |   |   |    |     data accuracy. As such, a new 'confirmed'      |    |
|   |   |   |    |     timestamp will be reflected in the CS and VCC  |    |
|   |   |   |    |     Exam Centre pages.]{.mark}                     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 6.  [An alert shall be prompted if the users       |    |
|   |   |   |    |     attempt to log out before confirming the exam  |    |
|   |   |   |    |     data accuracy of the attendance and collected  |    |
|   |   |   |    |     script data.]{.mark}                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 7.  [Users shall be able to receive a notification |    |
|   |   |   |    |     after HKEAA confirmed the accuracy of the      |    |
|   |   |   |    |     attendance and collected script records of     |    |
|   |   |   |    |     their responsible exam sessions.]{.mark}       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | >                                                  |    |
|   |   |   |    | >                                                  |    |
|   |   |   |    | > [[For Classroom CS:]{.underline}]{.mark}         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   [After all the Classroom invigilators          |    |
|   |   |   |    |     submitted the Sessional Reports to the         |    |
|   |   |   |    |     Classroom CS, the Classroom CS shall be able   |    |
|   |   |   |    |     to submit the Sessional Reports to VCC,, then  |    |
|   |   |   |    |     the exam data shall be confirmed to VCC by the |    |
|   |   |   |    |     Classroom CS through the Classroom             |    |
|   |   |   |    |     List.]{.mark}                                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   [Users shall be able to easily identify        |    |
|   |   |   |    |     classroom centres with problems through the    |    |
|   |   |   |    |     indicator displayed in the list after the      |    |
|   |   |   |    |     Classroom invigilator has submitted the        |    |
|   |   |   |    |     sessional report:]{.mark}                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Red indicator shall be shown at the row   |    |
|   |   |   |    |         header to indicate that there is           |    |
|   |   |   |    |         discrepancy.]{.mark}                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Green indicator shall be shown at the row |    |
|   |   |   |    |         header to indicate that there is no        |    |
|   |   |   |    |         discrepancy.]{.mark}                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   [Users shall be able to view the remarks of    |    |
|   |   |   |    |     sessional reports submitted by the CRIs        |    |
|   |   |   |    |     through the 'Remark' button.]{.mark}           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   [After the Classroom invigilator submitted the |    |
|   |   |   |    |     Sessional Report and the Classroom CS          |    |
|   |   |   |    |     submitted the Sessional Report to VCC but not  |    |
|   |   |   |    |     yet confirm the exam data, if the Classroom    |    |
|   |   |   |    |     invigilator changes exam data and submit the   |    |
|   |   |   |    |     Sessional Report again, Classroom CS shall     |    |
|   |   |   |    |     receive alert to submit the Sessional Report   |    |
|   |   |   |    |     to VCC again.]{.mark}                          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   [Before the 1st time confirmation of the exam  |    |
|   |   |   |    |     data by the Classroom CS, Classroom            |    |
|   |   |   |    |     invigilator shall be able to re-edit and       |    |
|   |   |   |    |     re-submit the Sessional Report. Classroom CS   |    |
|   |   |   |    |     shall receive an alert if the Classroom        |    |
|   |   |   |    |     Invigilator changes the exam data.]{.mark}     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   [Users shall be able to single/multiple select |    |
|   |   |   |    |     and select all records to submit the Sessional |    |
|   |   |   |    |     Reports through the checkbox(es) and then      |    |
|   |   |   |    |     click the 'Submit Sessional Report'            |    |
|   |   |   |    |     button.]{.mark}                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   \[Confirm Exam Data\] button shall be enabled  |    |
|   |   |   |    |     for the users to confirm exam data to VCC at   |    |
|   |   |   |    |     once after the submission of all Sessional     |    |
|   |   |   |    |     Reports to VCC.                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   Classroom invigilators shall not be able to    |    |
|   |   |   |    |     edit the exam data after Classroom CS has      |    |
|   |   |   |    |     confirmed the exam data.                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   The 'Edit' button shall be enabled for         |    |
|   |   |   |    |     Classroom CS to edit the Sessional Report      |    |
|   |   |   |    |     after Classroom CS's first time exam data      |    |
|   |   |   |    |     confirmation or a Classroom Invigilator has    |    |
|   |   |   |    |     checked out before the exam end before the     |    |
|   |   |   |    |     exam data confirmation                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   Users shall submit all finalized sessional     |    |
|   |   |   |    |     reports and confirm all exam data to VCC       |    |
|   |   |   |    |     within the designated period of time (i.e.     |    |
|   |   |   |    |     defined as a parameter at the Exam Support     |    |
|   |   |   |    |     Backend (SEAD) Module) after the exam end time |    |
|   |   |   |    |     of the last exam session among the classroom   |    |
|   |   |   |    |     centres on the same exam day.                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | >                                                  |    |
+---+---+---+----+----------------------------------------------------+----+
| C | 8 | 1 | M[ | 1.  [sers shall be able to retrieve, be notified   | >  |
| S | 4 | 3 | es |     and read messages or information from          |  O |
|   |   | . | sa |     HKEAA.]{.mark}                                 | ut |
|   |   | 2 | ge |                                                    | >  |
|   |   | . | B  | 2.  [Users shall be able to disseminate            |  S |
|   |   | 1 | oa |     message/information from HKEAA to one or       | co |
|   |   | 9 | rd |     selected invigilators who have checked-in      | pe |
|   |   |   | ]{ |     their responsible exam sessions.]{.mark}       |    |
|   |   |   | .m |                                                    |    |
|   |   |   | ar | 3.  [Users shall be able to exchange messages with |    |
|   |   |   | k} |     VCC staff instantly. Due to individual         |    |
|   |   |   |    |     schools' privacy, messaging between CSs of     |    |
|   |   |   |    |     different exam centres are restricted.]{.mark} |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  [Users shall be able to send messages and      |    |
|   |   |   |    |     images / audios / videos to the VCC            |    |
|   |   |   |    |     users.]{.mark}                                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 5.  [Users shall be able to create invigilator     |    |
|   |   |   |    |     groups and communicate with particular groups  |    |
|   |   |   |    |     of invigilators.]{.mark}                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 6.  [System Administration shall be able to        |    |
|   |   |   |    |     extract all the message logs.]{.mark}          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 7.  [Users shall be able to disseminate the        |    |
|   |   |   |    |     information to individual/all invigilators     |    |
|   |   |   |    |     directly.]{.mark}                              |    |
+---+---+---+----+----------------------------------------------------+----+
| C | 8 | 1 | CS | 1.  [There is an instruction in the box of the     | >  |
| S | 5 | 3 | I  |     exam information to guide the users to submit  |  O |
|   |   | . | ns |     the Sessional Report and confirm the exam data | ut |
|   |   | 2 | tr |     after the exam ended.]{.mark}                  | >  |
|   |   | . | uc |                                                    |  S |
|   |   | 2 | ti | 2.  [For Hall CS:]{.mark}                          | co |
|   |   | 0 | on |                                                    | pe |
|   |   |   | to |     -   [Before the exam ends, steps of the        |    |
|   |   |   | Su |         Sessional Report submission and the exam   |    |
|   |   |   | bm |         data confirmation shall be                 |    |
|   |   |   | it |         displayed.]{.mark}                         |    |
|   |   |   | S  |                                                    |    |
|   |   |   | es |     -   [After the exam ends, the step number of   |    |
|   |   |   | si |         the Sessional Report submission shall      |    |
|   |   |   | on |         become bigger to remind the user to submit |    |
|   |   |   | al |         the sessional report.]{.mark}              |    |
|   |   |   | Re |                                                    |    |
|   |   |   | po |     -   [After the users submitted the sessional   |    |
|   |   |   | rt |         report, the step number of the Sessional   |    |
|   |   |   | a  |         Report submission shall become a green     |    |
|   |   |   | nd |         tick, and the step number of the exam data |    |
|   |   |   | C  |         confirmation shall become bigger.]{.mark}  |    |
|   |   |   | on |                                                    |    |
|   |   |   | fi |     -   [After users confirm the exam data         |    |
|   |   |   | rm |         confirmation, the step number of the exam  |    |
|   |   |   | Ex |         data confirmation shall become a green     |    |
|   |   |   | am |         tick.]{.mark}                              |    |
|   |   |   | Da |                                                    |    |
|   |   |   | ta |     -   [If users edit the exam data after         |    |
|   |   |   |    |         confirming the exam data, it shall be back |    |
|   |   |   |    |         to point 2.2.]{.mark}                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [These steps shall be iterated until both  |    |
|   |   |   |    |         the step numbers become green ticks that   |    |
|   |   |   |    |         implies that the processes have been       |    |
|   |   |   |    |         finished.]{.mark}                          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 3.  [For Classroom CS:]{.mark}                     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Users need to submit the Sessional        |    |
|   |   |   |    |         Reports of all the classroom centres       |    |
|   |   |   |    |         before confirming the exam data.]{.mark}   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Before the exam ends, steps of the        |    |
|   |   |   |    |         Receiving all classrooms' Sessional        |    |
|   |   |   |    |         Reports, Sessional Report submission to    |    |
|   |   |   |    |         VCC and the exam data confirmation shall   |    |
|   |   |   |    |         be displayed.]{.mark}                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [After the exam ended, the step number of  |    |
|   |   |   |    |         Receiving all classrooms' Sessional        |    |
|   |   |   |    |         Reports shall become bigger.]{.mark}       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Until all the classrooms' Sessional       |    |
|   |   |   |    |         Reports have been received, the step       |    |
|   |   |   |    |         number of Receiving all classrooms'        |    |
|   |   |   |    |         Sessional Reports shall be displayed as a  |    |
|   |   |   |    |         green tick.]{.mark}                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [Once all the classrooms' Sessional        |    |
|   |   |   |    |         Reports have been received, the step       |    |
|   |   |   |    |         number of Submit Sessional Reports to VCC  |    |
|   |   |   |    |         shall become bigger.]{.mark}               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [After all the classrooms' Sessional       |    |
|   |   |   |    |         Reports have been submitted to VCC, the    |    |
|   |   |   |    |         step number of Submit Sessional Reports to |    |
|   |   |   |    |         VCC shall be displayed as a green tick and |    |
|   |   |   |    |         the step number of exam data confirmation  |    |
|   |   |   |    |         shall become bigger.]{.mark}               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [After users confirm the exam data, the    |    |
|   |   |   |    |         step number of the exam data confirmation  |    |
|   |   |   |    |         shall become a green tick.]{.mark}         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   [If users edit the exam data after         |    |
|   |   |   |    |         confirmation, it should go back to point   |    |
|   |   |   |    |         3.5 to remind the users to submit the      |    |
|   |   |   |    |         Sessional Report to VCC again.]{.mark}     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | >                                                  |    |
|   |   |   |    | >                                                  |    |
|   |   |   |    | >                                                  |    |
+---+---+---+----+----------------------------------------------------+----+
| V | 9 | 1 | G  | 1.  Data shown on the pages of Dashboard and Exam  | >  |
| C | 0 | 3 | en |     Centre is refreshed automatically every 5      |  O |
| C |   | . | er |     seconds throughout the exam session.           | ut |
|   |   | 3 | al |                                                    | >  |
|   |   |   | R  | 2.  Records of Centres without any update on the   |  S |
|   |   |   | eq |     attendance figures after a designated period   | co |
|   |   |   | ui |     of time (i.e. specified as parameter at Exam   | pe |
|   |   |   | re |     Support Backend (SEAD), e.g. 15 mins) from the |    |
|   |   |   | me |     scheduled exam start time shall be floated on  |    |
|   |   |   | nt |     top and highlighted in 'red' colour in the     |    |
|   |   |   |    |     tables (under Exam Centres and Dashboard       |    |
|   |   |   |    |     pages) automatically.                          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 3.  Roles of Manager, Officer and Operator are     |    |
|   |   |   |    |     able to view both the hall centres and         |    |
|   |   |   |    |     classroom centres of an exam school.           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  Users shall be able to filter the exam data by |    |
|   |   |   |    |     selecting the criteria listed below:           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Operator - applicable to officer / manager |    |
|   |   |   |    |         role users                                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Exam date - default to system date         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Centre type                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Subject code-paper group - e.g. A020E-1,   |    |
|   |   |   |    |         only provide the subject papers of the     |    |
|   |   |   |    |         selected exam date for user filtering      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Subject name                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Centre code                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   School code                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   School name                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Scheduled exam end time (in the format of  |    |
|   |   |   |    |         hh:mn, there are few exam end time in the  |    |
|   |   |   |    |         same exam session because of the           |    |
|   |   |   |    |         supervised                                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   CS logged in - Yes/No                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Attendance/Scripts Discrepancy - Yes/No    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Yes - missing attendance + Missing     |    |
|   |   |   |    |             script + absent with script \> 0       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   No - missing attendance + Missing      |    |
|   |   |   |    |             script + absent with script = 0        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Sessional report submitted - Yes/No        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Notified CS - Yes/No                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   If the CS edited exam data after       |    |
|   |   |   |    |             helpdesk/operator notification, it     |    |
|   |   |   |    |             should be considered as No.            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 5.  For Subject name, Centre code, School code and |    |
|   |   |   |    |     School name, the system shall filter and       |    |
|   |   |   |    |     display relevant data in the dropdown list for |    |
|   |   |   |    |     selection according to the character(s)        |    |
|   |   |   |    |     entered by the users.                          |    |
+---+---+---+----+----------------------------------------------------+----+
| V | 9 | 1 | L  | 1.  Only allow VCC Manager, Officer, or Operator   | >  |
| C | 2 | 3 | og |     role with SEN permission to view the SEN       |  O |
| C |   | . | in |     centre data, and they are restricted to access | ut |
|   |   | 3 |    |     SEN exam centres only.                         | >  |
|   |   | . |    |                                                    |  S |
|   |   | 1 |    |                                                    | co |
|   |   |   |    |                                                    | pe |
+---+---+---+----+----------------------------------------------------+----+
| V | 9 | 1 | D  | 1.  An initial page of the Dashboard shall be      | >  |
| C | 3 | 3 | as |     displayed after the users login to the VCC     |  O |
| C |   | . | hb |     until the selection is made by filtering the   | ut |
|   |   | 3 | oa |     event at the left side menu.                   | >  |
|   |   | . | rd |                                                    |  S |
|   |   | 2 |    | 2.  The Dashboard page of a helpdesk/an operator   | co |
|   |   |   |    |     shall display the overviews of his/her         | pe |
|   |   |   |    |     assigned exam centes:                          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   A pie chart of an overview on the CSs      |    |
|   |   |   |    |         Login status('CS Login Status'):           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Yes - in blue color: once the CSs      |    |
|   |   |   |    |             logged in the exam session in an exam  |    |
|   |   |   |    |             day                                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   No - in pink color: CSs have not       |    |
|   |   |   |    |             logged in yet in an exam session in an |    |
|   |   |   |    |             exam day                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   A pie chart of an overview on the          |    |
|   |   |   |    |         confirmation status('Overall Submission    |    |
|   |   |   |    |         Situation'):                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Pending to confirm - in gray color:    |    |
|   |   |   |    |             the accuracy of the attendance and     |    |
|   |   |   |    |             collected script data is pending to be |    |
|   |   |   |    |             confirmed by CS                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Confirmed without discrepancy - in     |    |
|   |   |   |    |             green color:                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |             -   the accuracy of the attendance and |    |
|   |   |   |    |                 collected script data was          |    |
|   |   |   |    |                 confirmed by CS without any        |    |
|   |   |   |    |                 discrepancy                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |             -   Missing attendance + missing       |    |
|   |   |   |    |                 script + absent with scripts +     |    |
|   |   |   |    |                 pending special case (i.e.         |    |
|   |   |   |    |                 incomplete SR Forms) = 0           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Confirmed with pending special case -  |    |
|   |   |   |    |             in yellow color:                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |             -   The accuracy of the attendance and |    |
|   |   |   |    |                 collected script data was          |    |
|   |   |   |    |                 confirmed by CS without any        |    |
|   |   |   |    |                 discrepancy but with the           |    |
|   |   |   |    |                 incomplete SR Forms                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |             -   Missing attendance + missing       |    |
|   |   |   |    |                 script + absent with scripts = 0   |    |
|   |   |   |    |                 but pending special case (i.e.     |    |
|   |   |   |    |                 incomplete SR Forms) \> 0          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Confirmed but with attendance and/or   |    |
|   |   |   |    |             script discrepancy - in red color:     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |             -   CS confirmed the accuracy of       |    |
|   |   |   |    |                 number of candidates present and   |    |
|   |   |   |    |                 the number of scripts collected    |    |
|   |   |   |    |                 but with discrepancy               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |             -   Missing attendance + missing       |    |
|   |   |   |    |                 script + absent with scripts \> 0  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   A pie chart showing overall the CSs have   |    |
|   |   |   |    |         been notified by the operator/helpdesk     |    |
|   |   |   |    |         ('Notified CS')                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Yes - in cyan color: the notification  |    |
|   |   |   |    |             has been sent to CSs                   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   No - in brown color: the CSs have not  |    |
|   |   |   |    |             been notified yet                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Mouseover the pie shall display the        |    |
|   |   |   |    |         corresponding count number.                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 3.  The Dashboard page of the officer/manager role |    |
|   |   |   |    |     users shall display the overviews of the exam  |    |
|   |   |   |    |     centres of all the helpdesks/operators are     |    |
|   |   |   |    |     responsible for:                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   A bar chart showing the CSs Login          |    |
|   |   |   |    |         status('CS Login Status by Helpdesk'):     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Yes - in blue color: once the CSs      |    |
|   |   |   |    |             logged in the exam session in an exam  |    |
|   |   |   |    |             day                                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   No - in pink color: CSs have not       |    |
|   |   |   |    |             logged in yet in an exam session in an |    |
|   |   |   |    |             exam day                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   A bar chart showing overall discrepancy    |    |
|   |   |   |    |         situation by helpdesk/operator ('Overall   |    |
|   |   |   |    |         Submission Status by Helpdesk')            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Pending to confirm - in gray color:    |    |
|   |   |   |    |             the accuracy of the attendance and     |    |
|   |   |   |    |             collected script data is pending to be |    |
|   |   |   |    |             confirmed by CS                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Confirmed without discrepancy - in     |    |
|   |   |   |    |             green color:                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |             -   the accuracy of the attendance and |    |
|   |   |   |    |                 collected script data was          |    |
|   |   |   |    |                 confirmed by CS without any        |    |
|   |   |   |    |                 discrepancy                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |             -   Missing attendance + missing       |    |
|   |   |   |    |                 script + absent with scripts +     |    |
|   |   |   |    |                 pending special case (i.e.         |    |
|   |   |   |    |                 incomplete SR Forms) = 0           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Confirmed with pending special case -  |    |
|   |   |   |    |             in yellow color:                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |             -   The accuracy of the attendance and |    |
|   |   |   |    |                 collected script data was          |    |
|   |   |   |    |                 confirmed by CS without any        |    |
|   |   |   |    |                 discrepancy but with the           |    |
|   |   |   |    |                 incomplete SR Forms                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |             -   Missing attendance + missing       |    |
|   |   |   |    |                 script + absent with scripts = 0   |    |
|   |   |   |    |                 but pending special case (i.e.     |    |
|   |   |   |    |                 incomplete SR Forms) \> 0          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Confirmed but with attendance and/or   |    |
|   |   |   |    |             script discrepancy - in red color:     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |             -   CS confirmed the accuracy of       |    |
|   |   |   |    |                 number of candidates present and   |    |
|   |   |   |    |                 the number of scripts collected    |    |
|   |   |   |    |                 but with discrepancy               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |             -   Missing attendance + missing       |    |
|   |   |   |    |                 script + absent with scripts \> 0  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   A bar chart showing the status that the    |    |
|   |   |   |    |         CSs have been notified by the helpdesk     |    |
|   |   |   |    |         ('Notified CS by Helpdesk')                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Yes - in cyan color: the notification  |    |
|   |   |   |    |             has been sent to CSs                   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   No - in brown color: the CSs have not  |    |
|   |   |   |    |             been notified yet                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Mouseover the bar shall display the        |    |
|   |   |   |    |         corresponding count number.                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  For the result tables, users shall be able to  |    |
|   |   |   |    |     select columns displayed by toggling the       |    |
|   |   |   |    |     'Preferences' button.                          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 5.  In order to facilitate the operations of the   |    |
|   |   |   |    |     users, the functions of notifying CSs shall be |    |
|   |   |   |    |     provided in the Dashboard page.                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 6.  Following fields shall be displayed in the     |    |
|   |   |   |    |     result table as the exam data summary          |    |
|   |   |   |    |     according to the selection criteria of the     |    |
|   |   |   |    |     filtering events:                              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Operator - the login name of the           |    |
|   |   |   |    |         helpdesk/operator, applicable to the       |    |
|   |   |   |    |         officer/manager role users                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Centre supervisor Logged in at - Centre    |    |
|   |   |   |    |         supervisor name with EP no. and the post,  |    |
|   |   |   |    |         and the time (hh:mm) of his/her logged in  |    |
|   |   |   |    |         CS Module. E.g. CHAN TIN NAM(10088-076 CS) |    |
|   |   |   |    |         07:24; mouseover the centre supervisor     |    |
|   |   |   |    |         name shall popup the school telephone no.  |    |
|   |   |   |    |         of the centre supervisor.                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Subject code                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Subject name                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Paper group                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Centre code                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Centre type                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   School code; mouseover the school code     |    |
|   |   |   |    |         shall popup the school name and the        |    |
|   |   |   |    |         address                                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Missing attendance - no. of candidates     |    |
|   |   |   |    |         that the attendance record have not been   |    |
|   |   |   |    |         taken yet                                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Missing script - the total no. of missing  |    |
|   |   |   |    |         scripts that should be collected from the  |    |
|   |   |   |    |         allocated candidates and the special case  |    |
|   |   |   |    |         present at the exam centre(except those    |    |
|   |   |   |    |         moved to and at the special room).         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Absent with script - rename of absent but  |    |
|   |   |   |    |         with script collected                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Remark from CS - remarks inputted by CS    |    |
|   |   |   |    |         when confirming the exam data accuracy.    |    |
|   |   |   |    |         \[View\] button shall be displayed if      |    |
|   |   |   |    |         there is a remark and show 'Nil' if CS has |    |
|   |   |   |    |         not input any remarks.                     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Pending SR Form case - no. of incompleted  |    |
|   |   |   |    |         SR cases over no. of total SR cases        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Notification to CS - for confirming exam   |    |
|   |   |   |    |         data accuracy, users shall be able to      |    |
|   |   |   |    |         single/multiple select the records or      |    |
|   |   |   |    |         select the checkbox of 'Select all to      |    |
|   |   |   |    |         notify CS' and click the \[Notify          |    |
|   |   |   |    |         Selected\] button or \[Notify All\]        |    |
|   |   |   |    |         button, the notification(s) shall be sent  |    |
|   |   |   |    |         to the related CSs.                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Action - popup menu for directing to the   |    |
|   |   |   |    |         individual exam situation page, message    |    |
|   |   |   |    |         board and downloading message board        |    |
|   |   |   |    |         history.                                   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 7.  There are 4 types of indicators located at the |    |
|   |   |   |    |     row header to facilitate the users to know the |    |
|   |   |   |    |     exam data confirmation status of the exam      |    |
|   |   |   |    |     centre after the 1st confirmation of the exam  |    |
|   |   |   |    |     data by the CS.                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   Gray color bar - indicates the exam data       |    |
|   |   |   |    |     confirmation status of the exam centre is      |    |
|   |   |   |    |     pending to confirm by CS                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   Green color bar - Confirmed without            |    |
|   |   |   |    |     discrepancy:                                   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   the accuracy of the attendance and         |    |
|   |   |   |    |         collected script data was confirmed by CS  |    |
|   |   |   |    |         without any discrepancy                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Missing attendance + missing script +      |    |
|   |   |   |    |         absent with scripts + pending special case |    |
|   |   |   |    |         (i.e. incomplete SR Forms) = 0             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   Yellow color bar - Confirmed with pending      |    |
|   |   |   |    |     special case:                                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   The accuracy of the attendance and         |    |
|   |   |   |    |         collected script data was confirmed by CS  |    |
|   |   |   |    |         without any discrepancy but with the       |    |
|   |   |   |    |         incomplete SR Forms                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Missing attendance + missing script +      |    |
|   |   |   |    |         absent with scripts = 0 but pending        |    |
|   |   |   |    |         special case (i.e. incomplete SR Forms) \> |    |
|   |   |   |    |         0                                          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   Red color bar - Confirmed but with attendance  |    |
|   |   |   |    |     and/or script discrepancy:                     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   CS confirmed the accuracy of number of     |    |
|   |   |   |    |         candidates present and the number of       |    |
|   |   |   |    |         scripts collected but with discrepancy     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Missing attendance + missing script +      |    |
|   |   |   |    |         absent with scripts \> 0                   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 8.  The 'View Exam Detail' in the 'Actions' column |    |
|   |   |   |    |     shall direct the VCC manager / officer to the  |    |
|   |   |   |    |     pages where he/she can:                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Manager shall view and edit the attendance |    |
|   |   |   |    |         and script records of the candidates and   |    |
|   |   |   |    |         the officer shall view the data only.      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   View the candidate's exam information      |    |
|   |   |   |    |         during the exam, e.g. self check-in time,  |    |
|   |   |   |    |         invigilator's attendance taking time, no.  |    |
|   |   |   |    |         of scripts collected, spare barcode,       |    |
|   |   |   |    |         confirmation status of the special room    |    |
|   |   |   |    |         exam records, toilet request, and SR1 case |    |
|   |   |   |    |         records.                                   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Manager shall view and edit the special    |    |
|   |   |   |    |         case details and the officer shall view    |    |
|   |   |   |    |         the data only.                             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   View the CS/deputy CS/invigilator's        |    |
|   |   |   |    |         check-in/out time and assignment.          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   View the Sessional Report of the exam      |    |
|   |   |   |    |         session after the exam data of the exam    |    |
|   |   |   |    |         centre has been confirmed.                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 9.  For classroom centres, there is an additional  |    |
|   |   |   |    |     item 'Classroom Summary' in the 'Actions'      |    |
|   |   |   |    |     column, users shall be able to view the        |    |
|   |   |   |    |     related figures of each classroom centre and   |    |
|   |   |   |    |     the total number of corresponding candidates   |    |
|   |   |   |    |     (including both the assigned candidates and    |    |
|   |   |   |    |     special cases) who sit the exam in the         |    |
|   |   |   |    |     classroom centres of an exam school shall be   |    |
|   |   |   |    |     shown.                                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | >                                                  |    |
|   |   |   |    | >                                                  |    |
|   |   |   |    | >                                                  |    |
|   |   |   |    | >                                                  |    |
|   |   |   |    | >                                                  |    |
+---+---+---+----+----------------------------------------------------+----+
| V | 9 | 1 | D  | 1.  Users shall be able to view a table with the   | >  |
| C | 9 | 3 | is |     real-time exam information of all / designated |  O |
| C |   | . | pl |     exam centres via a 'Exam Centres' page.        | ut |
|   |   | 3 | ay |                                                    | >  |
|   |   | . | E  | 2.  Users shall be able to sort the tables by the  |  S |
|   |   | 3 | xa |     field labels and select the field labels       | co |
|   |   |   | mi |     through the 'Preference' button.               | pe |
|   |   |   | na |                                                    |    |
|   |   |   | ti | 3.  There are 4 types of indicators located at the |    |
|   |   |   | on |     row header to facilitate the users to know the |    |
|   |   |   | S  |     exam data confirmation status of the exam      |    |
|   |   |   | es |     centre after the 1st confirmation of the exam  |    |
|   |   |   | si |     data by the CS.                                |    |
|   |   |   | on |                                                    |    |
|   |   |   | I  | -   Gray color bar - indicates the exam data       |    |
|   |   |   | nf |     confirmation status of the exam centre is      |    |
|   |   |   | or |     pending to confirm by CS                       |    |
|   |   |   | ma |                                                    |    |
|   |   |   | ti | -   Green color bar - Confirmed without            |    |
|   |   |   | on |     discrepancy:                                   |    |
|   |   |   | (  |                                                    |    |
|   |   |   | Ex |     -   the accuracy of the attendance and         |    |
|   |   |   | am |         collected script data was confirmed by CS  |    |
|   |   |   | Ce |         without any discrepancy                    |    |
|   |   |   | nt |                                                    |    |
|   |   |   | re |     -   Missing attendance + missing script +      |    |
|   |   |   | s) |         absent with scripts + pending special case |    |
|   |   |   |    |         (i.e. incomplete SR Forms) = 0             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   Yellow color bar - Confirmed with pending      |    |
|   |   |   |    |     special case:                                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   The accuracy of the attendance and         |    |
|   |   |   |    |         collected script data was confirmed by CS  |    |
|   |   |   |    |         without any discrepancy but with the       |    |
|   |   |   |    |         incomplete SR Forms                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Missing attendance + missing script +      |    |
|   |   |   |    |         absent with scripts = 0 but pending        |    |
|   |   |   |    |         special case (i.e. incomplete SR Forms) \> |    |
|   |   |   |    |         0                                          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   Red color bar - Confirmed but with attendance  |    |
|   |   |   |    |     and/or script discrepancy:                     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   CS confirmed the accuracy of number of     |    |
|   |   |   |    |         candidates present and the number of       |    |
|   |   |   |    |         scripts collected but with discrepancy     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Missing attendance + missing script +      |    |
|   |   |   |    |         absent with scripts \> 0                   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  The 'View Exam Detail' and 'Classroom Summary' |    |
|   |   |   |    |     (it shall be displayed at the row of the       |    |
|   |   |   |    |     classroom centre) in the 'Action' column       |    |
|   |   |   |    |     provides the same functions stated in the      |    |
|   |   |   |    |     Dashboard.                                     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 5.  The columns displayed in the result tables     |    |
|   |   |   |    |     mainly separated into 2 parts:                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Exam data of the exam centre               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Exam data confirmation                     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 6.  Users shall be able to select the Simple mode  |    |
|   |   |   |    |     or Full mode to display the columns in the     |    |
|   |   |   |    |     'Exam Centres' page by clicking the \[Simple   |    |
|   |   |   |    |     Mode\] or \[Full Mode\] button.                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 7.  Following fields are listed in different mode: |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | > Part 1 - exam data of the exam centre:           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | +-------+--------+----------------------------+    |    |
|   |   |   |    | | Di    | Fields | Description                |    |    |
|   |   |   |    | | splay |        |                            |    |    |
|   |   |   |    | | in    |        |                            |    |    |
|   |   |   |    | | S     |        |                            |    |    |
|   |   |   |    | | imple |        |                            |    |    |
|   |   |   |    | | /Full |        |                            |    |    |
|   |   |   |    | | Mode  |        |                            |    |    |
|   |   |   |    | +=======+========+============================+    |    |
|   |   |   |    | | Both  | Op     | -   the login name of the  |    |    |
|   |   |   |    | |       | erator |     helpdesk/operator      |    |    |
|   |   |   |    | |       |        |                            |    |    |
|   |   |   |    | |       |        | -   applicable to the      |    |    |
|   |   |   |    | |       |        |     officer/manager role   |    |    |
|   |   |   |    | |       |        |     users                  |    |    |
|   |   |   |    | +-------+--------+----------------------------+    |    |
|   |   |   |    | | Both  | Centre | -   Centre supervisor name |    |    |
|   |   |   |    | |       | Supe   |     with EP no. and the    |    |    |
|   |   |   |    | |       | rvisor |     post, and the time of  |    |    |
|   |   |   |    | |       | Logged |     his/her logged in CS   |    |    |
|   |   |   |    | |       | In At  |     Module. E.g. CHAN TIN  |    |    |
|   |   |   |    | |       |        |     NAM(10088-076 CS)      |    |    |
|   |   |   |    | |       |        |     07:24                  |    |    |
|   |   |   |    | |       |        |                            |    |    |
|   |   |   |    | |       |        | -   mouseover the centre   |    |    |
|   |   |   |    | |       |        |     supervisor name shall  |    |    |
|   |   |   |    | |       |        |     popup the school       |    |    |
|   |   |   |    | |       |        |     telephone no. of the   |    |    |
|   |   |   |    | |       |        |     centre supervisor      |    |    |
|   |   |   |    | +-------+--------+----------------------------+    |    |
|   |   |   |    | | Both  | S      | Unique code of the subject |    |    |
|   |   |   |    | |       | ubject | as recorded in the HKDSE   |    |    |
|   |   |   |    | |       | Code   | system                     |    |    |
|   |   |   |    | +-------+--------+----------------------------+    |    |
|   |   |   |    | | Both  | Paper  | Paper code of the subject  |    |    |
|   |   |   |    | |       | Group  |                            |    |    |
|   |   |   |    | +-------+--------+----------------------------+    |    |
|   |   |   |    | | Both  | Centre | Unique code of the exam    |    |    |
|   |   |   |    | |       | Code   | centre as recorded in the  |    |    |
|   |   |   |    | |       |        | HKDSE system               |    |    |
|   |   |   |    | +-------+--------+----------------------------+    |    |
|   |   |   |    | | Both  | Centre | Type of the exam centre as |    |    |
|   |   |   |    | |       | Type   | recorded in the HKDSE      |    |    |
|   |   |   |    | |       |        | system, e.g. HALL, HALL2,  |    |    |
|   |   |   |    | |       |        | SEN CLASSROOM, etc.        |    |    |
|   |   |   |    | +-------+--------+----------------------------+    |    |
|   |   |   |    | | Both  | As     | -   Assigned candidate     |    |    |
|   |   |   |    | |       | signed |                            |    |    |
|   |   |   |    | |       | Cand   | -   the number of          |    |    |
|   |   |   |    | |       |        |     candidates assigned to |    |    |
|   |   |   |    | |       |        |     the exam session       |    |    |
|   |   |   |    | +-------+--------+----------------------------+    |    |
|   |   |   |    | | Both  | P      | the number of assigned     |    |    |
|   |   |   |    | |       | resent | candidates who are present |    |    |
|   |   |   |    | |       | Count  | at the exam session        |    |    |
|   |   |   |    | +-------+--------+----------------------------+    |    |
|   |   |   |    | | Both  | Absent | the number of assigned     |    |    |
|   |   |   |    | |       | Count  | candidates who are absent  |    |    |
|   |   |   |    | |       |        | from the exam session      |    |    |
|   |   |   |    | +-------+--------+----------------------------+    |    |
|   |   |   |    | | Both  | M      | -   the number of assigned |    |    |
|   |   |   |    | |       | issing |     candidates whose       |    |    |
|   |   |   |    | |       | Atte   |     attendance status have |    |    |
|   |   |   |    | |       | ndance |     not been updated as    |    |    |
|   |   |   |    | |       |        |     present or absent yet  |    |    |
|   |   |   |    | +-------+--------+----------------------------+    |    |
|   |   |   |    | | Both  | Wrong  | the number of special case |    |    |
|   |   |   |    | |       | Centre | candidates present at the  |    |    |
|   |   |   |    | |       |        | exam session               |    |    |
|   |   |   |    | +-------+--------+----------------------------+    |    |
|   |   |   |    | | Both  | Absent | -   the total number of    |    |    |
|   |   |   |    | |       | with   |     scripts collected that |    |    |
|   |   |   |    | |       | Script |     the assigned           |    |    |
|   |   |   |    | |       |        |     candidates who are     |    |    |
|   |   |   |    | |       |        |     absent from the exam   |    |    |
|   |   |   |    | |       |        |     session                |    |    |
|   |   |   |    | +-------+--------+----------------------------+    |    |
|   |   |   |    | | Full  | Ex     | the total number of        |    |    |
|   |   |   |    | |       | pected | scripts to be collected    |    |    |
|   |   |   |    | |       | Script | from assigned candidates   |    |    |
|   |   |   |    | |       | Count  | and the wrong centre       |    |    |
|   |   |   |    | |       |        | candidates present at the  |    |    |
|   |   |   |    | |       |        | exam session               |    |    |
|   |   |   |    | +-------+--------+----------------------------+    |    |
|   |   |   |    | | Full  | Script | the total number of        |    |    |
|   |   |   |    | |       | Col    | scripts collected from     |    |    |
|   |   |   |    | |       | lected | assigned candidates and    |    |    |
|   |   |   |    | |       |        | the wrong centre           |    |    |
|   |   |   |    | |       |        | candidates present at the  |    |    |
|   |   |   |    | |       |        | exam session               |    |    |
|   |   |   |    | +-------+--------+----------------------------+    |    |
|   |   |   |    | | Both  | M      | -   the total number of    |    |    |
|   |   |   |    | |       | issing |     missing scripts that   |    |    |
|   |   |   |    | |       | Script |     should be collected    |    |    |
|   |   |   |    | |       |        |     from the assigned      |    |    |
|   |   |   |    | |       |        |     candidates and the     |    |    |
|   |   |   |    | |       |        |     wrong centre candidate |    |    |
|   |   |   |    | |       |        |     present at the exam    |    |    |
|   |   |   |    | |       |        |     session                |    |    |
|   |   |   |    | +-------+--------+----------------------------+    |    |
|   |   |   |    | | Full  | Total  | -   the total number of    |    |    |
|   |   |   |    | | mode  | SR     |     irregularity           |    |    |
|   |   |   |    | |       | Form   |     cases(with SR Form     |    |    |
|   |   |   |    | |       |        |     created) of the        |    |    |
|   |   |   |    | |       |        |     assigned candidates    |    |    |
|   |   |   |    | |       |        |     and the wrong centre   |    |    |
|   |   |   |    | |       |        |     candidate present at   |    |    |
|   |   |   |    | |       |        |     the exam session       |    |    |
|   |   |   |    | +-------+--------+----------------------------+    |    |
|   |   |   |    | | Both  | P      | -   the total number of    |    |    |
|   |   |   |    | |       | ending |     incomplete             |    |    |
|   |   |   |    | |       | SR     |     irregularity cases,    |    |    |
|   |   |   |    | |       | Form   |     i.e. the SR Form       |    |    |
|   |   |   |    | |       |        |     status not completed   |    |    |
|   |   |   |    | |       |        |     yet                    |    |    |
|   |   |   |    | +-------+--------+----------------------------+    |    |
|   |   |   |    | | Both  | Fol    | -   Y/N                    |    |    |
|   |   |   |    | |       | low-up |                            |    |    |
|   |   |   |    | |       |        | -   Y when there is        |    |    |
|   |   |   |    | |       |        |     pending SR Form,       |    |    |
|   |   |   |    | |       |        |     otherwise, N shall be  |    |    |
|   |   |   |    | |       |        |     displayed              |    |    |
|   |   |   |    | +-------+--------+----------------------------+    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | >                                                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   Part 2 - Exam data confirmation                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | +------+-----+--------------------------------+    |    |
|   |   |   |    | | Dis  | Fie | Description                    |    |    |
|   |   |   |    | | play | lds |                                |    |    |
|   |   |   |    | | in   |     |                                |    |    |
|   |   |   |    | | Sim  |     |                                |    |    |
|   |   |   |    | | ple/ |     |                                |    |    |
|   |   |   |    | | Full |     |                                |    |    |
|   |   |   |    | | Mode |     |                                |    |    |
|   |   |   |    | +======+=====+================================+    |    |
|   |   |   |    | | Both | Rem | -   remarks inputted by CS     |    |    |
|   |   |   |    | |      | ark |     when confirming the exam   |    |    |
|   |   |   |    | |      | f   |     data accuracy              |    |    |
|   |   |   |    | |      | rom |                                |    |    |
|   |   |   |    | |      | CS  | -   \[View\] button shall be   |    |    |
|   |   |   |    | |      |     |     displayed if there is a    |    |    |
|   |   |   |    | |      |     |     remark and show 'Nil' if   |    |    |
|   |   |   |    | |      |     |     remarks are not inputted   |    |    |
|   |   |   |    | +------+-----+--------------------------------+    |    |
|   |   |   |    | | Both | Not | -   for confirming exam data   |    |    |
|   |   |   |    | |      | ifi |     accuracy, users shall be   |    |    |
|   |   |   |    | |      | cat |     able to single/multiple    |    |    |
|   |   |   |    | |      | ion |     select the records or      |    |    |
|   |   |   |    | |      | to  |     select the checkbox of     |    |    |
|   |   |   |    | |      | CS  |     'Select all to notify CS'  |    |    |
|   |   |   |    | |      |     |     and click the \[Notify     |    |    |
|   |   |   |    | |      |     |     Selected\] button or       |    |    |
|   |   |   |    | |      |     |     \[Notify All\] button, the |    |    |
|   |   |   |    | |      |     |     notification(s) shall be   |    |    |
|   |   |   |    | |      |     |     sent to the related CSs    |    |    |
|   |   |   |    | +------+-----+--------------------------------+    |    |
|   |   |   |    | | Both | C   | -   for officer/manager role   |    |    |
|   |   |   |    | |      | onf |     users to notify and        |    |    |
|   |   |   |    | |      | irm |     confirm the exam data      |    |    |
|   |   |   |    | |      | to  |     accuracy for ESU, users    |    |    |
|   |   |   |    | |      | ESU |     shall be able to           |    |    |
|   |   |   |    | |      |     |     single/multiple select the |    |    |
|   |   |   |    | |      |     |     records or select the      |    |    |
|   |   |   |    | |      |     |     checkbox of 'Select All    |    |    |
|   |   |   |    | |      |     |     Confirm' and click the     |    |    |
|   |   |   |    | |      |     |     \[Confirm Selected\]       |    |    |
|   |   |   |    | |      |     |     button or \[Confirm All\]  |    |    |
|   |   |   |    | |      |     |     button                     |    |    |
|   |   |   |    | +------+-----+--------------------------------+    |    |
|   |   |   |    | | Both | Con | the account of the             |    |    |
|   |   |   |    | |      | fir | officer/manager role user who  |    |    |
|   |   |   |    | |      | med | confirms the exam data         |    |    |
|   |   |   |    | |      | by  | accuracy for ESU               |    |    |
|   |   |   |    | +------+-----+--------------------------------+    |    |
|   |   |   |    | | Both | Con | the time when the              |    |    |
|   |   |   |    | |      | fir | officer/manager role user who  |    |    |
|   |   |   |    | |      | med | confirms the exam data         |    |    |
|   |   |   |    | |      | T   | accuracy for ESU               |    |    |
|   |   |   |    | |      | ime |                                |    |    |
|   |   |   |    | +------+-----+--------------------------------+    |    |
|   |   |   |    | | Both | Act | A popup menu for directing to  |    |    |
|   |   |   |    | |      | ion | the individual exam situation  |    |    |
|   |   |   |    | |      |     | page, classroom summary        |    |    |
|   |   |   |    | |      |     | (applicable to the row of      |    |    |
|   |   |   |    | |      |     | classroom centre), message     |    |    |
|   |   |   |    | |      |     | board and downloading message  |    |    |
|   |   |   |    | |      |     | board history                  |    |    |
|   |   |   |    | +------+-----+--------------------------------+    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | >                                                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   After CS(s) have confirmed the exam data of    |    |
|   |   |   |    |     the exam centre(s) to VCC, manager / officer   |    |
|   |   |   |    |     role users can download the Sessional Reports  |    |
|   |   |   |    |     of the exam centre(s) to the Excel file by     |    |
|   |   |   |    |     clicking the \[Sessional Report\] button.      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   After CS(s) have confirmed the exam data of    |    |
|   |   |   |    |     the exam centre(s) to VCC, users can single    |    |
|   |   |   |    |     select or multiple select the checkbox(es) of  |    |
|   |   |   |    |     the 'Notification to CS' and click the         |    |
|   |   |   |    |     \[Notify Selected\] button to send             |    |
|   |   |   |    |     notification to the CS(s) of the selected exam |    |
|   |   |   |    |     centre(s).                                     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   Users shall be able to select all the exam     |    |
|   |   |   |    |     centres of the filtering result by ticking the |    |
|   |   |   |    |     checkbox of the 'Select All Notification' and  |    |
|   |   |   |    |     clicking the \[Notify Selected\] button for    |    |
|   |   |   |    |     notification to the CSs of all the exam        |    |
|   |   |   |    |     centres across all the pages of the filtering  |    |
|   |   |   |    |     result.                                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   A notification shall be sent to the message    |    |
|   |   |   |    |     board of the CS.                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   Users shall receive an alert if the CS changes |    |
|   |   |   |    |     the sessional report / attendance / script     |    |
|   |   |   |    |     data.                                          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   Users shall be able to single select or        |    |
|   |   |   |    |     multiple select the checkbox(es) of the        |    |
|   |   |   |    |     'Confirm to ESU' and click the \[Confirm       |    |
|   |   |   |    |     Selected\] button to confirm the exam data of  |    |
|   |   |   |    |     the selected exam centre(s) to ESU.            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   Users shall be able to select all the exam     |    |
|   |   |   |    |     centres of the filtering result by ticking the |    |
|   |   |   |    |     checkbox of 'Select All Confirm' button and    |    |
|   |   |   |    |     click the \[Confirm Selected\] to confirm the  |    |
|   |   |   |    |     exam data of all exam centres across all the   |    |
|   |   |   |    |     pages of the filtering result to ESU.          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   Once the VCC manager / officer has confirmed   |    |
|   |   |   |    |     the exam data to ESU, his/her username and the |    |
|   |   |   |    |     confirmation time shall be displayed.          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   Confirmation to ESU is iterative, the username |    |
|   |   |   |    |     and the confirmation time shall be kept        |    |
|   |   |   |    |     updating.                                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   CS shall be able to re-confirm the exam data   |    |
|   |   |   |    |     to VCC if there is any change in the exam      |    |
|   |   |   |    |     data. If the VCC manager / officer has         |    |
|   |   |   |    |     confirmed the exam data to ESU after 1st exam  |    |
|   |   |   |    |     data confirmation by CS, the VCC manager /     |    |
|   |   |   |    |     officer shall receive an alert and be reminded |    |
|   |   |   |    |     to confirm the exam data to ESU again.         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | >                                                  |    |
|   |   |   |    | >                                                  |    |
|   |   |   |    | >                                                  |    |
+---+---+---+----+----------------------------------------------------+----+
| V | 1 | 1 | S  | 1.  After the CS(s) confirms the exam data of the  | >  |
| C | 0 | 3 | es |     exam centre(s), the manager/officer role users |  O |
| C | 5 | . | si |     shall be able to download the Sessional        | ut |
|   |   | 3 | on |     Report(s) in CSV/Excel format by clicking the  | >  |
|   |   | . | al |     \[Sessional Report\] button from the menu bar  |  S |
|   |   | 4 | Re |     of the 'Exam Centres' page.                    | co |
|   |   |   | po |                                                    | pe |
|   |   |   | rt | 2.  The filename starts with                       |    |
|   |   |   |    |     'sessional-report-summary' followed by         |    |
|   |   |   |    |     yyyymmdd and 6 digit serial number.            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | > The export file shall be provided are listed as  |    |
|   |   |   |    | > below:                                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | +-----+----------------------------------------+   |    |
|   |   |   |    | | Rep | Description                            |   |    |
|   |   |   |    | | ort |                                        |   |    |
|   |   |   |    | +=====+========================================+   |    |
|   |   |   |    | | Hal | Export file content:                   |   |    |
|   |   |   |    | | l-D |                                        |   |    |
|   |   |   |    | | eta | centre code, school code, school name, |   |    |
|   |   |   |    | | ils | subject code, subject name, paper      |   |    |
|   |   |   |    | |     | code, exam date, location, actual      |   |    |
|   |   |   |    | |     | starting time, actual finishing time,  |   |    |
|   |   |   |    | |     | number of packets, number of answer    |   |    |
|   |   |   |    | |     | scripts collected, listening test mode |   |    |
|   |   |   |    | |     | (paper 3), reception of the listening  |   |    |
|   |   |   |    | |     | component (paper 3), remark (paper 3), |   |    |
|   |   |   |    | |     | report verified by invigilator 1, ep   |   |    |
|   |   |   |    | |     | no./application no./account no. of     |   |    |
|   |   |   |    | |     | invigilator 1, name of invigilator 1,  |   |    |
|   |   |   |    | |     | school name of invigilator 1,          |   |    |
|   |   |   |    | |     | invigilator 1's verification time,     |   |    |
|   |   |   |    | |     | report verified by invigilator 2, ep   |   |    |
|   |   |   |    | |     | no./application no./account no. of     |   |    |
|   |   |   |    | |     | invigilator 2, name of invigilator 2,  |   |    |
|   |   |   |    | |     | school name of invigilator 2,          |   |    |
|   |   |   |    | |     | invigilator 2's verification time, CS  |   |    |
|   |   |   |    | |     | name, ep no. of CS, report submission  |   |    |
|   |   |   |    | |     | time to HKEAA, with IRR candidate      |   |    |
|   |   |   |    | |     | record (Y/N), with IRR invigilator     |   |    |
|   |   |   |    | |     | record (Y/N)                           |   |    |
|   |   |   |    | +-----+----------------------------------------+   |    |
|   |   |   |    | | Cl  | Export file content:                   |   |    |
|   |   |   |    | | ass |                                        |   |    |
|   |   |   |    | | roo | centre code, school code, school name, |   |    |
|   |   |   |    | | m-D | subject code, subject name, paper      |   |    |
|   |   |   |    | | eta | code, exam date, location, actual      |   |    |
|   |   |   |    | | ils | starting time, actual finishing time,  |   |    |
|   |   |   |    | |     | number of packets, number of answer    |   |    |
|   |   |   |    | |     | scripts collected, listening test mode |   |    |
|   |   |   |    | |     | (paper 3), reception of the listening  |   |    |
|   |   |   |    | |     | component (paper 3), remark (paper 3), |   |    |
|   |   |   |    | |     | report submitted by CRI, ep            |   |    |
|   |   |   |    | |     | no./application no./account no. of     |   |    |
|   |   |   |    | |     | CRI, name of CRI, school name of CRI,  |   |    |
|   |   |   |    | |     | report submission time to classroom    |   |    |
|   |   |   |    | |     | CS, CS name, ep no. of CS, report      |   |    |
|   |   |   |    | |     | submission time to HKEAA, with IRR     |   |    |
|   |   |   |    | |     | candidate record (Y/N), with IRR       |   |    |
|   |   |   |    | |     | invigilator record (Y/N)               |   |    |
|   |   |   |    | +-----+----------------------------------------+   |    |
|   |   |   |    | | C   | Export file content:                   |   |    |
|   |   |   |    | | and |                                        |   |    |
|   |   |   |    | | ida | centre code, school code, subject      |   |    |
|   |   |   |    | | tes | code, paper code, exam date, candidate |   |    |
|   |   |   |    | | w   | no. and name involved IRR              |   |    |
|   |   |   |    | | ith |                                        |   |    |
|   |   |   |    | | Ir  |                                        |   |    |
|   |   |   |    | | reg |                                        |   |    |
|   |   |   |    | | ula |                                        |   |    |
|   |   |   |    | | rit |                                        |   |    |
|   |   |   |    | | ies |                                        |   |    |
|   |   |   |    | | (I  |                                        |   |    |
|   |   |   |    | | RR) |                                        |   |    |
|   |   |   |    | +-----+----------------------------------------+   |    |
|   |   |   |    | | Inv | Export file content:                   |   |    |
|   |   |   |    | | igi |                                        |   |    |
|   |   |   |    | | lat | centre code, school code, subject      |   |    |
|   |   |   |    | | ors | code, paper code, exam date, ep        |   |    |
|   |   |   |    | | w   | no./application no./account no. and    |   |    |
|   |   |   |    | | ith | name of invigilator involved IRR       |   |    |
|   |   |   |    | | Ir  |                                        |   |    |
|   |   |   |    | | reg |                                        |   |    |
|   |   |   |    | | ula |                                        |   |    |
|   |   |   |    | | rit |                                        |   |    |
|   |   |   |    | | ies |                                        |   |    |
|   |   |   |    | | (I  |                                        |   |    |
|   |   |   |    | | RR) |                                        |   |    |
|   |   |   |    | +-----+----------------------------------------+   |    |
|   |   |   |    | | Inv | Export file content:                   |   |    |
|   |   |   |    | | igi |                                        |   |    |
|   |   |   |    | | lat | centre code, school code, subject      |   |    |
|   |   |   |    | | ors | code, paper code, exam date, ep        |   |    |
|   |   |   |    | |     | no./application no./account no. and    |   |    |
|   |   |   |    | |     | name of invigilators, invigilator      |   |    |
|   |   |   |    | |     | type(TECH, SRI, DCS, AD HOC, INV, CS), |   |    |
|   |   |   |    | |     | last check-in time, last check-out     |   |    |
|   |   |   |    | |     | time                                   |   |    |
|   |   |   |    | +-----+----------------------------------------+   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | >                                                  |    |
|   |   |   |    | >                                                  |    |
|   |   |   |    | >                                                  |    |
+---+---+---+----+----------------------------------------------------+----+
| V | 1 | 1 | D  | 1.  Users shall be able to view the detailed       | >  |
| C | 0 | 3 | is |     examination, candidate, CS and invigilator     |  O |
| C | 6 | . | pl |     information of each of the (assigned) exam     | ut |
|   |   | 3 | ay |     centres by clicking the 'View Exam Detail'     | >  |
|   |   | . | In |     hyperlink under the 'Action' button in the     |  S |
|   |   | 5 | di |     'Dashboard' or 'Exam Centre' page.             | co |
|   |   |   | vi |                                                    | pe |
|   |   |   | du | 2.  Through the 'View Exam Detail' link, users     |    |
|   |   |   | al |     shall be able to view the:                     |    |
|   |   |   | Ex |                                                    |    |
|   |   |   | am | -   Exam Information                               |    |
|   |   |   | Ce |                                                    |    |
|   |   |   | nt |     -   Exam Type and Year, e.g. DSE 2022          |    |
|   |   |   | re |                                                    |    |
|   |   |   | S  |     -   Exam Date                                  |    |
|   |   |   | it |                                                    |    |
|   |   |   | ua |     -   Centre Code and Name of Centre School      |    |
|   |   |   | ti |                                                    |    |
|   |   |   | on |     -   Centre Type                                |    |
|   |   |   | (  |                                                    |    |
|   |   |   | Vi |     -   Subject Code and Subject Name              |    |
|   |   |   | ew |                                                    |    |
|   |   |   | Ex |     -   Paper Group                                |    |
|   |   |   | am |                                                    |    |
|   |   |   | D  | -   CS and Invigilator Assignment                  |    |
|   |   |   | et |                                                    |    |
|   |   |   | ai |     -   For CS:                                    |    |
|   |   |   | l) |                                                    |    |
|   |   |   |    |         -   display CS's name, EP number, school   |    |
|   |   |   |    |             name and telephone number of the       |    |
|   |   |   |    |             school as recorded in the HKDSE        |    |
|   |   |   |    |             system.                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   For Invigilator:                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   display allocated invigilator's name   |    |
|   |   |   |    |             and EP number / Application number as  |    |
|   |   |   |    |             recorded in the HKDSE system.          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   For the absent invigilator, '(Absent)'     |    |
|   |   |   |    |         shall be displayed after the information   |    |
|   |   |   |    |         of the invigilator.                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   Attendance and Script Records - a list of      |    |
|   |   |   |    |     allocated candidates of the exam centre shall  |    |
|   |   |   |    |     be displayed.                                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Candidate number                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Candidate name                             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Case number                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Seat number                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Subject code                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Paper group                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Zone assigned in the exam centre           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Present status                             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   '- -' means attendance record not yet  |    |
|   |   |   |    |             taken                                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Present                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   ABS - absent                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Number of collected script(s) / number of  |    |
|   |   |   |    |         scripts to be collected from each          |    |
|   |   |   |    |         candidate                                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Discrepancy related to the candidate case  |    |
|   |   |   |    |         (missing attendance, missing script,       |    |
|   |   |   |    |         absent with script collected or missing    |    |
|   |   |   |    |         attendance with script collected, if any)  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   A 'magnifying' button for display          |    |
|   |   |   |    |         information of candidate during the exam   |    |
|   |   |   |    |         (self check-in time, invigilator's         |    |
|   |   |   |    |         attendance taking time, number of scripts  |    |
|   |   |   |    |         collected, spare barcode, toilet request,  |    |
|   |   |   |    |         and SR1 case records)                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   An 'pencil' button for editing the         |    |
|   |   |   |    |         attendance and Script records (applicable  |    |
|   |   |   |    |         to Manager role only)                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   Special Case                                   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Candidate number                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Identification document number or          |    |
|   |   |   |    |         Candidate name                             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Case number                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Zone assigned in the exam centre, similar  |    |
|   |   |   |    |         to the Centre Supervisor, users shall be   |    |
|   |   |   |    |         able to create new zone by clicking the    |    |
|   |   |   |    |         '+' icon                                   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Spare barcode assigned to each candidate   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Number of collected script(s) / number of  |    |
|   |   |   |    |         scripts to be collected from each          |    |
|   |   |   |    |         candidate                                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Discrepancy related to the candidates      |    |
|   |   |   |    |         (e.g. Missing script)                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   The 'Add Special Case' button for creating |    |
|   |   |   |    |         special case, users shall be able to add   |    |
|   |   |   |    |         special case by candidate number,          |    |
|   |   |   |    |         candidate's identification number and      |    |
|   |   |   |    |         candidate name.                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Users shall be able to create a new zone   |    |
|   |   |   |    |         in the existing exam centre, assign an     |    |
|   |   |   |    |         invigilator of that exam centre to it.     |    |
|   |   |   |    |         Then assign the worng centre candidate to  |    |
|   |   |   |    |         the new zone.                              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   An 'pencil' button for editing the         |    |
|   |   |   |    |         collected script record of each candidate  |    |
|   |   |   |    |         (applicable to Manager role only)          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   An 'eraser' button for removing the        |    |
|   |   |   |    |         special case record (applicable to Manager |    |
|   |   |   |    |         role only)                                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   CS / Invigilator Assignment and Check-in       |    |
|   |   |   |    |     Status                                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   EP number / Application number / ad hoc    |    |
|   |   |   |    |         invigilator number of CS / invigilator     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   English name                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Post (CS / DCS / Invigilator / AD HOC)     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Assignment (exam centre code of CS, DCS    |    |
|   |   |   |    |         and classroom invigilator / seat number    |    |
|   |   |   |    |         range of hall invigilator)                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Check-in date and time                     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Check-out date and time                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   Discrepancy Report                             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Candidate type                             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Allocated                              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Special case                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Candidate number / candidate's             |    |
|   |   |   |    |         identification number                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Candidate name                             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Case number                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Seat number                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Subject code                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Paper group                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Zone assigned in the exam centre           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Spare barcode number                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Remarks - discrepancy type:                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Missing attendance record(s)           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Missing attendance with script(s)      |    |
|   |   |   |    |             collected                              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Missing script record(s)               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Absent with script(s) collected        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   Sessional reports of the selected exam session |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 3.  Users shall be able to sort the tables (2.3    |    |
|   |   |   |    |     and 2.4 mentioned above) by the field labels   |    |
|   |   |   |    |     and select the field labels through the        |    |
|   |   |   |    |     'Preference' button.                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  Users shall be able to filter the list of      |    |
|   |   |   |    |     candidates displayed by the attendance and     |    |
|   |   |   |    |     script status (2.3 mentioned above).           |    |
+---+---+---+----+----------------------------------------------------+----+
| V | 1 | 1 | Sc | -   By filtering the Centre Type of an exam        | >  |
| C | 1 | 3 | ho |     school, VCC manager shall be able to reassign  |  O |
| C | 5 | . | ol |     the operator to be responsible for the exam    | ut |
|   |   | 3 | As |     centres.                                       | >  |
|   |   | . | si |                                                    |  S |
|   |   | 6 | gn |                                                    | co |
|   |   |   | me |                                                    | pe |
|   |   |   | nt |                                                    |    |
+---+---+---+----+----------------------------------------------------+----+
| E | 1 | 1 | L  | 1.  Users shall be able to enter their username    | >  |
| S | 1 | 3 | og |     and password to identify their role, and the   |  O |
| B | 5 | . | in |     access to specific functions and data are set  | ut |
| ( |   | 4 |    |     by the IT Admin.                               | >  |
| S |   | . |    |                                                    |  S |
| E |   | 1 |    | 2.  Function access is limited to the SEN system   | co |
| A |   |   |    |     only.                                          | pe |
| D |   |   |    |                                                    |    |
| ) |   |   |    |                                                    |    |
+---+---+---+----+----------------------------------------------------+----+
| E | 1 | 1 | At | 1.  Searching fields include exam date, exam start | >  |
| S | 1 | 3 | te |     and end time, subject code, paper, school      |  O |
| B | 6 | . | nd |     code, school name, centre code and centre      | ut |
| ( |   | 4 | an |     type.                                          | >  |
| S |   | . | ce |                                                    |  S |
| E |   | 2 | Re | 2.  Related exam centre(s) of the filtering result | co |
| A |   |   | co |     shall be listed according to the user's        | pe |
| D |   |   | rd |     selection.                                     |    |
| ) |   |   |    |                                                    |    |
|   |   |   |    | 3.  By clicking the 'right arrow' of the exam      |    |
|   |   |   |    |     centre, each exam session of the corresponding |    |
|   |   |   |    |     exam centre shall be displayed at the right    |    |
|   |   |   |    |     side.                                          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  By clicking the 'right arrow' of the exam      |    |
|   |   |   |    |     session, the attendance records related to     |    |
|   |   |   |    |     allocated candidates and special cases shall   |    |
|   |   |   |    |     be displayed. Users shall be able to select    |    |
|   |   |   |    |     among two types of cases by clicking the       |    |
|   |   |   |    |     corresponding tabs.                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 5.  Searching fields shall include attendance      |    |
|   |   |   |    |     status(e.g. '- -' attendance record not yet    |    |
|   |   |   |    |     taken, present and absent), location (centre   |    |
|   |   |   |    |     type, such as HALL, SEN CLASSROOM), answer     |    |
|   |   |   |    |     script collection status, and keywords such as |    |
|   |   |   |    |     candidate no., candidate name and spare        |    |
|   |   |   |    |     barcode no.                                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 6.  Users shall be able to sort the table by the   |    |
|   |   |   |    |     field labels.                                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 7.  Users shall be able to select columns          |    |
|   |   |   |    |     displayed by toggling the 'Preferences'        |    |
|   |   |   |    |     button.                                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 8.  Allocated Candidates                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   The exam data of allocated candidates      |    |
|   |   |   |    |         shall be displayed in a table, such as:    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   School name                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Subject name                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Subject code                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Paper group                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Centre code                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Centre type (HALL, SEN CLASSROOM)      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Mode (applicable to the listening      |    |
|   |   |   |    |             paper)                                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Zone                                   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Candidate number                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Candidate name                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Seat number                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Case number                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Attendance status ('- -' - attendance  |    |
|   |   |   |    |             record not yet taken, present, absent) |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Answer script collection status        |    |
|   |   |   |    |             (answer script collected / answer      |    |
|   |   |   |    |             script to be collected)                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Location (applicable to the normal     |    |
|   |   |   |    |             exam centre )                          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Self check-in time                     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Invigilator's taking attendance time   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Spare barcode number                   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 9.  Special Cases                                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   The special cases of the exam centre shall |    |
|   |   |   |    |         be displayed with the information of the:  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   School name                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Subject name                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Subject code                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Paper group                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Centre code                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Centre type                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Mode (applicable to the listening      |    |
|   |   |   |    |             paper)                                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Candidate number                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Candidate name                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Candidate's identification number      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Zone                                   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Spare barcode number                   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Case number                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   CS creates special case time           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Answer script collection status        |    |
|   |   |   |    |             (answer script collected / answer      |    |
|   |   |   |    |             script to be collected)                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 10. The exam data shall be downloaded as CSV by    |    |
|   |   |   |    |     single/multiple selecting the records or       |    |
|   |   |   |    |     select the check box next to the 'Export'      |    |
|   |   |   |    |     button to select all records in the result     |    |
|   |   |   |    |     table of all pages, and then click the         |    |
|   |   |   |    |     'Export' button.                               |    |
+---+---+---+----+----------------------------------------------------+----+
| E | 1 | 1 | D  | 1.  4 situations shall be covered in the           | >  |
| S | 1 | 3 | is |     discrepancy report:                            |  O |
| B | 9 | . | cr |                                                    | ut |
| ( |   | 4 | ep |     -   Missing attendance record(s)               | >  |
| S |   | . | an |                                                    |  S |
| E |   | 3 | cy |     -   Missing attendance but with script         | co |
| A |   |   | Re |         collected                                  | pe |
| D |   |   | po |                                                    |    |
| ) |   |   | rt |     -   Missing script records                     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Absent but with script(s) collected        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 2.  Discrepancy records related to allocated       |    |
|   |   |   |    |     candidates and special cases shall be          |    |
|   |   |   |    |     displayed. Users shall be able to select among |    |
|   |   |   |    |     two types of cases by clicking the             |    |
|   |   |   |    |     corresponding tabs.                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 3.  Records with discrepancy shall be displayed:   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Candidate number                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Candidate name                             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Subject name                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Subject code, paper group                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   School name                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   School code                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Centre code                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Centre type                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Zone                                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Mode (applicable to the listening paper)   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Spare barcode number                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Seat number                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Case number                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Attendance status (present, absent, '- -'  |    |
|   |   |   |    |         means attendance record not yet taken)     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Answer script collection status (answer    |    |
|   |   |   |    |         script collected / answer script to be     |    |
|   |   |   |    |         collected)                                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Remarks (4 types of discrepancy situation  |    |
|   |   |   |    |         listed above)                              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  The information shall be downloaded as CSV by  |    |
|   |   |   |    |     single/multiple selecting the records or       |    |
|   |   |   |    |     select the check box next to the 'Export'      |    |
|   |   |   |    |     button to select all records in the result     |    |
|   |   |   |    |     table of all pages, and then click the         |    |
|   |   |   |    |     'Export' button.                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 5.  Information can be viewed by filtering the     |    |
|   |   |   |    |     exam date, exam start and end time, subject    |    |
|   |   |   |    |     code, paper group, school code, school name,   |    |
|   |   |   |    |     centre code, centre type, and candidate        |    |
|   |   |   |    |     number..                                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 6.  Information of the tables shall be sorted by   |    |
|   |   |   |    |     different columns.                             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | <!-- -->                                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 7.  Users shall be able to select columns          |    |
|   |   |   |    |     displayed by toggling the 'Preferences'        |    |
|   |   |   |    |     button.                                        |    |
+---+---+---+----+----------------------------------------------------+----+
| E | 1 | 1 | E  | 1.  Users shall be able to view the actions of     | >  |
| S | 2 | 3 | ve |     Candidate App, Invigilator App, CS Module and  |  O |
| B | 0 | . | nt |     VCC Module.                                    | ut |
| ( |   | 4 | L  |                                                    | >  |
| S |   | . | og | 2.  The events logged shall be displayed by        |  S |
| E |   | 4 |    |     filtering the exam date, exam time period,     | co |
| A |   |   |    |     subject code, paper, school code, school name, | pe |
| D |   |   |    |     centre code, centre type, CS/invigilator no.   |    |
| ) |   |   |    |     and candidate number.                          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 3.  The Information Result table should include:   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Event date and time (in dddd-mm-yy         |    |
|   |   |   |    |         hh:mn:ss format)                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Centre code                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   School code                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Candidate number / EP no. of CS or         |    |
|   |   |   |    |         invigilator                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Actor type (candidate, CS, DCS, VCC)       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Event                                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Location (HALL, SEN CLASSROOM)             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  Users shall be able to select columns          |    |
|   |   |   |    |     displayed by toggling the 'Preferences'        |    |
|   |   |   |    |     button.                                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 5.  Records of event log shall be downloaded as    |    |
|   |   |   |    |     CSV. The existing list of event / access /     |    |
|   |   |   |    |     activity logs is pending enhancement and       |    |
|   |   |   |    |     further update by taking into account the      |    |
|   |   |   |    |     possible actions related to SEN Module.        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 6.  The list of event logs covered in PESS2 are    |    |
|   |   |   |    |     provided below, (it shall be kept on update    |    |
|   |   |   |    |     during implementation in phase 3 if needed):   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | *  | **Event** | **Sample**                  |   |    |
|   |   |   |    | | *  |           |                             |   |    |
|   |   |   |    | | ** |           |                             |   |    |
|   |   |   |    | +====+===========+=============================+   |    |
|   |   |   |    | | *  |           |                             |   |    |
|   |   |   |    | | *V |           |                             |   |    |
|   |   |   |    | | CC |           |                             |   |    |
|   |   |   |    | | ** |           |                             |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 1  | Update    | VCC Manager nmanager        |   |    |
|   |   |   |    | |    | school    | assigns school 10001 centre |   |    |
|   |   |   |    | |    | a         | D1000 with subject A080C    |   |    |
|   |   |   |    | |    | ssignment | paper 2 to VCC Operator     |   |    |
|   |   |   |    | |    |           | B1400-help03.               |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 2  | Delete    | VCC Manager nmanager        |   |    |
|   |   |   |    | |    | school    | deletes 3 school            |   |    |
|   |   |   |    | |    | a         | assignments by uploading    |   |    |
|   |   |   |    | |    | ssignment | excel.                      |   |    |
|   |   |   |    | |    | by Excel  |                             |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 3  | Update    | VCC Manager nmanager        |   |    |
|   |   |   |    | |    | school    | updates 9 school            |   |    |
|   |   |   |    | |    | a         | assignments by uploading    |   |    |
|   |   |   |    | |    | ssignment | excel.                      |   |    |
|   |   |   |    | |    | by Excel  |                             |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 4  | Modify    | VCC Manager nmanager        |   |    |
|   |   |   |    | |    | assigned  | modifies the collected      |   |    |
|   |   |   |    | |    | candidate | script count of assigned    |   |    |
|   |   |   |    | |    | script    | candidate 929393040 into 1  |   |    |
|   |   |   |    | |    |           | at exam school 10066 centre |   |    |
|   |   |   |    | |    |           | B1400 with subject A010C    |   |    |
|   |   |   |    | |    |           | paper 3.                    |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 5  | Modify    | VCC Manager nmanager        |   |    |
|   |   |   |    | |    | assigned  | modifies attendance status  |   |    |
|   |   |   |    | |    | candidate | of assigned candidate       |   |    |
|   |   |   |    | |    | a         | 924224030 into present at   |   |    |
|   |   |   |    | |    | ttendance | exam school 10066 centre    |   |    |
|   |   |   |    | |    |           | B1400 with subject A010C    |   |    |
|   |   |   |    | |    |           | paper 3.                    |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 6  | Log out   | VCC User nmanager logs out. |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 7  | Send      | VCC User nmanager sends     |   |    |
|   |   |   |    | |    | dismissal | dismissal message to exam   |   |    |
|   |   |   |    | |    | message   | school 10058 centre D1350   |   |    |
|   |   |   |    | |    |           | with subject A010C paper 2. |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 8  | Create    | VCC Manager nmanager        |   |    |
|   |   |   |    | |    | special   | creates special case        |   |    |
|   |   |   |    | |    | case      | 225398945 at exam school    |   |    |
|   |   |   |    | |    |           | 10058 centre D1350 with     |   |    |
|   |   |   |    | |    |           | subject A010C paper 3.      |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 9  | Update    | VCC Manager nmanager        |   |    |
|   |   |   |    | |    | special   | updates special case        |   |    |
|   |   |   |    | |    | case      | my-test-nov-6 script count  |   |    |
|   |   |   |    | |    |           | from 0 into 1 at exam       |   |    |
|   |   |   |    | |    |           | school 30740 centre S1750   |   |    |
|   |   |   |    | |    |           | with subject A010C paper 2. |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 10 | Delete    | VCC Manager nmanager        |   |    |
|   |   |   |    | |    | special   | deletes special case Tai    |   |    |
|   |   |   |    | |    | case      | Chan Man at exam school     |   |    |
|   |   |   |    | |    |           | 10058 centre D1350 with     |   |    |
|   |   |   |    | |    |           | subject A010C paper 3.      |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 11 | Add       | VCC Manager nmanager adds   |   |    |
|   |   |   |    | |    | helpdesk  | helpdesk user mc-new-opera  |   |    |
|   |   |   |    | |    | user      | as Normal Officer & Normal  |   |    |
|   |   |   |    | |    |           | Operator.                   |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 12 | Update    | VCC Manager nmanager        |   |    |
|   |   |   |    | |    | helpdesk  | updates helpdesk user       |   |    |
|   |   |   |    | |    | user      | mc-new-opera Normal Officer |   |    |
|   |   |   |    | |    |           | role from false into true,  |   |    |
|   |   |   |    | |    |           | Normal Operator role from   |   |    |
|   |   |   |    | |    |           | true into false, English    |   |    |
|   |   |   |    | |    |           | name from mc-operator into  |   |    |
|   |   |   |    | |    |           | mc-officer, Chinese name    |   |    |
|   |   |   |    | |    |           | from mv-operator into       |   |    |
|   |   |   |    | |    |           | mc-officer.                 |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 13 | Update    | VCC Manager nmanager        |   |    |
|   |   |   |    | |    | manager   | updates information of VCC  |   |    |
|   |   |   |    | |    |           | Manager nmanager English    |   |    |
|   |   |   |    | |    |           | name from normal-manager    |   |    |
|   |   |   |    | |    |           | into nmanager2022, Chinese  |   |    |
|   |   |   |    | |    |           | name from normal-manager    |   |    |
|   |   |   |    | |    |           | into nmanager2022.          |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 14 | Delete    | VCC Manager nmanager        |   |    |
|   |   |   |    | |    | helpdesk  | deletes helpdesk user       |   |    |
|   |   |   |    | |    | user      | mc-new-opera.               |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 15 | Confirm   | VCC User nmanager confirms  |   |    |
|   |   |   |    | |    | to ESU    | exam school 10058 centre    |   |    |
|   |   |   |    | |    |           | D1350 with subject A010C    |   |    |
|   |   |   |    | |    |           | paper 2 to ESU.             |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 16 | Download  | VCC User nmanager downloads |   |    |
|   |   |   |    | |    | exam      | excel of 30 exam sessions.  |   |    |
|   |   |   |    | |    | session   |                             |   |    |
|   |   |   |    | |    | excel     |                             |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 17 | Download  | VCC Manager nmanager        |   |    |
|   |   |   |    | |    | school    | downloads excel of 9635     |   |    |
|   |   |   |    | |    | a         | school assignments.         |   |    |
|   |   |   |    | |    | ssignment |                             |   |    |
|   |   |   |    | |    | excel     |                             |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 18 | Log in    | VCC User nmanager logs in.  |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 19 | Send a    | VCC User nmanager sends a   |   |    |
|   |   |   |    | |    | broadcast | broadcast message to 847    |   |    |
|   |   |   |    | |    | message   | candidates.                 |   |    |
|   |   |   |    | |    | to        |                             |   |    |
|   |   |   |    | |    | selected  |                             |   |    |
|   |   |   |    | |    | c         |                             |   |    |
|   |   |   |    | |    | andidates |                             |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 20 | Send a    | VCC User nmanager sends a   |   |    |
|   |   |   |    | |    | broadcast | broadcast message to 10100  |   |    |
|   |   |   |    | |    | message   | invigilators.               |   |    |
|   |   |   |    | |    | to        |                             |   |    |
|   |   |   |    | |    | selected  |                             |   |    |
|   |   |   |    | |    | inv       |                             |   |    |
|   |   |   |    | |    | igilators |                             |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | CS |           |                             |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 1  | Create Ad | Centre supervisor 10058-059 |   |    |
|   |   |   |    | |    | Hoc       | creates Ad Hoc invigilator  |   |    |
|   |   |   |    | |    | in        | 10034-087 at exam school    |   |    |
|   |   |   |    | |    | vigilator | 10058 centre D1350 with     |   |    |
|   |   |   |    | |    |           | subject A010C paper 3.      |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 2  | Modify    | Centre supervisor 10058-059 |   |    |
|   |   |   |    | |    | assigned  | modifies the collected      |   |    |
|   |   |   |    | |    | candidate | script count of assigned    |   |    |
|   |   |   |    | |    | script    | candidate 928949270 into 2  |   |    |
|   |   |   |    | |    |           | at exam school 10058 centre |   |    |
|   |   |   |    | |    |           | D1350 with subject A010C    |   |    |
|   |   |   |    | |    |           | paper 3.                    |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 3  | Create    | Centre supervisor 10058-059 |   |    |
|   |   |   |    | |    | centre    | creates invigilator         |   |    |
|   |   |   |    | |    | in        | assignment of exam centre   |   |    |
|   |   |   |    | |    | vigilator | at exam school 10058 centre |   |    |
|   |   |   |    | |    | a         | D1350 with subject A010C    |   |    |
|   |   |   |    | |    | ssignment | paper 3.                    |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 4  | Create    | Centre supervisor 10058-059 |   |    |
|   |   |   |    | |    | special   | creates invigilator         |   |    |
|   |   |   |    | |    | room      | assignment of 3 special     |   |    |
|   |   |   |    | |    | in        | room(s) at exam school      |   |    |
|   |   |   |    | |    | vigilator | 10058 centre D1350 with     |   |    |
|   |   |   |    | |    | a         | subject A010C paper 3.      |   |    |
|   |   |   |    | |    | ssignment |                             |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 5  | Delete    | Centre supervisor 30692-005 |   |    |
|   |   |   |    | |    | in        | deletes invigilator         |   |    |
|   |   |   |    | |    | vigilator | assignment at exam school   |   |    |
|   |   |   |    | |    | a         | 30692 centre P1150 with     |   |    |
|   |   |   |    | |    | ssignment | subject A010C paper 3.      |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 6  | Replace   | Centre supervisor 30701-029 |   |    |
|   |   |   |    | |    | in        | replaces the assignee of    |   |    |
|   |   |   |    | |    | vigilator | Seat Number 1-41 with       |   |    |
|   |   |   |    | |    | a         | invigilator 30701-052 at    |   |    |
|   |   |   |    | |    | ssignment | exam school 30701 centre    |   |    |
|   |   |   |    | |    |           | S1600 with subject A010C    |   |    |
|   |   |   |    | |    |           | paper 3.                    |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 7  | Modify    | Centre supervisor 10073-004 |   |    |
|   |   |   |    | |    | assigned  | modifies attendance status  |   |    |
|   |   |   |    | |    | candidate | of candidate 923503910 into |   |    |
|   |   |   |    | |    | a         | absent using spare barcode  |   |    |
|   |   |   |    | |    | ttendance | 0A010C0030A135065336 at     |   |    |
|   |   |   |    | |    |           | exam school 10073 centre    |   |    |
|   |   |   |    | |    |           | A1350 with subject A010C    |   |    |
|   |   |   |    | |    |           | paper 3.                    |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 8  | Log in    | Centre supervisor 10058-059 |   |    |
|   |   |   |    | |    |           | logs in at exam school      |   |    |
|   |   |   |    | |    |           | 10058 centre D1350 with     |   |    |
|   |   |   |    | |    |           | subject A010C paper 3.      |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 9  | Log out   | Centre supervisor 10066-004 |   |    |
|   |   |   |    | |    |           | logs out at exam school     |   |    |
|   |   |   |    | |    |           | 10066 centre B1400 with     |   |    |
|   |   |   |    | |    |           | subject A010C paper 3.      |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 10 | Create    | Centre supervisor 30740-061 |   |    |
|   |   |   |    | |    | chat      | creates chat group          |   |    |
|   |   |   |    | |    | group     | classroom_1025 with         |   |    |
|   |   |   |    | |    |           | invigilator(s) 30740-045,   |   |    |
|   |   |   |    | |    |           | 30740-041, 30740-020 at     |   |    |
|   |   |   |    | |    |           | exam school 30740 centre    |   |    |
|   |   |   |    | |    |           | S1750 with subject A010C    |   |    |
|   |   |   |    | |    |           | paper 3.                    |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 11 | Remove    | Centre supervisor 30740-061 |   |    |
|   |   |   |    | |    | chat      | removes chat group          |   |    |
|   |   |   |    | |    | group     | (classroom_1025) at exam    |   |    |
|   |   |   |    | |    |           | school 30740 centre S1750   |   |    |
|   |   |   |    | |    |           | with subject A010C paper 3. |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 12 | Save      | Centre supervisor 20355-044 |   |    |
|   |   |   |    | |    | sessional | saves sessional report at   |   |    |
|   |   |   |    | |    | report    | exam school 20355 centre    |   |    |
|   |   |   |    | |    |           | E1980 with subject A010C    |   |    |
|   |   |   |    | |    |           | paper 3.                    |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 13 | Submit    | Centre supervisor 20355-044 |   |    |
|   |   |   |    | |    | sessional | submits sessional report at |   |    |
|   |   |   |    | |    | report    | exam school 20355 centre    |   |    |
|   |   |   |    | |    |           | E1980 with subject A010C    |   |    |
|   |   |   |    | |    |           | paper 3.                    |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 14 | Create    | Centre supervisor 10058-059 |   |    |
|   |   |   |    | |    | special   | creates special room LTSR-2 |   |    |
|   |   |   |    | |    | room      | (MC-201) at exam school     |   |    |
|   |   |   |    | |    |           | 10058 centre D1350 with     |   |    |
|   |   |   |    | |    |           | subject A010C paper 3.      |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 15 | Delete    | Centre supervisor 10058-059 |   |    |
|   |   |   |    | |    | special   | deletes special room LTSR-2 |   |    |
|   |   |   |    | |    | room      | (MC-201) at exam school     |   |    |
|   |   |   |    | |    |           | 10058 centre D1350 with     |   |    |
|   |   |   |    | |    |           | subject A010C paper 3.      |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 16 | Move      | Centre supervisor 10058-059 |   |    |
|   |   |   |    | |    | assigned  | moves assigned candidate    |   |    |
|   |   |   |    | |    | candidate | 922569630 to special room   |   |    |
|   |   |   |    | |    | to        | at exam school 10058 centre |   |    |
|   |   |   |    | |    | special   | D1350 with subject A010C    |   |    |
|   |   |   |    | |    | room      | paper 3.                    |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 17 | Move      | Centre supervisor 10058-059 |   |    |
|   |   |   |    | |    | wrong     | moves wrong centre          |   |    |
|   |   |   |    | |    | centre    | candidate 227563142 to      |   |    |
|   |   |   |    | |    | candidate | special room at exam school |   |    |
|   |   |   |    | |    | to        | 10058 centre D1350 with     |   |    |
|   |   |   |    | |    | special   | subject A010C paper 3.      |   |    |
|   |   |   |    | |    | room      |                             |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 18 | Undo      | Centre supervisor 10058-059 |   |    |
|   |   |   |    | |    | moving    | undoes moving 928949270 to  |   |    |
|   |   |   |    | |    | candidate | special room at exam school |   |    |
|   |   |   |    | |    | to        | 10058 centre D1350 with     |   |    |
|   |   |   |    | |    | special   | subject A010C paper 3.      |   |    |
|   |   |   |    | |    | room      |                             |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 19 | Create    | Centre supervisor 10058-059 |   |    |
|   |   |   |    | |    | special   | creates special case        |   |    |
|   |   |   |    | |    | case      | Channnnnn using spare       |   |    |
|   |   |   |    | |    |           | barcode                     |   |    |
|   |   |   |    | |    |           | 0A010C0030D135073530 at     |   |    |
|   |   |   |    | |    |           | exam school 10058 centre    |   |    |
|   |   |   |    | |    |           | D1350 with subject A010C    |   |    |
|   |   |   |    | |    |           | paper 3.                    |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 20 | Update    | Centre supervisor 10058-059 |   |    |
|   |   |   |    | |    | special   | updates special case        |   |    |
|   |   |   |    | |    | case      | 227563142 candidate name    |   |    |
|   |   |   |    | |    |           | from \[empty\] into         |   |    |
|   |   |   |    | |    |           | 考生227563142, identity     |   |    |
|   |   |   |    | |    |           | document from \[empty\]     |   |    |
|   |   |   |    | |    |           | into 22756314(2), spare     |   |    |
|   |   |   |    | |    |           | barcode from                |   |    |
|   |   |   |    | |    |           | 0A010C0030D135062435 into   |   |    |
|   |   |   |    | |    |           | 0A010C0030D135030444,       |   |    |
|   |   |   |    | |    |           | script count from 2 into 3  |   |    |
|   |   |   |    | |    |           | at exam school 10058 centre |   |    |
|   |   |   |    | |    |           | D1350 with subject A010C    |   |    |
|   |   |   |    | |    |           | paper 3.                    |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 21 | Delete    | Centre supervisor 10058-059 |   |    |
|   |   |   |    | |    | special   | deletes special case Yo     |   |    |
|   |   |   |    | |    | case      | with spare barcode          |   |    |
|   |   |   |    | |    |           | 0A010C0030D135088910at exam |   |    |
|   |   |   |    | |    |           | school 10058 centre D1350   |   |    |
|   |   |   |    | |    |           | with subject A010C paper 3. |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 22 | Confirm   | Centre supervisor 10058-059 |   |    |
|   |   |   |    | |    | exam      | confirms exam status to     |   |    |
|   |   |   |    | |    | status    | Virtual Command Centre at   |   |    |
|   |   |   |    | |    |           | exam school 10058 centre    |   |    |
|   |   |   |    | |    |           | D1350 with subject A010C    |   |    |
|   |   |   |    | |    |           | paper 3.                    |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 23 | Check     | Centre supervisor 10058-059 |   |    |
|   |   |   |    | |    | in        | checks invigilator 2972615  |   |    |
|   |   |   |    | |    | vigilator | out at exam school 10058    |   |    |
|   |   |   |    | |    | out       | centre D1350 with subject   |   |    |
|   |   |   |    | |    |           | A010C paper 3.              |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 24 | Start     | Centre supervisor 10058-059 |   |    |
|   |   |   |    | |    | timer     | starts timer at 2022-10-28  |   |    |
|   |   |   |    | |    |           | 00:00 with duration 1380    |   |    |
|   |   |   |    | |    |           | minutes at exam school      |   |    |
|   |   |   |    | |    |           | 10058 centre D1350 with     |   |    |
|   |   |   |    | |    |           | subject A010C paper 3.      |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 25 | Switch to | Centre supervisor 10066-004 |   |    |
|   |   |   |    | |    | another   | switches to another subject |   |    |
|   |   |   |    | |    | subject   | or paper from exam school   |   |    |
|   |   |   |    | |    | or paper  | 10066 centre B1400 with     |   |    |
|   |   |   |    | |    | at the    | subject A010C paper 3.      |   |    |
|   |   |   |    | |    | same exam |                             |   |    |
|   |   |   |    | |    | centre    |                             |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 26 | Send      | Centre Supervisor 10066-004 |   |    |
|   |   |   |    | |    | not       | sends a notification        |   |    |
|   |   |   |    | |    | ification | message to invigilator      |   |    |
|   |   |   |    | |    | message   | 3642469 at exam school      |   |    |
|   |   |   |    | |    | to        | 10058 centre D1350 with     |   |    |
|   |   |   |    | |    | in        | subject A010C paper 3.      |   |    |
|   |   |   |    | |    | vigilator |                             |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 27 | Request   | Centre supervisor 10066-004 |   |    |
|   |   |   |    | |    | confirm   | requests invigilator        |   |    |
|   |   |   |    | |    | sessional | 3642469 and invigilator     |   |    |
|   |   |   |    | |    | report    | 5187641\'s confirmation of  |   |    |
|   |   |   |    | |    |           | the sessional report of     |   |    |
|   |   |   |    | |    |           | exam school 10058 centre    |   |    |
|   |   |   |    | |    |           | D1350 with subject A010C    |   |    |
|   |   |   |    | |    |           | paper 3.                    |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | C  |           |                             |   |    |
|   |   |   |    | | an |           |                             |   |    |
|   |   |   |    | | di |           |                             |   |    |
|   |   |   |    | | da |           |                             |   |    |
|   |   |   |    | | te |           |                             |   |    |
|   |   |   |    | | A  |           |                             |   |    |
|   |   |   |    | | pp |           |                             |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 1  | Request   | Candidate 229442562         |   |    |
|   |   |   |    | |    | passcode  | requests passcode.          |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 2  | Log in    | Candidate 229442562 logs    |   |    |
|   |   |   |    | |    |           | in.                         |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 3  | Log out   | Candidate 923515474 logs    |   |    |
|   |   |   |    | |    |           | out.                        |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 4  | Self      | Candidate 925736630         |   |    |
|   |   |   |    | |    | check-in  | succeeds to self check-in   |   |    |
|   |   |   |    | |    |           | at exam school 10058 centre |   |    |
|   |   |   |    | |    |           | D1350 with subject A010C    |   |    |
|   |   |   |    | |    |           | paper 3.                    |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 5  | Scan      | Candidate 226177594 scans a |   |    |
|   |   |   |    | |    | wrong     | wrong barcode               |   |    |
|   |   |   |    | |    | barcode   | 0A010C00392573663049z.      |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 6  | Confirm   | Candidate 925736630         |   |    |
|   |   |   |    | |    | at        | confirms reason and arrival |   |    |
|   |   |   |    | |    | special   | time in special room        |   |    |
|   |   |   |    | |    | room      | Special Room at exam school |   |    |
|   |   |   |    | |    | reason    | 10058 centre D1350 with     |   |    |
|   |   |   |    | |    | and       | subject A010C paper 3.      |   |    |
|   |   |   |    | |    | arrival   |                             |   |    |
|   |   |   |    | |    | time      |                             |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 7  | Read a    | Candidate 226177594 reads a |   |    |
|   |   |   |    | |    | message   | message from HKEAA,         |   |    |
|   |   |   |    | |    | from      | \"Hello4\".                 |   |    |
|   |   |   |    | |    | HKEAA     |                             |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 8  | Launch    | Candidate 226177594         |   |    |
|   |   |   |    | |    | ap        | launches the application as |   |    |
|   |   |   |    | |    | plication | a logged-in user.           |   |    |
|   |   |   |    | |    | as a      |                             |   |    |
|   |   |   |    | |    | logged-in |                             |   |    |
|   |   |   |    | |    | user      |                             |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 9  | Capture   | Candidate 226177594         |   |    |
|   |   |   |    | |    | S         | captures screenshot at exam |   |    |
|   |   |   |    | |    | creenshot | school 10058 centre D1350   |   |    |
|   |   |   |    | |    |           | with subject A010C paper 3. |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | I  |           |                             |   |    |
|   |   |   |    | | nv |           |                             |   |    |
|   |   |   |    | | ig |           |                             |   |    |
|   |   |   |    | | il |           |                             |   |    |
|   |   |   |    | | at |           |                             |   |    |
|   |   |   |    | | or |           |                             |   |    |
|   |   |   |    | | A  |           |                             |   |    |
|   |   |   |    | | pp |           |                             |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 1  | Log out   | Invigilator 3642469 logs    |   |    |
|   |   |   |    | |    |           | out.                        |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 2  | Mark      | Invigilator 5187641 marks   |   |    |
|   |   |   |    | |    | present   | candidate 927790210 present |   |    |
|   |   |   |    | |    | at centre | at exam school 10037 centre |   |    |
|   |   |   |    | |    |           | A1000 with subject A010C    |   |    |
|   |   |   |    | |    |           | paper 3.                    |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 3  | Create    | Invigilator 8548870 creates |   |    |
|   |   |   |    | |    | candidate | a flag for assigned         |   |    |
|   |   |   |    | |    | flag      | candidate CANDIDATE NAME    |   |    |
|   |   |   |    | |    |           | 929701546 at exam school    |   |    |
|   |   |   |    | |    |           | 10058 centre D1350 with     |   |    |
|   |   |   |    | |    |           | subject A010C paper 3.      |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 4  | Add       | Invigilator 7813095 adds a  |   |    |
|   |   |   |    | |    | candidate | remark to the flag for      |   |    |
|   |   |   |    | |    | remark    | assigned candidate          |   |    |
|   |   |   |    | |    |           | 923038470 at exam school    |   |    |
|   |   |   |    | |    |           | 10058 centre D1350 with     |   |    |
|   |   |   |    | |    |           | subject A010C paper 3.      |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 5  | Create    | Invigilator 7813095 creates |   |    |
|   |   |   |    | |    | check-out | a check-out record for      |   |    |
|   |   |   |    | |    | record    | assigned candidate          |   |    |
|   |   |   |    | |    |           | 923038470 at exam school    |   |    |
|   |   |   |    | |    |           | 10058 centre D1350 with     |   |    |
|   |   |   |    | |    |           | subject A010C paper 3.      |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 6  | Create    | Invigilator 30701-015       |   |    |
|   |   |   |    | |    | check-in  | creates a check-in record   |   |    |
|   |   |   |    | |    | record    | for assigned candidate      |   |    |
|   |   |   |    | |    |           | 922415239 at exam school    |   |    |
|   |   |   |    | |    |           | 30701 centre S1600 with     |   |    |
|   |   |   |    | |    |           | subject A010C paper 3.      |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 7  | Collect   | Invigilator 30701-015       |   |    |
|   |   |   |    | |    | script    | collects script from        |   |    |
|   |   |   |    | |    |           | assigned candidate          |   |    |
|   |   |   |    | |    |           | 927026601 at exam school    |   |    |
|   |   |   |    | |    |           | 30701 centre S1600 with     |   |    |
|   |   |   |    | |    |           | subject A010C paper 3.      |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 8  | Assgin    | Invigilator 8548870         |   |    |
|   |   |   |    | |    | spare     | registers spare barcode     |   |    |
|   |   |   |    | |    | barcode   | 0A010C0030D135068318 for    |   |    |
|   |   |   |    | |    | to        | assigned candidate          |   |    |
|   |   |   |    | |    | candidate | 929922120 at exam school    |   |    |
|   |   |   |    | |    |           | 10058 centre D1350 special  |   |    |
|   |   |   |    | |    |           | room LTSR-1 (SR1) with      |   |    |
|   |   |   |    | |    |           | subject A010C paper 3.      |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 9  | Create    | Invigilator 8548870 creates |   |    |
|   |   |   |    | |    | special   | special case 222102709 at   |   |    |
|   |   |   |    | |    | case      | exam school 10058 centre    |   |    |
|   |   |   |    | |    |           | D1350 with subject A010C    |   |    |
|   |   |   |    | |    |           | paper 3.                    |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 10 | Assign    | **Candidate Name is         |   |    |
|   |   |   |    | |    | wrong     | inputted:**                 |   |    |
|   |   |   |    | |    | centre    |                             |   |    |
|   |   |   |    | |    | candidate | Invigilator 8548870 assigns |   |    |
|   |   |   |    | |    | (Hall     | wrong centre candidate      |   |    |
|   |   |   |    | |    | special   | CCCCCCCC to special room    |   |    |
|   |   |   |    | |    | Case) to  | LTSR-1 (SR1) at exam school |   |    |
|   |   |   |    | |    | special   | 10058 centre D1350 with     |   |    |
|   |   |   |    | |    | room      | subject A010C paper 3.      |   |    |
|   |   |   |    | |    |           |                             |   |    |
|   |   |   |    | |    |           | /                           |   |    |
|   |   |   |    | |    |           |                             |   |    |
|   |   |   |    | |    |           | **Candidate No. is          |   |    |
|   |   |   |    | |    |           | inputted:**                 |   |    |
|   |   |   |    | |    |           |                             |   |    |
|   |   |   |    | |    |           | Invigilator 8548870 assigns |   |    |
|   |   |   |    | |    |           | wrong centre candidate      |   |    |
|   |   |   |    | |    |           | 229551349 to special room   |   |    |
|   |   |   |    | |    |           | LTSR-1 (SR1) at exam school |   |    |
|   |   |   |    | |    |           | 10058 centre D1350 with     |   |    |
|   |   |   |    | |    |           | subject A010C paper 3.      |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 11 | Assign    | Invigilator 8548870 assigns |   |    |
|   |   |   |    | |    | candidate | assigned candidate          |   |    |
|   |   |   |    | |    | special   | 928541456 to special room   |   |    |
|   |   |   |    | |    | room      | LTSR-1 (SR1) at exam school |   |    |
|   |   |   |    | |    |           | 10058 centre D1350 with     |   |    |
|   |   |   |    | |    |           | subject A010C paper 3.      |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 12 | Update    | Invigilator 30701-015       |   |    |
|   |   |   |    | |    | spare     | updates spare barcode from  |   |    |
|   |   |   |    | |    | barcode   | 0A010C0030A105011263 to     |   |    |
|   |   |   |    | |    |           | 0A010C0030S160077074 for    |   |    |
|   |   |   |    | |    |           | candidate 927790210 at exam |   |    |
|   |   |   |    | |    |           | school 30701 centre S1600   |   |    |
|   |   |   |    | |    |           | special room LTSR-1 (A001)  |   |    |
|   |   |   |    | |    |           | with subject A010C paper 3. |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 13 | Modify    | Invigilator 30701-015       |   |    |
|   |   |   |    | |    | candidate | modifies the collected      |   |    |
|   |   |   |    | |    | script    | script count of candidate   |   |    |
|   |   |   |    | |    |           | 927790210 into 1 at exam    |   |    |
|   |   |   |    | |    |           | school 30701 centre S1600   |   |    |
|   |   |   |    | |    |           | special room LTSR-1 (A001)  |   |    |
|   |   |   |    | |    |           | with subject A010C paper 3. |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 14 | Modify    | Invigilator 30701-015       |   |    |
|   |   |   |    | |    | candidate | modifies the confirmation   |   |    |
|   |   |   |    | |    | con       | status of candidate         |   |    |
|   |   |   |    | |    | firmation | 220011944 into SR4g at exam |   |    |
|   |   |   |    | |    | SR4g      | school 30701 centre S1600   |   |    |
|   |   |   |    | |    |           | special room LTSR-1 (A001)  |   |    |
|   |   |   |    | |    |           | with subject A010C paper 3. |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 15 | Create    | Invigilator 30701-015       |   |    |
|   |   |   |    | |    | special   | creates special room        |   |    |
|   |   |   |    | |    | room      | sessional report at exam    |   |    |
|   |   |   |    | |    | sessional | school 30701 centre S1600   |   |    |
|   |   |   |    | |    | report    | special room LTSR-1 (A001)  |   |    |
|   |   |   |    | |    |           | with subject A010C paper 3. |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 16 | Update    | Invigilator 30701-015       |   |    |
|   |   |   |    | |    | special   | updates special room        |   |    |
|   |   |   |    | |    | room      | sessional report at exam    |   |    |
|   |   |   |    | |    | sessional | school 30701 centre S1600   |   |    |
|   |   |   |    | |    | report    | special room LTSR-1 (A001)  |   |    |
|   |   |   |    | |    |           | with subject A010C paper 3. |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 17 | Complete  | Invigilator 30701-015       |   |    |
|   |   |   |    | |    | special   | completes special room      |   |    |
|   |   |   |    | |    | room      | sessional report at exam    |   |    |
|   |   |   |    | |    | sessional | school 30701 centre S1600   |   |    |
|   |   |   |    | |    | report    | special room LTSR-1 (A001)  |   |    |
|   |   |   |    | |    |           | with subject A010C paper 3. |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 18 | Confirm   | Invigilator 30701-015       |   |    |
|   |   |   |    | |    | di        | confirms discrepancy        |   |    |
|   |   |   |    | |    | screpancy | record(s) at exam school    |   |    |
|   |   |   |    | |    | record    | 30701 centre S1600 special  |   |    |
|   |   |   |    | |    |           | room LTSR-1 (A001) with     |   |    |
|   |   |   |    | |    |           | subject A010C paper 3.      |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 19 | Check in  | Invigilator 3642469 checks  |   |    |
|   |   |   |    | |    |           | in at exam school 10037     |   |    |
|   |   |   |    | |    |           | centre A1000 with subject   |   |    |
|   |   |   |    | |    |           | A010C paper 3.              |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 20 | Check out | Invigilator 3642469 checks  |   |    |
|   |   |   |    | |    |           | out at exam school 10037    |   |    |
|   |   |   |    | |    |           | centre A1000 with subject   |   |    |
|   |   |   |    | |    |           | A010C paper 3.              |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 21 | Mark      | Invigilator 9084306 marks   |   |    |
|   |   |   |    | |    | present   | candidate 225507716 present |   |    |
|   |   |   |    | |    | at        | at exam school 10058 centre |   |    |
|   |   |   |    | |    | special   | D1350 special room LTSR-1   |   |    |
|   |   |   |    | |    | room      | (1) with subject A010C      |   |    |
|   |   |   |    | |    |           | paper 3.                    |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 22 | SR update | Invigilator 8548870 marks   |   |    |
|   |   |   |    | |    | reason,   | reason at special room as B |   |    |
|   |   |   |    | |    | SR        | and arrival time as         |   |    |
|   |   |   |    | |    | arrival   | 2022-10-30 16:19 for        |   |    |
|   |   |   |    | |    | time      | assigned candidate          |   |    |
|   |   |   |    | |    |           | 924525711 goes to special   |   |    |
|   |   |   |    | |    |           | room LTSR-1 (SR1) at exam   |   |    |
|   |   |   |    | |    |           | school 10058 centre D1350   |   |    |
|   |   |   |    | |    |           | with subject A010C paper 3. |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 23 | SRI timer | Invigilator 8002055 starts  |   |    |
|   |   |   |    | |    |           | timer at 2022-10-30 20:26   |   |    |
|   |   |   |    | |    |           | with duration 75 minutes at |   |    |
|   |   |   |    | |    |           | exam school 10058 centre    |   |    |
|   |   |   |    | |    |           | D1350 special room LTSR-1   |   |    |
|   |   |   |    | |    |           | (aaa) with subject A010C    |   |    |
|   |   |   |    | |    |           | paper 3.                    |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 24 | Pause     | Invigilator 8002055         |   |    |
|   |   |   |    | |    | timer /   | pauses/resumes timer at     |   |    |
|   |   |   |    | |    | Resume    | 2022-10-30 20:26 with       |   |    |
|   |   |   |    | |    | timer     | duration 75 minutes at exam |   |    |
|   |   |   |    | |    |           | school 10058 centre D1350   |   |    |
|   |   |   |    | |    |           | special room LTSR-1 (aaa)   |   |    |
|   |   |   |    | |    |           | with subject A010C paper 3. |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 25 | Log in by | Invigilator 5317598 logs in |   |    |
|   |   |   |    | |    | scanning  | by scanning a QR code.      |   |    |
|   |   |   |    | |    | a QR code |                             |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 26 | View      | Invigilator 30740-020 views |   |    |
|   |   |   |    | |    | in        | information of candidate    |   |    |
|   |   |   |    | |    | formation | 920763210 displayed without |   |    |
|   |   |   |    | |    | of        | completing identity         |   |    |
|   |   |   |    | |    | candidate | verification or attendance  |   |    |
|   |   |   |    | |    | displayed | taking at exam school 30740 |   |    |
|   |   |   |    | |    | withou    | centre S1750 with subject   |   |    |
|   |   |   |    | |    | c         | A010C paper 3.              |   |    |
|   |   |   |    | |    | ompleting |                             |   |    |
|   |   |   |    | |    | indentity |                             |   |    |
|   |   |   |    | |    | ve        |                             |   |    |
|   |   |   |    | |    | rfication |                             |   |    |
|   |   |   |    | |    | or        |                             |   |    |
|   |   |   |    | |    | a         |                             |   |    |
|   |   |   |    | |    | ttendance |                             |   |    |
|   |   |   |    | |    | taking    |                             |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 27 | Verify    | Invigilator 30740-020       |   |    |
|   |   |   |    | |    | identity  | verifies identity of        |   |    |
|   |   |   |    | |    | of        | candidate 925307441 present |   |    |
|   |   |   |    | |    | c         | at exam school 30740 centre |   |    |
|   |   |   |    | |    | andidates | S1750 with subject A010C    |   |    |
|   |   |   |    | |    |           | paper 3.                    |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 28 | Take      | Invigilator 30740-020 takes |   |    |
|   |   |   |    | |    | a         | attendance for candidate    |   |    |
|   |   |   |    | |    | ttendance | 927752250 present at exam   |   |    |
|   |   |   |    | |    | for       | school 30740 centre S1750   |   |    |
|   |   |   |    | |    | c         | with subject A010C paper 3. |   |    |
|   |   |   |    | |    | andidates |                             |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    | | 29 | Launch    | Invigilator 30740-020       |   |    |
|   |   |   |    | |    | ap        | launches the application as |   |    |
|   |   |   |    | |    | plication | a logged-in user.           |   |    |
|   |   |   |    | |    | as a      |                             |   |    |
|   |   |   |    | |    | logged-in |                             |   |    |
|   |   |   |    | |    | user      |                             |   |    |
|   |   |   |    | +----+-----------+-----------------------------+   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | >                                                  |    |
|   |   |   |    | >                                                  |    |
|   |   |   |    | >                                                  |    |
+---+---+---+----+----------------------------------------------------+----+
| E | 1 | 1 | Re | 1.  More report types may be developed / available | >  |
| S | 2 | 3 | po |     for downloading in the Exam Support Backend    |  O |
| B | 8 | . | rt |     (SEAD) after the SR Forms Module was           | ut |
| ( |   | 4 | Li |     developed.                                     | >  |
| S |   | . | st |                                                    |  S |
| E |   | 5 |    | 2.  In order to prevent a huge volume of           | co |
| A |   |   |    |     information from being loaded, the 'No Data'   | pe |
| D |   |   |    |     page shall be displayed at first.              |    |
| ) |   |   |    |                                                    |    |
|   |   |   |    | 3.  Sessional Report                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   By filtering, a list of the centre related |    |
|   |   |   |    |         to the completion of the sessional reports |    |
|   |   |   |    |         shall be displayed, such as:               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Exam date (in yyyy-mm-dd format)       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Exam time (in hh:mn format)            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   School code                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   School name                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Centre code                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Centre type                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Exam date (in yyyy-mm-dd format)       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Exam time (in hh:mn format)            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Report completion status (Y/N)         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Exam data confirmation status by CS    |    |
|   |   |   |    |             (Y/N)                                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Searching fields shall include exam date,  |    |
|   |   |   |    |         exam start and end time, subject code,     |    |
|   |   |   |    |         paper group, school code, school name,     |    |
|   |   |   |    |         centre code, and centre type.              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Users shall be able to select columns      |    |
|   |   |   |    |         displayed by toggling the 'Preferences'    |    |
|   |   |   |    |         button.                                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   \[View\] button shall be available for the |    |
|   |   |   |    |         completed Sessional Reports and exam data  |    |
|   |   |   |    |         has been confirmed by CS. Click \[View\]   |    |
|   |   |   |    |         button shall display the Sessional Report  |    |
|   |   |   |    |         of the corresponding exam session.         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Click the check box on the column header   |    |
|   |   |   |    |         of the result table to select all records  |    |
|   |   |   |    |         and click the \[Export\] button to export  |    |
|   |   |   |    |         all records on all pages or                |    |
|   |   |   |    |         single/multiple select the row(s) and      |    |
|   |   |   |    |         click the \[Export\] button to export the  |    |
|   |   |   |    |         selected records in csv or excel.          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  Irregularities - Screenshot events (More       |    |
|   |   |   |    |     reports shall be provided after the            |    |
|   |   |   |    |     implementation of the SR Forms Module)         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   By filtering, a list of filtering results  |    |
|   |   |   |    |         shall be displayed with the information    |    |
|   |   |   |    |         of:                                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Subject name                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Subject code                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Paper group                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   School name                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   School code                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Centre code                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Centre type                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Exam date (in yyyy-mm-dd format)       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Exam time (in hh:mn:ss format)         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Number of abnormal case                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Searching fields shall include exam date,  |    |
|   |   |   |    |         exam start and end time, subject code,     |    |
|   |   |   |    |         paper group, school code, school name,     |    |
|   |   |   |    |         centre code, and centre type.              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Users shall be able to select columns      |    |
|   |   |   |    |         displayed by toggling the 'Preferences'    |    |
|   |   |   |    |         button.                                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   \[View\] button in the 'Action' column     |    |
|   |   |   |    |         shall be available for the detailed        |    |
|   |   |   |    |         records of irregularities in the           |    |
|   |   |   |    |         corresponding exam session. Following      |    |
|   |   |   |    |         fields shall be displayed:                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Candidate no./ID no., candidate name,      |    |
|   |   |   |    |         normal or special case, seat no., and the  |    |
|   |   |   |    |         screenshot event time in yyyy-mm-dd        |    |
|   |   |   |    |         hh:mn:ss format.                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Click the check box on the column header   |    |
|   |   |   |    |         of the result table to select all records  |    |
|   |   |   |    |         and click the \[Export\] button to export  |    |
|   |   |   |    |         all records on all pages or                |    |
|   |   |   |    |         single/multiple select the row(s) and      |    |
|   |   |   |    |         click the \[Export\] button to export the  |    |
|   |   |   |    |         selected records in csv or excel.          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 5.  CS / Invigilator Check in / out records        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   By filtering, a list of the exam session   |    |
|   |   |   |    |         shall be displayed including:              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Exam date (in yyyy-mm-dd format)       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Exam time (in hh:mn format)            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   School code                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   School name                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Centre code                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Centre type                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Subject code                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Subject name                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Paper group                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Searching fields shall include exam date,  |    |
|   |   |   |    |         exam start and end time, subject code,     |    |
|   |   |   |    |         paper group, school code, school name,     |    |
|   |   |   |    |         centre code, and centre type.              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Users shall be able to select columns      |    |
|   |   |   |    |         displayed by toggling the 'Preferences'    |    |
|   |   |   |    |         button.                                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   \[View\] button shall be available for the |    |
|   |   |   |    |         detailed check in / out records of exam    |    |
|   |   |   |    |         personnel in the corresponding exam        |    |
|   |   |   |    |         session. Following fields shall be         |    |
|   |   |   |    |         displayed:                                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   EP no./Application no./Ad hoc          |    |
|   |   |   |    |             invigilator no.                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   English name of invigilator            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Post (INV, SRI, CS)                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Assignment (centre code or seat no.    |    |
|   |   |   |    |             range if assignment created, '\--' for |    |
|   |   |   |    |             those assignments not yet created)     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Checked in time (in yyyy-mm-dd         |    |
|   |   |   |    |             hh:mn:ss format)                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Checked out time (in yyyy-mm-dd hh:mn:ss   |    |
|   |   |   |    |         format)                                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Click the check box on the column header   |    |
|   |   |   |    |         of the result table to select all records  |    |
|   |   |   |    |         and click the \[Export\] button to export  |    |
|   |   |   |    |         all records on all pages or                |    |
|   |   |   |    |         single/multiple select the row(s) and      |    |
|   |   |   |    |         click the \[Export\] button to export the  |    |
|   |   |   |    |         selected records into csv or excel.        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 6.  Candidate toilet request records               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   By filtering, a list of the exam session   |    |
|   |   |   |    |         shall be displayed including subject name, |    |
|   |   |   |    |         subject code, paper, school name, school   |    |
|   |   |   |    |         code, centre code, centre type, exam date  |    |
|   |   |   |    |         and exam time.                             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Searching fields shall include exam date,  |    |
|   |   |   |    |         exam start and end time, subject code,     |    |
|   |   |   |    |         paper group, school code, school name,     |    |
|   |   |   |    |         centre code, and centre type.              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Users shall be able to select columns      |    |
|   |   |   |    |         displayed by toggling the 'Preferences'    |    |
|   |   |   |    |         button.                                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   \[View\] button shall be available for the |    |
|   |   |   |    |         detailed toilet request records in the     |    |
|   |   |   |    |         corresponding exam session. Following      |    |
|   |   |   |    |         fields shall be displayed:                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Candidate No./ID No., candidate name,      |    |
|   |   |   |    |         normal or special case, action (IN/OUT),   |    |
|   |   |   |    |         recording time in hh:mm:ss format and      |    |
|   |   |   |    |         recorded by (EP no. and name of            |    |
|   |   |   |    |         CS/invigilator)                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Click the check box on the column header   |    |
|   |   |   |    |         of the result table to select all records  |    |
|   |   |   |    |         and click the \[Export\] button to export  |    |
|   |   |   |    |         all records on all pages or                |    |
|   |   |   |    |         single/multiple select the row(s) and      |    |
|   |   |   |    |         click the \[Export\] button to export the  |    |
|   |   |   |    |         selected records into csv or excel.        |    |
+---+---+---+----+----------------------------------------------------+----+
| E | 1 | 1 | S  | 1.  By filtering the Centre Type of an exam        | >  |
| S | 3 | 3 | us |     school, a list of suspended records shall be   |  O |
| B | 4 | . | pe |     displayed.                                     | ut |
| ( |   | 4 | nd |                                                    | >  |
| S |   | . | S  | 2.  Suspend an exam session                        |  S |
| E |   | 6 | es |                                                    | co |
| A |   |   | si |     -   Click the \[Add\] button                   | pe |
| D |   |   | on |                                                    |    |
| ) |   |   |    |     -   Search an exam session by selecting the    |    |
|   |   |   |    |         exam date, subject, paper, centre type of  |    |
|   |   |   |    |         an exam school.                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   a list of the centres shall be displayed.  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Click the check box on the column header   |    |
|   |   |   |    |         of the result table to select all records  |    |
|   |   |   |    |         and click the \[Suspend\] button to        |    |
|   |   |   |    |         suspend all the exam sessions of all pages |    |
|   |   |   |    |         or single/multiple select the exam         |    |
|   |   |   |    |         session(s) to suspend the selected exam    |    |
|   |   |   |    |         session(s)..                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Suspended result(s) shall be displayed.    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Suspended information shall be displayed   |    |
|   |   |   |    |         in the CS page and the invigilator app.    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 3.  Unsuspend an exam session                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   By filtering the Centre Type of an exam    |    |
|   |   |   |    |         school, a list of suspended exam           |    |
|   |   |   |    |         session(s) shall be displayed.             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Click the \[Edit\] button for unsuspend    |    |
|   |   |   |    |         exam session(s).                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Single / multiple select the suspended     |    |
|   |   |   |    |         exam session(s) to unsuspend the selected  |    |
|   |   |   |    |         exam session(s), or click the check box on |    |
|   |   |   |    |         the column header to select all the exam   |    |
|   |   |   |    |         sessions to unsuspend the exam sessions.   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Confirm to unsuspend the selected exam     |    |
|   |   |   |    |         session.                                   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Unsuspended information shall be displayed |    |
|   |   |   |    |         in the CS page and the invigilator app.    |    |
+---+---+---+----+----------------------------------------------------+----+
| E | 1 | 1 | L  | 1.  Users shall be able to enter their username    | >  |
| S | 3 | 3 | og |     and password to identify their role, and the   |  O |
| B | 6 | . | in |     access to specific functions and data are set  | ut |
| ( |   | 5 |    |     by the IT Admin.                               | >  |
| E |   | . |    |                                                    |  S |
| S |   | 1 |    | 2.  Function access is limited to the SEN system   | co |
| U |   |   |    |     only.                                          | pe |
| ) |   |   |    |                                                    |    |
+---+---+---+----+----------------------------------------------------+----+
| E | 1 | 1 | D  | 1.  Users shall be able to view the records by     | >  |
| S | 3 | 3 | as |     filtering VCC [confirmation]{.mark} status,    |  O |
| B | 7 | . | hb |     exam date, operator, school code, school name, | ut |
| ( |   | 5 | oa |     centre code, centre type, subject code,        | >  |
| E |   | . | rd |     subject name, and paper code.                  |  S |
| S |   | 2 |    |                                                    | co |
| U |   |   |    | 2.  Pie charts shall be able to reflect the        | pe |
| ) |   |   |    |     statistics of the filtering result:            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   Attendance discrepancy                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Unverified                                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Present and Absent                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   Overall situation                              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Pending to Confirm                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Confirmed without Discrepancy              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Confirmed but with Attendance and/or       |    |
|   |   |   |    |         Script Discrepancy                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | -   Irregularity by Helpdesk                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Confirmed but with Attendance and/or       |    |
|   |   |   |    |         Script Discrepancy                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 3.  A table displaying the real-time exam          |    |
|   |   |   |    |     information of all / designated:               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | +----------+-----------------------------------+   |    |
|   |   |   |    | | Field    | Description                       |   |    |
|   |   |   |    | | Name     |                                   |   |    |
|   |   |   |    | +==========+===================================+   |    |
|   |   |   |    | | VCC      | The timestamp of confirmation of  |   |    |
|   |   |   |    | | c        | exam data accuracy by VCC         |   |    |
|   |   |   |    | | onfirmed |                                   |   |    |
|   |   |   |    | | time     |                                   |   |    |
|   |   |   |    | +----------+-----------------------------------+   |    |
|   |   |   |    | | Operator | The helpdesk account assigned to  |   |    |
|   |   |   |    | |          | monitor the exam session          |   |    |
|   |   |   |    | +----------+-----------------------------------+   |    |
|   |   |   |    | | Subject  | Unique code of the subject as     |   |    |
|   |   |   |    | | Code     | recorded in the HKDSE system      |   |    |
|   |   |   |    | +----------+-----------------------------------+   |    |
|   |   |   |    | | Paper    | Paper code of the subject         |   |    |
|   |   |   |    | | Group    |                                   |   |    |
|   |   |   |    | +----------+-----------------------------------+   |    |
|   |   |   |    | | Centre   | Unique code of the exam centre as |   |    |
|   |   |   |    | | Code     | recorded in the HKDSE system      |   |    |
|   |   |   |    | +----------+-----------------------------------+   |    |
|   |   |   |    | | Centre   | Type of teh exam centre, such as  |   |    |
|   |   |   |    | | Type     | HALL, CLASSROOM, etc.             |   |    |
|   |   |   |    | +----------+-----------------------------------+   |    |
|   |   |   |    | | Assigned | No. of candidates assigned to the |   |    |
|   |   |   |    | | C        | exam centre.                      |   |    |
|   |   |   |    | | andidate |                                   |   |    |
|   |   |   |    | +----------+-----------------------------------+   |    |
|   |   |   |    | | Present  | No. of candidate with attendance  |   |    |
|   |   |   |    | | Count    | status 'Present'                  |   |    |
|   |   |   |    | +----------+-----------------------------------+   |    |
|   |   |   |    | | Absent   | No. of candidate with attendance  |   |    |
|   |   |   |    | | Count    | status 'Absent'                   |   |    |
|   |   |   |    | +----------+-----------------------------------+   |    |
|   |   |   |    | | Moved to | No. of candidates who were moved  |   |    |
|   |   |   |    | | SR Count | by the CS from the assigned exam  |   |    |
|   |   |   |    | |          | centre to the special room.       |   |    |
|   |   |   |    | |          |                                   |   |    |
|   |   |   |    | |          | For SEN, it should be zero.       |   |    |
|   |   |   |    | +----------+-----------------------------------+   |    |
|   |   |   |    | | Un       | The total number of assigned      |   |    |
|   |   |   |    | | verified | candidates whose attendance       |   |    |
|   |   |   |    | | At       | status have not yet been updated  |   |    |
|   |   |   |    | | tendance | as present or absent              |   |    |
|   |   |   |    | |          |                                   |   |    |
|   |   |   |    | |          | i.e. missing attendance           |   |    |
|   |   |   |    | +----------+-----------------------------------+   |    |
|   |   |   |    | | Absent   | The total number of scripts       |   |    |
|   |   |   |    | | but with | collected that the assigned       |   |    |
|   |   |   |    | | script   | candidates who are absent from    |   |    |
|   |   |   |    | | c        | the exam session                  |   |    |
|   |   |   |    | | ollected |                                   |   |    |
|   |   |   |    | +----------+-----------------------------------+   |    |
|   |   |   |    | | Special  | Total no. of special cases in the |   |    |
|   |   |   |    | | Case     | exam centre, i.e. wrong centre    |   |    |
|   |   |   |    | | Count    | candidate                         |   |    |
|   |   |   |    | +----------+-----------------------------------+   |    |
|   |   |   |    | | Special  | No. of special case created by    |   |    |
|   |   |   |    | | Case At  | the CS in the exam centre         |   |    |
|   |   |   |    | | Hall/C   |                                   |   |    |
|   |   |   |    | | lassroom |                                   |   |    |
|   |   |   |    | +----------+-----------------------------------+   |    |
|   |   |   |    | | Special  | No. of special cases created by   |   |    |
|   |   |   |    | | Case at  | the special room invigilator in   |   |    |
|   |   |   |    | | SR       | the special room of the exam      |   |    |
|   |   |   |    | |          | centre.                           |   |    |
|   |   |   |    | |          |                                   |   |    |
|   |   |   |    | |          | For SEN, it should be zero.       |   |    |
|   |   |   |    | +----------+-----------------------------------+   |    |
|   |   |   |    | | Total    | Total no. of script to be         |   |    |
|   |   |   |    | | Script   | collected of the subject paper    |   |    |
|   |   |   |    | | to be    | multiply (assigned candidate and  |   |    |
|   |   |   |    | | C        | the special case).                |   |    |
|   |   |   |    | | ollected |                                   |   |    |
|   |   |   |    | +----------+-----------------------------------+   |    |
|   |   |   |    | | Missing  | Total no. of missing scripts that |   |    |
|   |   |   |    | | Script   | should be collected of the        |   |    |
|   |   |   |    | |          | assigned candidates (with present |   |    |
|   |   |   |    | |          | status) + Total no. of missing    |   |    |
|   |   |   |    | |          | scripts that should be collected  |   |    |
|   |   |   |    | |          | of the special cases (wrong       |   |    |
|   |   |   |    | |          | centre candidates)                |   |    |
|   |   |   |    | +----------+-----------------------------------+   |    |
|   |   |   |    | | Script   | The total number of scripts       |   |    |
|   |   |   |    | | C        | collected that the assigned       |   |    |
|   |   |   |    | | ollected | candidates whose attendance       |   |    |
|   |   |   |    | | from     | status is present + Total number  |   |    |
|   |   |   |    | | Present  | of scripts collected from the     |   |    |
|   |   |   |    | | C        | special cases(wrong centre        |   |    |
|   |   |   |    | | andidate | candidates)                       |   |    |
|   |   |   |    | +----------+-----------------------------------+   |    |
|   |   |   |    | | Remarks  | Written remarks inputted by a CS  |   |    |
|   |   |   |    | | from CS  | when confirming the exam data     |   |    |
|   |   |   |    | |          | accuracy                          |   |    |
|   |   |   |    | +----------+-----------------------------------+   |    |
|   |   |   |    | | Noti     | The CS of the exam centre was     |   |    |
|   |   |   |    | | fication | notified for exam                 |   |    |
|   |   |   |    | | to CS    | dismissal(Yes/No)                 |   |    |
|   |   |   |    | +----------+-----------------------------------+   |    |
|   |   |   |    | | Confirm  | Confirm status from VCC to ESU    |   |    |
|   |   |   |    | | to ESU   | (Pending to Confirm/Confirmed to  |   |    |
|   |   |   |    | |          | ESU)                              |   |    |
|   |   |   |    | +----------+-----------------------------------+   |    |
|   |   |   |    | | C        | VCC staff who confirm the exam    |   |    |
|   |   |   |    | | onfirmed | data to ESU                       |   |    |
|   |   |   |    | | by       |                                   |   |    |
|   |   |   |    | +----------+-----------------------------------+   |    |
|   |   |   |    | | VCC      | VCC's input remark when confirm   |   |    |
|   |   |   |    | | Conf     | exam data to ESU                  |   |    |
|   |   |   |    | | irmation |                                   |   |    |
|   |   |   |    | | Remark   |                                   |   |    |
|   |   |   |    | +----------+-----------------------------------+   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | >                                                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  Users shall be able to sort the table by the   |    |
|   |   |   |    |     field labels.                                  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | <!-- -->                                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 5.  Users shall be able to select columns          |    |
|   |   |   |    |     displayed by toggling the 'Preferences'        |    |
|   |   |   |    |     button.                                        |    |
+---+---+---+----+----------------------------------------------------+----+
| E | 1 | 1 | At | 1.  Users shall be able to select to display the   | >  |
| S | 3 | 3 | te |     attendance record between the allocated        |  O |
| B | 9 | . | nd |     candidates and the special case by clicking    | ut |
| ( |   | 5 | an |     the corresponding tabs.                        | >  |
| E |   | . | ce |                                                    |  S |
| S |   | 3 | R  | 2.  Users shall be able to view the records by     | co |
| U |   |   | ec |     filtering the exam year, exam date range,      | pe |
| ) |   |   | or |     centre code, subject code, paper group,        |    |
|   |   |   | ds |     candidate no., seat no., attendance status     |    |
|   |   |   |    |     (i.e. present, absent, not yet taken), answer  |    |
|   |   |   |    |     script collection status and the special room  |    |
|   |   |   |    |     (centre type).                                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 3.  Exam data shall be displayed in the result     |    |
|   |   |   |    |     table, such as:                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   School name                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Subject name                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Paper group                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Centre code                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Mode (applicable to listening paper)       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Candidate number                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Candidate surname                          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Candidate name                             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Seat number                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Attendance status (U - attendance record   |    |
|   |   |   |    |         not yet taken, present, absent)            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Answer script collection status (answer    |    |
|   |   |   |    |         scripts collected / answer scripts to be   |    |
|   |   |   |    |         collected)                                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Location (applicable to normal exam        |    |
|   |   |   |    |         centre)                                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Number of answer script collected by ESU   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Subject code                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  Exam data displayed in the result table shall  |    |
|   |   |   |    |     be sorted by the fields.                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 5.  Users shall be able to select columns          |    |
|   |   |   |    |     displayed by toggling the 'Preferences'        |    |
|   |   |   |    |     button.                                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 6.  Exam data displayed in the result table shall  |    |
|   |   |   |    |     be able to be exported as a CSV file.          |    |
+---+---+---+----+----------------------------------------------------+----+
| E | 1 | 1 | D  | 1.  Users shall be able to view the discrepancy    | >  |
| S | 4 | 3 | is |     records by filtering the exam date, exam time, |  O |
| B | 0 | . | cr |     centre code, centre type, subject code, paper  | ut |
| ( |   | 5 | ep |     group and the candidate no.                    | >  |
| E |   | . | an |                                                    |  S |
| S |   | 4 | cy | 2.  Discrepancy records related to allocated       | co |
| U |   |   | Re |     candidates and special cases shall be          | pe |
| ) |   |   | po |     displayed. Users shall be able to select among |    |
|   |   |   | rt |     two types of cases by clicking the             |    |
|   |   |   |    |     corresponding tabs.                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 3.  Discrepancy records shall be displayed in the  |    |
|   |   |   |    |     result table, such as:                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Candidate number                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Candidate name                             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Subject name                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Subject code                               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Paper group                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   School name                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   School code                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Centre code                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Centre type                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Mode (applicable to the listening paper)   |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Spare barcode number                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Seat number                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Attendance status ('- -' means attendance  |    |
|   |   |   |    |         record not yet taken, present, absent)     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Answer script collection status (answer    |    |
|   |   |   |    |         scripts collected / answer scripts to be   |    |
|   |   |   |    |         collected)                                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Remarks - there are 4 types of discrepancy |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Missing attendance record(s)           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Missing attendance but with script     |    |
|   |   |   |    |             collected                              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Missing script records                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Absent but with script(s) collected    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Location (applicable to the normal exam    |    |
|   |   |   |    |         centre)                                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  Discrepancy records displayed in the result    |    |
|   |   |   |    |     table shall be sorted by the fields.           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 5.  Users shall be able to select columns          |    |
|   |   |   |    |     displayed by toggling the 'Preferences'        |    |
|   |   |   |    |     button.                                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 6.  Users shall be able to export the discrepancy  |    |
|   |   |   |    |     records displayed in the result table to a CSV |    |
|   |   |   |    |     file.                                          |    |
+---+---+---+----+----------------------------------------------------+----+
| E | 1 | 1 | E  | 1.  Users shall be able to view the event log by   | >  |
| S | 4 | 3 | ve |     filtering the exam date, exam time, school     |  O |
| B | 2 | . | nt |     code, centre code, centre type, subject code,  | ut |
| ( |   | 5 | L  |     paper group and the candidate no.              | >  |
| E |   | . | og |                                                    |  S |
| S |   | 5 |    | 2.  Event log shall be displayed in the result     | co |
| U |   |   |    |     table, such as:                                | pe |
| ) |   |   |    |                                                    |    |
|   |   |   |    |     -   Event date and time (in yyyy-mm-dd         |    |
|   |   |   |    |         hh:mn:ss format)                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Centre code                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   School code                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Candidate number / EP no. of CS or         |    |
|   |   |   |    |         invigilator                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Actor type (candidate, CS, DCS, VCC)       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Event                                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Location (HALL, SEN CLASSROOM)             |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 3.  The event log displayed in the result table    |    |
|   |   |   |    |     shall be sorted by the fields.                 |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  Users shall be able to select columns          |    |
|   |   |   |    |     displayed by toggling the 'Preferences'        |    |
|   |   |   |    |     button.                                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 5.  Users shall be able to export the event log    |    |
|   |   |   |    |     displayed in the result table to a CSV file.   |    |
+---+---+---+----+----------------------------------------------------+----+
| E | 1 | 1 | Re | 1.  Different report types shall be developed and  | >  |
| S | 4 | 3 | po |     selected for downloading.                      |  O |
| B | 2 | . | rt |                                                    | ut |
| ( |   | 5 | Li | 2.  [Audit Report]{.mark}                          | >  |
| E |   | . | st |                                                    |  S |
| S |   | 6 |    |     -   [Users]{.mark} shall be able to retrieve   | co |
| U |   |   |    |         the data by filtering candidate no.,       | pe |
| ) |   |   |    |         subject code, paper group, attendance      |    |
|   |   |   |    |         status and the exam data range.            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Records shall be displayed with:           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Action (event)                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Action time (in yyyy-mm-dd hh:mn:ss    |    |
|   |   |   |    |             format)                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Exam year                              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Subject code                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Paper group                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Centre code                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Seat number                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Exam date (in yyyy-mm-dd format)       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Candidate number                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Candidate name                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Invigilator number                     |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Attendance status (present, absent,    |    |
|   |   |   |    |             not yet taken)                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Scanning status                        |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Remarks                                |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Last update by                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Last update date                       |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Function of quick download shall be        |    |
|   |   |   |    |         provided without showing the data on       |    |
|   |   |   |    |         screen.                                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | <!-- -->                                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 3.  Attendance Summary Report                      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Users shall be able to retrieve the data   |    |
|   |   |   |    |         by filtering the exam date range.          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Records shall be displayed with:           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Subject code                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Paper group                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Centre code                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Centre type                            |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   Centre name (school name)              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   No. of candidates unverified           |    |
|   |   |   |    |             (attendance record not yet taken)      |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   No. of candidates present              |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   No. of candidates absent               |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |         -   No. of candidates move to SR           |    |
|   |   |   |    |             (applicable to the nomal exam centre)  |    |
|   |   |   |    |                                                    |    |
|   |   |   |    |     -   Function of quick download shall be        |    |
|   |   |   |    |         provided without showing the data on       |    |
|   |   |   |    |         screen.                                    |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 4.  Data displayed in the result table shall be    |    |
|   |   |   |    |     sorted by the fields.                          |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 5.  Users shall be able to export the data         |    |
|   |   |   |    |     displayed as CSV file.                         |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | <!-- -->                                           |    |
|   |   |   |    |                                                    |    |
|   |   |   |    | 6.  SR Form shall be added (Details will be synced |    |
|   |   |   |    |     with the SR Form Modules)                      |    |
+---+---+---+----+----------------------------------------------------+----+
