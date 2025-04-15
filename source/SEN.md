Function in SEN Spec

 

<table>
<colgroup>
<col style="width: 3%" />
<col style="width: 3%" />
<col style="width: 3%" />
<col style="width: 7%" />
<col style="width: 74%" />
<col style="width: 7%" />
</colgroup>
<thead>
<tr class="header">
<th>Module</th>
<th>Page</th>
<th>Index</th>
<th>Summary</th>
<th>Feature Detail</th>
<th><p>In Scope /</p>
<p>Out Scope</p></th>
</tr>
<tr class="odd">
<th>Invi App</th>
<th>5</th>
<th>13.1.1</th>
<th>SEN Invigilator Login</th>
<th><ol type="1">
<li><blockquote>
<p>Invigilator’s EP number/Application number shall be used to recognize
the specific exam session of the exam centre that he/she is responsible
for.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to login the App with or without the EP number /
Application number.</p>
</blockquote></li>
<li><blockquote>
<p>For ad hoc invigilators without EP / Application number, CS shall
enter their english name / HKID no. and select the school name and code
they come from in the drop-down list to create a unique QR code for the
invigilator to login.</p>
</blockquote></li>
<li><blockquote>
<p>Invigilator shall scan the QR code provided by the SEN CS to login
‘i-Invigilation (HKDSE)’ (Invigilator App)</p>
</blockquote></li>
<li><blockquote>
<p>Under certain circumstances (e.g. a single candidate classroom centre
which may not have the formal invigilator), the CS shall be able to scan
and login themselves as the classroom invigilator to perform
invigilation besides performing the duties of CS at the same time.</p>
</blockquote></li>
<li><blockquote>
<p>After login, the App shall show:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Invigilator information:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Name</p>
</blockquote></li>
<li><blockquote>
<p>EP number/Application number</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Assigned duties:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Exam date</p>
</blockquote></li>
<li><blockquote>
<p>Exam centre code (for Classroom Invigilators, it shall be displayed
after assignment created by the Classroom CS)</p>
</blockquote></li>
<li><blockquote>
<p>Exam centre location</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>For Hall Invigilators, a dashboard of basic functions shall be
displayed.</p>
</blockquote>
<ul>
<li><blockquote>
<p>Take attendance / Verify identity</p>
</blockquote></li>
<li><blockquote>
<p>Check-in/Out (Toilet Request)</p>
</blockquote></li>
<li><blockquote>
<p>Script Counting</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>For Classroom Invigilators, an empty dashboard shall be shown.</p>
</blockquote></li>
<li><blockquote>
<p>The dashboard shall be updated after the invigilator assignment
created by the Hall or Classroom CS.</p>
</blockquote></li>
</ul></li>
</ol>
<blockquote>
<p> </p>
</blockquote></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="header">
<th>Invi App</th>
<th>6</th>
<th>13.1.2</th>
<th>SEN Invigilators shift duty without the presence of CS</th>
<th><ol type="1">
<li><blockquote>
<p>Users shall be able to login the App without the presence of CS to
provide the login code if they are assigned to take over the duties of
existing invigilators (e.g. A PM invigilator takes over the duties of an
AM invigilator during 12:00pm - 12:30pm for an exam session to end after
2:00pm, Early leave of the existing invigilator) by one of the following
methods:</p>
</blockquote>
<ul>
<li><blockquote>
<p>For the invigilators who bring their own devices for invigilation
(i.e. BYOD), the App shall allow the existing invigilator to trigger the
inheritance of assignment by tapping the ‘Shift duty’ button at the side
menu. Then, a QR code shall be shown on the ‘Shift Duty’ page. The new
invigilator shall tap the ‘Login’ button on his / her own device, scan
the QR code, and enter the login credential to login and check-in in
order to take over the assignment.</p>
</blockquote></li>
<li><blockquote>
<p>For both the existing and new invigilators who share the same device
provided by the HKEAA, the App shall allow the existing invigilator to
trigger the inheritance of assignment by tapping the ‘Shift duty’ button
at the side menu and then tapping the ‘Shift duty’ button on the ‘Shift
Duty’ page. The new invigilator shall enter the login credential to
login and check-in in order to take over the assignment.</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>For the invigilators to login, EP / Application Number shall be
entered.</p>
</blockquote></li>
<li><blockquote>
<p>For the ad hoc invigilators without EP / Application Number to login,
English Name / ID Number shall be entered. School Name and Code of the
schools where they come from shall be mandatorily selected from the
drop-down list:</p>
</blockquote>
<ul>
<li><blockquote>
<p>The drop-down list with all school names and codes shall be displayed
at the field for users to select if no character(s) is inputted.</p>
</blockquote></li>
<li><blockquote>
<p>By inputting character(s), corresponding school name(s) and code(s)
shall be displayed in the drop-down list at the field for users to
select.</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Once the new invigilator has logged in the module, the system shall
force to logout the existing invigilator who has logged in the same exam
session and a message "Do you want to replace the existing invigilator?”
shall be displayed to confirm the forced logout.</p>
</blockquote></li>
<li><blockquote>
<p>Once the new invigilator has logged in the module and the existing
invigilator has been forced to log out, the states of assignment and
tasks of the existing invigilator shall be inherited by the new
invigilator.</p>
</blockquote></li>
<li><blockquote>
<p>The system shall record the actions which shall be able to be found
at the ‘Event Log’ of Exam Support Backend (SEAD) module.</p>
</blockquote></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>Invi App</th>
<th>8</th>
<th>13.1.3</th>
<th>Assignment Retrieval</th>
<th><ol type="1">
<li><blockquote>
<p>Users shall be assigned to manage the zone(s) consisting of the
candidates that are arranged according to their exam time.</p>
</blockquote>
<ul>
<li><blockquote>
<p>Single invigilator shall be able to be assigned to manage multiple
zones.</p>
</blockquote></li>
<li><blockquote>
<p>Multiple invigilators shall be allowed to be assigned to a single
zone (i.e. applicable to Classroom Invigilator).</p>
</blockquote></li>
<li><blockquote>
<p>Users shall view &amp; work with the candidates in those zone(s)
assigned to them.</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Users shall be able to view the updated dashboard with:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Take attendance/verify identity with alert if missing attendance
records found</p>
</blockquote>
<ul>
<li><blockquote>
<p>Present count including:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Verified self check-in with the format of x (y) where x is number of
self checked-in candidates verified by the invigilator and y is the
number of candidates who have self checked-in.</p>
</blockquote></li>
<li><blockquote>
<p>Verified and attendance taken by invigilator</p>
</blockquote></li>
<li><blockquote>
<p>Attendance involved SR1</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Special Case (i.e. wrong centre candidate, applicable to the
Classroom Invigilator)</p>
</blockquote></li>
<li><blockquote>
<p>Absent count</p>
</blockquote></li>
<li><blockquote>
<p>Total count of candidates assigned to the invigilator</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Check-in/out (Toilet Request) with alert if candidate not yet back
after check-out</p>
</blockquote></li>
<li><blockquote>
<p>Script Counting with number of scripts collected, with alert if there
is missing script</p>
</blockquote></li>
<li><blockquote>
<p>Report with alerts if discrepancy is found, sessional report is not
completed and no seating plan is uploaded (applicable to Classroom
Invigilator)</p>
</blockquote>
<ul>
<li><blockquote>
<p>Summary Report</p>
</blockquote></li>
<li><blockquote>
<p>Discrepancy Report with alert if there is a discrepancy</p>
</blockquote></li>
<li><blockquote>
<p>Sessional Report with alert if not completed</p>
</blockquote></li>
</ul></li>
</ul></li>
</ol>
<blockquote>
<p><mark>Seating Pla</mark>n with alert if not provided</p>
</blockquote></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="header">
<th>Invi App</th>
<th>11</th>
<th>13.1.4</th>
<th>Attendance Taking / Verify Identity</th>
<th><ol type="1">
<li><blockquote>
<p>A list of zones with the corresponding zone name(s) shall be
displayed under ‘Assign Zone’ after tapping the ‘Take attendance /
Verify identity’ section. Candidates of different subjects having the
same timetable shall be grouped under the same zone.</p>
</blockquote></li>
<li><blockquote>
<p>For each assigned zone, the exam time and the supervised break(s)
shall be listed.</p>
</blockquote></li>
<li><blockquote>
<p>By tapping into each zone, a list shall be able to separate the
candidates with different attendance status: Pending, Present, Absent
(and Special Cases for the Classroom Invigilator). Number of candidates
involved in different status shall also be displayed.</p>
</blockquote></li>
<li><blockquote>
<p>The candidate list shall be displayed for the selected attendance
status with the following fields:</p>
</blockquote>
<ul>
<li><blockquote>
<p>(Seat number of allocated candidate or ‘- -’ for wrong centre
candidate) Candidate number</p>
</blockquote></li>
<li><blockquote>
<p>Candidate name</p>
</blockquote></li>
<li><blockquote>
<p>Subject/Paper name</p>
</blockquote></li>
<li><blockquote>
<p>Case number (the length ranges from 11 to 12 characters depends on
the trailing numbers followed by the disabilities code, e.g. DSE2021A001
and DSE2021A0001).</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>There is a right arrow at the right side of the case number to
indicate that the candidate carries remarks.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to view the SEN Remarks of the candidate by
clicking the right arrow</p>
</blockquote></li>
<li><blockquote>
<p>There shall be no need to set the validation of preventing
invigilators from updating attendance records after the exam ends.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall confirm the candidates’ identity verification if the
candidates have self checked-in.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall scan the candidates’ personalized barcode and confirm
their identity verification if the candidates have not self
checked-in.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to input remarks when flagging a candidate.</p>
</blockquote></li>
<li><blockquote>
<p>SR1 shall be able to be chosen when at least one of the following
conditions exist (i.e. shall be updated after the SR Forms Module is
applied):</p>
</blockquote>
<ul>
<li><blockquote>
<p>Produce Admission Form - Yes / No</p>
</blockquote></li>
<li><blockquote>
<p>Produce Identity Card (or valid identification document with a
photograph) - Yes / No</p>
</blockquote></li>
<li><blockquote>
<p>Photograph resembles candidate - Yes / No</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Users shall be able to mark the candidate’s attendance record as
Absent by swiping a candidate record to the left and clicking the red
‘abs’ button.</p>
</blockquote></li>
<li><blockquote>
<p>Seating rearrangement (without changing the original seat no.) is
allowed in the SEN exam centre.</p>
</blockquote></li>
</ol></th>
<th><blockquote>
<p>Only point 13 is in-scope</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>Invi App</th>
<th>15</th>
<th>13.1.5</th>
<th>Maintain Attendance and Script Records of Special Case (applicable
to Classroom Invigilator)</th>
<th><ol type="1">
<li><blockquote>
<p>By tapping into each zone, select Special Case for filtering, a list
of special case candidates shall be displayed with following
information.</p>
</blockquote>
<ul>
<li><blockquote>
<p>(Seat number) Candidate number</p>
</blockquote></li>
<li><blockquote>
<p>Candidate name</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Users shall be able to swipe a candidate record to the left and click
the green ‘Details’ button. Then, they shall be able to edit the spare
barcode number and script collected.</p>
</blockquote></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="header">
<th>Invi App</th>
<th>17</th>
<th>13.1.6</th>
<th>Candidate Check-in/out (Toilet Request)</th>
<th><ol type="1">
<li><blockquote>
<p>Users shall be able to record the toilet request of candidates right
after they have checked-in the exam sessions in order to handle the
toilet requests before exam start.</p>
</blockquote></li>
<li><blockquote>
<p>An alert icon shall be shown if the candidate is not yet back after
check-out a specified period of time (e.g. 15 minutes, which shall be
maintained as the parameter by HKEAA in the Exam Support Backend (SEAD)
module).</p>
</blockquote></li>
<li><blockquote>
<p>By tapping the ‘Check-in/out (Toilet Request)’ section under the
Dashboard, the invigilator shall scan the candidate’s personalized
barcode or admission form to record the request. Then, the personal
information (i.e. document number, candidate number and seat number) of
the candidate and the status of toilet request (i.e. check-in/out and
current timestamp by default) shall be shown for user’s confirmation.
The notification signal for those candidates who take over specific time
should be sent to the relevant Invigilator or CS.</p>
</blockquote></li>
<li><blockquote>
<p>The default check-in/out timestamp shall be able to be edited by
clicking the pencil icon.</p>
</blockquote></li>
<li><blockquote>
<p>By tapping the ‘Toilet Request Record(s)’ button of the scanner page,
the users shall be able to view the list of candidates involving the
toilet requests. The following information shall be shown in each
record:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Candidate Number</p>
</blockquote></li>
<li><blockquote>
<p>Seat Number</p>
</blockquote></li>
<li><blockquote>
<p>Candidate Name</p>
</blockquote></li>
<li><blockquote>
<p>Check-in and/or check-out</p>
</blockquote></li>
<li><blockquote>
<p>The timestamp of check-in and /or check-out</p>
</blockquote></li>
</ul></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>Invi App</th>
<th>19</th>
<th>13.1.7</th>
<th>Script Counting</th>
<th><ol type="1">
<li><blockquote>
<p>Users shall be able to scan the personalised barcodes / spare
barcodes on the scripts to count the number of scripts collected.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to view the number of scripts collected by their
own accounts in the Dashboard.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be allowed to collect the number of scripts more or less
than the predefined number of scripts to be collected for each
candidate, ‘Zero’ script is not allowed.</p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall be allowed to collect scripts at different times
even after the end of the exam.</mark></p>
</blockquote></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="header">
<th>Invi App</th>
<th>20</th>
<th>13.1.8</th>
<th>Invigilator Report (applicable to Classroom Invigilator)</th>
<th><ol type="1">
<li><blockquote>
<p>Dashboard shall have the Report section which includes the following
functions. It shall display alerts if discrepancy found, not completed
sessional report and seating plan uploaded.</p>
</blockquote>
<ul>
<li><blockquote>
<p>Summary Report</p>
</blockquote></li>
<li><blockquote>
<p>Discrepancy Report</p>
</blockquote></li>
<li><blockquote>
<p>Sessional Report</p>
</blockquote></li>
<li><blockquote>
<p>Seating Plan</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Summary Report</p>
</blockquote>
<ul>
<li><blockquote>
<p>Users shall be able to view the following information.</p>
</blockquote></li>
</ul></li>
</ol>
<blockquote>
<p>For Allocated Candidate</p>
</blockquote>
<ul>
<li><blockquote>
<p>Number of candidates in exam centre</p>
</blockquote></li>
<li><blockquote>
<p>Number of candidates who are present</p>
</blockquote></li>
<li><blockquote>
<p>Number of candidates who are absent</p>
</blockquote></li>
<li><blockquote>
<p>Missing attendance record(s)</p>
</blockquote></li>
<li><blockquote>
<p>Number of answer scripts collected</p>
</blockquote></li>
</ul>
<ul>
<li><blockquote>
<p>For Special Case</p>
</blockquote>
<ul>
<li><blockquote>
<p>Number of candidates of special case</p>
</blockquote></li>
<li><blockquote>
<p>Number of answer scripts collected from special case</p>
</blockquote></li>
</ul></li>
</ul>
<ol start="3" type="1">
<li><blockquote>
<p>Discrepancy Report</p>
</blockquote>
<ul>
<li><blockquote>
<p>Users shall be able to view the full list of candidates having
discrepancy records with the types of discrepancies.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to filter a specific list of candidates involved
in the corresponding nature. Number of candidates involved in different
nature shall also be displayed.</p>
</blockquote>
<ul>
<li><blockquote>
<p>Missing attendance record(s)</p>
</blockquote></li>
<li><blockquote>
<p>Missing attendance but with script collected</p>
</blockquote></li>
<li><blockquote>
<p>Missing script record(s)</p>
</blockquote></li>
<li><blockquote>
<p>Absent but with script(s) collected</p>
</blockquote></li>
<li><blockquote>
<p>Special case without script collected</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Users shall be able to edit the attendance status, spare barcode
assigned (if applicable) and the number of scripts collected by clicking
on the candidate records for the both allocated and special case
candidates.</p>
</blockquote></li>
<li><blockquote>
<p>For those candidates involved in script discrepancy, users shall be
required to input reason by selecting one of the following options
through the radio buttons and then input the corresponding
information:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Option 1: Candidate has been approved to use other answering
methods.</p>
</blockquote></li>
<li><blockquote>
<p>Option 2: Others: (Please input the special situation in remarks), a
text box shall be provided for the user to input.</p>
</blockquote></li>
</ul></li>
</ul></li>
</ol>
<ol start="0" type="1">
<li><blockquote>
<p>Sessional Report</p>
</blockquote>
<ul>
<li><blockquote>
<p>Users shall be able to edit, save, preview, confirm, submit and
re-submit the Sessional Report to the CS before the CS first confirms
the exam data to VCC. The fields shall include:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Actual Starting Time and Finishing Time under each zone name which
are retrieved from the system automatically, users shall be able to
adjust in necessary</p>
</blockquote></li>
<li><blockquote>
<p>Packages of question paper received</p>
</blockquote></li>
<li><blockquote>
<p>Exam Irregularities for candidates</p>
</blockquote></li>
<li><blockquote>
<p>Exam Irregularities for invigilators</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p><mark>Different subject papers of the candidates shall be listed
under each zone in the Sessional Report.</mark></p>
</blockquote></li>
<li><blockquote>
<p>'Not yet recorded’ shall be displayed if there is no record in
Packages of question paper received, Exam Irregularities (Candidates)
and Exam Irregularities (Invigilators).</p>
</blockquote></li>
<li><blockquote>
<p>System shall display the Discrepancy Report with types of
discrepancies and candidate information if there is any discrepancy when
users clicked the ‘Submit to Classroom CS’ button in the preview page of
the Sessional Report.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to correct the attendance status, spare barcode
used and the number of scripts collected by clicking on the records
shown in the discrepancy report.</p>
</blockquote></li>
<li><blockquote>
<p>For those reasons of script discrepancy, it shall be preloaded to the
remarks. Besides, users shall be able to input additional remarks in
free text format if there is a discrepancy when submitting the Sessional
Report to the CS.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to edit and submit the Sessional Report
iteratively before the CS first confirms the exam data to VCC.</p>
</blockquote></li>
<li><blockquote>
<p>The App shall prompt an alert to remind users to submit Sessional
Report again if the attendance / script data was changed after previous
submission. Related alerts shall also be prompted at the CS Module.</p>
</blockquote></li>
</ul></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>Invi App</th>
<th>26</th>
<th>13.1.9</th>
<th>Seating Plan (applicable to Classroom Invigilator)</th>
<th><ol type="1">
<li><blockquote>
<p><mark>Users shall be able to take the photo from hardcopy of the
candidate seating plan form and</mark> upload the image through the App
<mark>at any time.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall be able to</mark> preview the candidate seating
<mark>at any time after the seating plan was uploaded.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall be able to use the function by tapping the ‘Seating
Plan’ section under the ‘Reports’. The system shall display an alert if
no seating plan is uploaded.</mark></p>
</blockquote></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="header">
<th>Invi App</th>
<th>27</th>
<th>13.1.10</th>
<th>Timer</th>
<th><ol type="1">
<li><blockquote>
<p>Under each zone listed on the ‘Assign Zone’ page, the scheduled exam
time (with start time and end time) and supervised break(s) (with start
time and end time) in accordance with the timetable of candidates shall
be displayed to the invigilators automatically and initially.</p>
</blockquote></li>
<li><blockquote>
<p>Timetable information of each candidate such as case number, break
information, special needs in remarks, etc. shall be provided by the SEN
system of HKEAA.</p>
</blockquote></li>
<li><blockquote>
<p>Hall Invigilator:</p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>The system shall update and display the actual start and end
times of the exam as well as those of the supervised break(s) under each
zone automatically after the CS</mark> edited <mark>the actual exam
start time on the CS panel(see CS Module).</mark></p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Classroom Invigilator:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Users shall only be able to edit <mark>the actual exam start time of
each zone. The system shall then update and display the start and end
times of the exam session as well as those of the supervised break(s)
under each zone accordingly.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall not be able to edit the actual exam start time of
Paper 1 earlier than the regular designated time (i.e.
8:30am).</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>The adjustment of time(s) in Paper 1 shall not affect the
scheduled exam start time of Paper 2 which is provided by the system in
default. On the other hand, the users shall be allowed to edit the
actual exam start time of Paper 2.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>The actual exam start time of Paper 1 and Paper 2 in the SEN
exam centre shall not be earlier than those in the normal
centre.</mark></p>
</blockquote></li>
<li><blockquote>
<p>The actual exam start time and end time fields of each zone in the
sessional report shall be updated based on the timer set.</p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall be able to check the exam end time in the routine
page, see UF-SEN-011 Routine.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>By tapping the ‘Rem</mark>ove all supervised break(s)’ and a
‘Confirm to remove all supervised break(s)’ button on the page of the
candidate list within the zone for a single candidate room, users shall
be able to remove the time settings of all scheduled supervised break(s)
at once. Validation shall be set to ensure that it is a single candidate
room before removal. The system shall then update and display the start
and end times of the exam (including the routine) automatically. A
message about the removal of supervised break(s) shall also be
highlighted.</p>
</blockquote></li>
<li><blockquote>
<p>Provide the no. of candidate to be allocated by zones under the
'Assign Zone' page &gt; Zone A (5 candidates)</p>
</blockquote></li>
</ul></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>Invi App</th>
<th>28</th>
<th>13.1.11</th>
<th>Routine</th>
<th><ol type="1">
<li><blockquote>
<p>Users shall be able to read the routine of the exam session by
tapping the [Routine] button in the page of the Assign Zone.</p>
</blockquote></li>
<li><blockquote>
<p>Each action occurring within the exam timeline of each assigned zone
shall be listed by time sequence.</p>
</blockquote>
<ol type="a">
<li><blockquote>
<p>The start and end time of the exam paper</p>
</blockquote></li>
<li><blockquote>
<p>The start and end time of all supervised breaks</p>
</blockquote></li>
<li><blockquote>
<p>The last 15 minutes and 5 minutes before exam end</p>
</blockquote></li>
</ol></li>
</ol>
<ol type="1">
<li><blockquote>
<p>The actions of the new zone created for the special case (wrong
centre candidate) shall be included in the exam timeline as well.</p>
</blockquote></li>
<li><blockquote>
<p>The system shall be able to display the effective times of the exam
automatically if the CS/invigilator adjusted the exam start time and/or
the supervised break(s) is/are removed for a single candidate room.</p>
</blockquote></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="header">
<th>Invi App</th>
<th>31</th>
<th>13.1.12</th>
<th>Message Board</th>
<th><ol type="1">
<li><blockquote>
<p>Users shall be able to communicate with and receive notification from
the CS through the Message Board.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to receive, be notified and read one-way messages
/ information disseminated from HKEAA.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to send/receive messages and <mark>images /
audios / videos</mark> to/from the CS of the checked-in exam
sessions.</p>
</blockquote></li>
<li><blockquote>
<p>VCC Manager and Officer role users shall be able to extract the
conversation logs.</p>
</blockquote></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>CS</th>
<th>31</th>
<th>13.2.1</th>
<th>SEN CS Login</th>
<th><ol type="1">
<li><blockquote>
<p>By selecting the Examination Date and SEN Centres, choosing the exam
centre, entering the EP Number, and Password, the assigned CS shall be
able to login to the SEN CS Module.</p>
</blockquote></li>
<li><blockquote>
<p>CS’s EP No. shall be used to recognize the specific exam session of
the SEN exam centre that the CS is responsible for.</p>
</blockquote></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="header">
<th>CS</th>
<th>32</th>
<th>13.2.2</th>
<th>Navigation Bar</th>
<th><ol type="1">
<li><blockquote>
<p>For Hall centres</p>
</blockquote>
<ul>
<li><blockquote>
<p>Users shall be able to click the ‘green QR code’ icon to prompt a
window that shows the QR code for invigilator to login ‘i-Invigilation
(HKDSE)’ (Invigilator App).</p>
</blockquote></li>
<li><blockquote>
<p>‘Pending Confirmation’ button shall be used for confirmation or
reconfirmation of the exam data sent to VCC (applicable to Hall CS).</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Users shall be able to click the [中文]/[ENG] button to switch the
language to either English or Chinese.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to click the ‘Selection of Subject/Paper’ button
to switch to another exam session, a message shall be displayed to
remind the users to confirm the exam data before switching to another
exam session.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to click the ‘Reports’ button to select the
shortcut link to Sessional Report, Discrepancy Report and Summary
Report.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall click the ‘Logout’ button to logout the SEN CS Module, a
message shall be displayed to reminder the users to confirm the exam
data before log out</p>
</blockquote></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>CS</th>
<th>33</th>
<th>13.2.3</th>
<th>Exam Information</th>
<th><ol type="1">
<li><blockquote>
<p><mark>On every page of the App, users shall be able to view the basic
examination information which are retrieved from HKEAA system by
scheduled synchronized job:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Exam name(e.g. DSE 2023)</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Exam centre code with the centre name</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Exam date</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>The step instructions to remind the CS to submit the Sessional
Report(s) and confirm the exam data.</mark></p>
</blockquote></li>
</ul></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="header">
<th>CS</th>
<th>33</th>
<th>13.2.4</th>
<th>Exam Time</th>
<th><ol type="1">
<li><blockquote>
<p><mark>On every page of the App,</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>The system shall display the scheduled exam time of both Paper
1 and 2 of the normal centre which is retrieved from the HKEAA
system.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>The start time of Paper 2 of different subjects on the exam
date at the normal centre within the message shown as below (i.e. “( )”
refers to scheduled start time of Paper 2 in the normal centre),
e.g.:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Note: All candidates of SEN Centres should return to exam rooms
before the exam start time of Paper 2 (i.e. <em>11:15</em> ) in normal
exam centres.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>注意：所有特別試場考生必須於一般試場卷二開考時間 (即
<em>11:15</em>) 前返回考室。</mark></p>
</blockquote></li>
</ul></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>CS</th>
<th>34</th>
<th>13.2.5</th>
<th>Login Code for Using Invigilator App</th>
<th><ol type="1">
<li><blockquote>
<p>For the hall invigilators who have been assigned to the exam session,
they shall be able to login the Invigilator App by scanning the QR code
of the exam session provided by the hall CS.</p>
</blockquote></li>
<li><blockquote>
<p>For ad hoc invigilators who have not been assigned to any exam
session yet, CS shall be able to generate a specific QR code for the
invigilator by entering invigilator’s English name. School Name and Code
of the schools where the invigilators come from shall be mandatorily
selected from the drop-down list:</p>
</blockquote>
<ul>
<li><blockquote>
<p>The drop-down list with all school names and codes shall be displayed
at the field for users to select if no character(s) is inputted.</p>
</blockquote></li>
<li><blockquote>
<p>By inputting character(s), corresponding school name(s) and code(s)
shall be displayed in the drop-down list at the field for users to
select.</p>
</blockquote></li>
<li><blockquote>
<p>The system shall create a unique account number for the
invigilator.</p>
</blockquote></li>
</ul></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="header">
<th>CS</th>
<th>35</th>
<th>13.2.6</th>
<th>CS Dashboard</th>
<th><ol type="1">
<li><blockquote>
<p><mark>Users shall have an overview of the real-time information of
the assigned exam centre(s) via the Dashboard page.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Hall CS Dashboard:</mark></p>
</blockquote></li>
</ol>
<ul>
<li><blockquote>
<p><mark>A summary of attendance records (‘Attendance Record’) shall
display the following number of candidates:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Present</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Absent</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Wrong Centre / Version Candidate(S)</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Attendance not taken</mark></p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p><mark>A pie chart of an overall situation shall reflect the counts
relating to attendance and collected script records.</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>By mouse hovering each sector of the chart, the figure and
percentage of the count shall be displayed.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>The figure of the counts shall be displayed at the
legend:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Present Candidate(s) with scripts collected</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Absent Candidate(s) without scripts collected</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Wrong Centre / Version Candidate(s) with scripts
collected</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Discrepancies</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>By clicking the sector, the following counts shall be shown on
a dialog box:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Attendance not taken without script(s) collected</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Attendance not taken with script(s) collected</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Present with missing script(s)</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Absent with script(s) collected</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Wrong Centre / Version candidates without script(s)
collected</mark></p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p><mark>By clicking each count in the dialog box, the users shall be
redirected to the corresponding page of ‘Discrepancy Report’.</mark></p>
</blockquote></li>
</ul></li>
</ul></li>
</ul></li>
<li><blockquote>
<p><mark>A pie chart of SR Form Status (‘Irregularities’) shall reflect
the number of corresponding SR Form Cases.</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>By mouse hovering each sector of the chart, the figure and
percentage of the count shall be displayed.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>The figure of the counts shall be displayed at the
legend:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>SR Form Cases with &lt;Completed&gt; status</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>SR Form Cases with &lt;Pending to Complete&gt;
status</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>By clicking the pie of SR Form Cases with &lt;Completed&gt;
Status, the users shall be redirected to the corresponding page of
‘Special Report for follow Up (Candidate)’ showing the completed cases
of the SR Forms.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>By clicking the pie of SR Form Cases with &lt;Pending to
Complete&gt; Status, the users shall be redirected to the corresponding
page of ‘Special Report for follow up (Candidate)’ showing the
outstanding cases of the SR Forms.</mark></p>
</blockquote></li>
</ul></li>
</ul></li>
</ul></li>
</ul>
<ol start="3" type="1">
<li><blockquote>
<p><mark>Classroom CS Dashboard:</mark></p>
</blockquote></li>
</ol>
<ul>
<li><blockquote>
<p><mark>A bar chart of an overall situation shall reflect the counts
relating to attendance and collected script records, at each bar which
represents a Classroom centre.</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>By mouse hovering each section of the bar of a classroom
centre, the counts for Classroom centre(s) (‘Classrooms Situation’)
shall be displayed:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Present Candidate(s) with scripts collected</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Absent Candidate(s) without scripts collected</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Wrong Centre / Version Candidate(s) with scripts
collected</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Discrepancies</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>By clicking the section, the Classroom centre code and the
following counts shall be shown on a dialog box:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Attendance not taken without script(s) collected</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Attendance not taken with script(s) collected</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Present with missing script(s)</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Absent with script(s) collected</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Wrong Centre / Version candidates without script(s)
collected</mark></p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p><mark>By clicking each count in the dialog box, the users shall be
redirected to the corresponding page of ‘Discrepancy Report’ under such
Classroom centre.</mark></p>
</blockquote></li>
</ul></li>
</ul></li>
<li><blockquote>
<p><mark>The following figure and the percentage of the attendance
records shall be displayed as well:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Present</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Absent</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Wrong Centre/Version Candidate(s)</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Attendance not taken</mark></p>
</blockquote></li>
</ul></li>
</ul></li>
<li><blockquote>
<p><mark>A bar chart of SR Form Status (‘Irregularities’) shall reflect
the number of corresponding SR Form Cases at each bar which represents a
Classroom centre.</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>By mouse hovering each section of the bar, the figure and
percentage of the count shall be displayed.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>The counts for both Classroom centre(s):</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>SR Form Cases with &lt;Completed&gt; status</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>SR Form Cases with &lt;Pending to Complete&gt;
status</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>By clicking the section of SR Form Cases with &lt;Completed&gt;
Status of the bar of a classroom centre, the users shall be redirected
to the corresponding page of ‘Special Report for follow up (Candidate)’
showing the completed cases of the SR Forms.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>By clicking the section of SR Form Cases with &lt;Pending to
Complete&gt; Status of the bar of a classroom centre, the users shall be
redirected to the corresponding page of ‘Special Report for follow Up
(Candidate)’ showing the outstanding cases of the SR Forms.</mark></p>
</blockquote></li>
</ul></li>
</ul></li>
</ul></li>
</ul></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>CS</th>
<th>40</th>
<th>13.2.7</th>
<th>Attendance and Script Records</th>
<th><ol type="1">
<li><blockquote>
<p><mark>Users shall be able to view the candidate’s attendance and
script records of the SEN exam centre.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall be able to filter the records by
selecting:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Attendance status (i.e. present or absent)</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Status of script collection (i.e. collected scripts and missing
script)</mark></p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Users shall be able to sort the records by clicking the corresponding
field names.</p>
</blockquote></li>
<li><blockquote>
<p><mark>The system shall list and group the candidate records under
zones having different timetables. Each zone shall consist of candidate
records of different subjects having the same timetable. Heading of each
zone shall be shown with its zone name, scheduled exam start and end
time, exam duration(including break), and supervised break(s) when mouse
hovering the ‘View Break Time’ icon.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>The system shall display candidate records with the following
fields:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Candidate number or identification document number</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Candidate name</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Case number</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Seat number</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Subject name</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Paper code</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Attendance status（'--' means attendance not yet taken, present
and absent)</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Answer script collected / answer script to be
collected</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Remarks of individual candidate’s timetable (if any) provided
by HKEAA</mark></p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p><mark>For the case number, the length ranges from 11 to 12 characters
depending on the trailing numbers followed by the disabilities code,
e.g. DSE2021A001 and DSE2021A0001. The format shall be expressed in the
following examples:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>DSE2021A001. “A” means aural disabilities</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>DSE2021V001. “V” means visual disabilities</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>DSE2021O001. “O” means oral disabilities</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>DSE2021L001. “L” means specific learning
disabilities</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>DSE2021P001. “P” means physical disabilities</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>DSE2021X001. “X” means other disabilities (e.g. Autism Spectrum
Disorder (ASD), Attention-Deficit/Hyperactivity Disorder (AD/HD),
intellectual disabilities (ID), disorder related to mental health,
chronic medical illnesses, etc)</mark></p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p><mark>Users shall be able to click the ‘View’ button to read the
candidate’s information. Following shall be displayed:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Candidate name and the candidate number as the title of the
popup window.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Document No.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Invigilator’s Attendance Taking Time</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Self Check-in Time</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>No. of Scripts Collected</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Spare Barcode</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>SR1 Case Records, such as photo not resemble candidate,
admission form not present and cannot verify identity</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Check-in/out (Toilet request)</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Candidate photo in REG</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Remarks of the candidate provided by HKEAA that shall be able
to display symbols and wordings in Chinese and English at the same
time.</mark></p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p><mark>A search bar shall enable the Classroom CS to filter the
classroom.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall be able to edit the candidate’s attendance and
scripts collected information in the edit form by clicking the ‘Edit’
button. The edit page shall display the candidate no, candidate name,
seat number and the remarks retrieved from the timetable. Users shall be
able to edit the followings:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Attendance status (i.e. ‘Yes’ - present or ‘No’ -
absent)</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Usage of spare barcode (i.e. Yes or No) and the spare barcode
number if ‘Yes is selected’, users shall be able to select the subject
code from a dropdown list and enter the last 5 digits. A message shall
be popped up if the combination of the subject code and the last 5
digits are incorrect (applicable to Hall CS only, for classroom centres,
assigning spare barcode is the duty of the Classroom
invigilators)</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Number of scripts collected, for those candidates involved in
script discrepancy, users shall be required to input reason by selecting
one of the following options through the radio buttons and then input
the corresponding information:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Option 1: Candidate has been approved to use other answering
methods.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Option 2: Others: (Please input the special situation in
remarks), a text box shall be provided for the user to input.</mark></p>
</blockquote></li>
</ul></li>
</ul></li>
</ol>
<blockquote>
<p> </p>
</blockquote></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="header">
<th>CS</th>
<th>45</th>
<th>13.2.8</th>
<th>Timer</th>
<th><ol type="1">
<li><blockquote>
<p><mark>Timetables of the candidates shall be retrieved from and
updated to the SEN system of HKEAA.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall be able to access the timer function via the
‘Timer’ page.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>System shall list and group the exam times under zones having
different timetables. Heading of each zone shall be shown with its zone
name, scheduled exam start and end time, and exam duration(including
break).</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>System shall show the following times under each zone by time
sequence:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Exam start and end time</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Start time(s) and end time(s) of all the supervised
break(s)</mark></p>
</blockquote></li>
</ul></li>
</ol>
<blockquote>
<p> </p>
<p><mark><u>Hall CS</u></mark></p>
<p> </p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Users shall only be able to edit the actual exam start time of
each zone. Then, the system shall update and display the start and end
times of the exam session as well as those of the supervised break(s)
under each zone automatically.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>For the zone does not have any supervised break(s), ‘Supervised
Break : NA’ shall be displayed.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall not be able to edit the actual exam start time of
Paper 1 earlier than the regular designated time (i.e.
8:30am).</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>The adjustment of time(s) in Paper 1 shall not affect the
scheduled exam start time of Paper 2 which is provided by the system in
default. On the other hand, the users shall be allowed to edit the
actual exam start time of Paper 2.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>The actual exam start time of Paper 1 and Paper 2 in the SEN
exam centre shall not be earlier than those in the normal
centre.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall be able to apply the actual exam start time of each
zone by clicking the ‘Confirm’ button.</mark></p>
</blockquote></li>
</ul>
<blockquote>
<p> </p>
<p><mark><u>Classroom CS</u></mark></p>
<p> </p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>A search bar shall enable the Classroom CS to filter the
classroom.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Classroom CS shall be able to view the exam time of each zone
in a filtered classroom, with a heading showing the zone name, scheduled
exam start and end time and the exam duration(including
break).</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Followings shall be shown under the zone heading:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Actual exam start time set by the classroom
invigilator</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Exam end time adjusted by the system</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Start time(s) of supervised break time(s) adjusted by the
system</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>End times(s) of supervised break time(s) adjusted by the
system</mark></p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p><mark>Single Candidate Room:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Users shall be able to remove the time settings of all existing
supervised break(s) by clicking the ‘Remove All Supervised Break(s)’
button at once. Validation shall be set to ensure that it is a single
candidate room before removal.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>A message shall be popup to get the CS’s confirmation to remove
all supervised breaks when the ‘Remove All Supervised Break(s)’ button
is clicked.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>The system shall then update and display the exam start and end
times automatically. A message about the removal of supervised break(s)
shall also be highlighted.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>The adjustment of time(s) in Paper 1 shall not affect the
scheduled exam start time of Paper 2 which is provided by the system in
default. On the other hand, the classroom invigilators shall be allowed
to edit the actual exam start time of Paper 2.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>The actual exam start time of Paper 1 and Paper 2 in the SEN
exam centre shall not be earlier than those in the normal
centre.</mark></p>
</blockquote></li>
</ul></li>
</ul>
<blockquote>
<p> </p>
</blockquote></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>CS</th>
<th>48</th>
<th>13.2.9</th>
<th>Maintain Special Cases</th>
<th><ol type="1">
<li><blockquote>
<p><mark>Users shall be able to maintain the special cases (wrong centre
candidates) in the Special Case page.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall be able to view the Special Case list with the
following fields:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Candidate Number</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Candidate name or identification document number</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Classroom centre code (applicable to Classroom CS)</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Zone name and the SEN exam time, e.g. A (SEN Exam Time 8:30 -
10:15)</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Spare barcode number</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Answer script collected / answer script to be
collected</mark></p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p><mark>Users shall be able to create special case(s) (wrong centre
candidates) by clicking the ‘Add’ button. Hall CS shall assign the
case(s) to the existing zone by selecting from a dropdown list while
Classroom CS shall assign the case(s) to the existing classroom centre
and zone.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>By clicking the ‘+’ icon next to the drop down list of
Zone,</mark> users shall be able to create new zone(s) in the existing
exam centre and assign the wrong centre candidate(s) to it., Followings
shall be specified to the new zone:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Subject</p>
</blockquote></li>
<li><blockquote>
<p>Paper</p>
</blockquote></li>
<li><blockquote>
<p>Invigilator</p>
</blockquote></li>
<li><blockquote>
<p>Exam start and end time</p>
</blockquote></li>
<li><blockquote>
<p>The time of supervised break(s) - they are optional and applicable to
the exam lasting 90 minutes or more. Users shall be able to add and
remove the supervised break time by clicking the ‘+’ and ‘-’ icon
respectively.</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p><mark>If a new zone is created and an invigilator is assigned to it
in an existing classroom centre, the information shall be reflected on
the pages of the ‘Invigilator Assignment’, the ‘Seating Plan’ and
Sessional Report.</mark></p>
</blockquote></li>
</ol>
<blockquote>
<p><mark> </mark></p>
</blockquote>
<ol start="6" type="1">
<li><blockquote>
<p><mark>Hall CS shall be able to update the candidate’s personal
information, spare barcode information, the number of collected scripts
and the zone assigned of each special case in the form by clicking the
‘Edit’ button. Classroom CS shall be able to update the classroom centre
assigned additionally.</mark><a href="about:blank"><u>[1]</u></a> <a
href="about:blank"><u>[2]</u></a> </p>
</blockquote></li>
<li><blockquote>
<p><mark>For those candidates involved in script discrepancy, users
shall be required to input reason by selecting one of the following
options through the radio buttons and then input the corresponding
information:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Option 1: Candidate has been approved to use other answering
methods.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Option 2: Others: (Please input the special situation in
remarks), a text box shall be provided for the user to input.</mark></p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p><mark>Users shall be able to remove special case(s) from the list by
clicking the ‘Remove’ button and confirming the action.</mark></p>
</blockquote></li>
</ol>
<blockquote>
<p> </p>
</blockquote></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="header">
<th>CS</th>
<th>56</th>
<th>13.2.10</th>
<th>Classroom List (applicable for Classroom CS)</th>
<th><ol type="1">
<li><blockquote>
<p><mark>The list shall be able to show all the classroom centres
with:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Classroom centre code</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Number of assigned candidates</mark></p>
</blockquote></li>
<li><blockquote>
<p>Actual exam start and end time - in the format of hh:mn - hh:mn</p>
</blockquote></li>
<li><blockquote>
<p><mark>EP / application / account number and the name of
invigilator</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Present count, absent count, unverified count (attendance
record is not yet taken)</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Number of absent case but with scripts collected</mark></p>
</blockquote></li>
<li><blockquote>
<p>Wrong centre <mark>count</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Total number of script to be collected (i.e. the total number
of scripts need to be collected from the present assigned candidates and
the wrong centre candidates)</mark></p>
</blockquote></li>
<li><blockquote>
<p>Missing scripts (i.e. the total number of scripts not received from
the present assigned candidates and the wrong centre candidates)</p>
</blockquote></li>
<li><blockquote>
<p><mark>Scripts collected from present (i.e. the total number of
missing scripts of the present assigned candidates and the wrong centre
candidates)</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Submission status of the sessional reports by the classroom
invigilators to CS:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p>Pending submission - Sessional report not yet submitted</p>
</blockquote></li>
<li><blockquote>
<p>Submitted - Sessional report submitted without Classroom
invigilator’s remarks</p>
</blockquote></li>
<li><blockquote>
<p>Submitted with a yellow ‘Remark’ button - Sessional report submitted
with Classroom invigilator’s remark. Mouse over the button shall display
the remarks inputted by the CRIs.</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>After the Classroom Invigilator has submitted the Sessional Report,
the [View] button of the corresponding centre shall be enabled and users
shall be able to view it.</p>
</blockquote></li>
<li><blockquote>
<p>Submit Sessional Report - for classroom CS to submit the classroom’s
sessional report to VCC by selecting single / multiple / all
<mark>classroom centre(s) and clicking the [Submit Sessional Report]
button.</mark></p>
</blockquote></li>
<li><blockquote>
<p>Submitted time displayed after submission of sessional report to
VCC</p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall be able to confirm the exam data of the classroom
centres to VCC by clicking the [Confirm Exam Data] button.</mark></p>
</blockquote></li>
<li><blockquote>
<p>Confirmed time displayed after confirmation of exam data to VCC</p>
</blockquote></li>
<li><blockquote>
<p>After confirming the exam data to VCC, users shall be able to edit
the Sessional Report by clicking the [Edit] button of the classroom
centre.</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>The number of classrooms displayed in a page shall be 20.</p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall be able to select columns displayed by toggling the
‘Preferences’ button.</mark></p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to filter the classroom centres with / without
discrepancy records by selecting the exam centre status.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to filter the classroom centres which the
sessional reports have been submitted or pending to submit to VCC by
selecting the Sessional Report Submission Status.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to easily identify classroom centres with
problems with the indicator displayed in the system after the Classroom
invigilator has submitted the sessional report.</p>
</blockquote>
<ul>
<li><blockquote>
<p>Red vertical bar shall be shown at the row header to indicate there
is discrepancy</p>
</blockquote></li>
<li><blockquote>
<p>Green vertical bar shall be shown if the sessional report of the
classroom is normal, without discrepancy.</p>
</blockquote></li>
<li><blockquote>
<p>The indicators shall be triggered once the Classroom Invigilator
submitted the sessional report. By default, no indicator (colorless
vertical bar) is displayed.</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>After the Classroom CS submitted the Sessional Report to VCC but not
yet confirmed the exam data, if the Classroom Invigilator changes exam
data and resubmit the Sessional Report again, Classroom CS should
receive an alert to submit the Sessional Report to VCC again.</p>
</blockquote></li>
<li><blockquote>
<p>Classroom CS shall only be able to confirm the exam data after all
the sessional reports of the classroom centres are submitted to VCC.</p>
</blockquote></li>
<li><blockquote>
<p>Once the classroom CS confirmed the exam data, all the classroom
invigilators cannot edit the exam data (attendance status and script
collected) and the sessional reports.</p>
</blockquote></li>
<li><blockquote>
<p>Classroom CS shall be able to edit the sessional reports of the
classroom centre after first confirmation of the exam data or the
Classroom Invigilator of a classroom has been checked out before the
exam end time.</p>
</blockquote></li>
<li><blockquote>
<p>After editing the sessional reports, classroom CS shall be able to
submit them to VCC and confirm the exam data iteratively.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall submit all finalized sessional reports and confirm all
exam data to VCC within the designated period of time (i.e. defined as a
parameter at the Exam Support Backend (SEAD) Module) after the exam end
time of the last exam session among the classroom centres on the same
exam day.</p>
</blockquote>
<ul>
<li><blockquote>
<p>Classroom CS shall be able to input remarks if there is any
discrepancy when confirming the exam data.</p>
</blockquote></li>
</ul></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>CS</th>
<th>60</th>
<th>13.2.11</th>
<th>SEN Invigilator Assignment</th>
<th><ol type="1">
<li><blockquote>
<p><mark>Candidates with the same exam time shall be assigned to and
shown in a zone with their seat numbers, names and candidate numbers by
the system automatically based on their timetables. Heading of each zone
shall be shown with its zone name, and scheduled exam start and end
time.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>An exam centre shall be able to accommodate more than one
zone.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Pre-assignment of Invigilator (applicable to hall centres
only):</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Before the invigilators check-in the exam session, the CS shall
also be able to assign those invigilators based on the invigilator list
on the exam date. The corresponding row in the invigilator list and
initial assignments shall be displayed font colour in ‘Grey’.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>After the invigilators have been assigned, users shall be able
to perform the reassignment by clicking the ‘Edit’ button.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Once the assigned invigilators have checked in, the
corresponding row in the invigilator list and initial assignments shall
be turned the font colour in ‘Black’.</mark></p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p><mark>For Hall CS:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Users shall assign invigilators to individual zones with their
names and EP numbers/Application numbers by selecting the invigilators
from the dropdown list.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Single invigilator shall be allowed to be assigned to multiple
zones.</mark></p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p><mark>For Classroom CS:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Users shall be able to assign checked-in invigilators to
individual zones in a classroom centre with their names and EP numbers /
Application numbers by selecting the invigilators from the dropdown
list.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Single invigilator shall be allowed to be assigned to multiple
zones in a classroom centre.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Multiple invigilators shall be allowed to be assigned to a
single zone in a classroom centre by clicking the ‘+’ button at the
invigilator list.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Under certain circumstances (e.g. a single candidate room which
may not have the formal invigilator), users shall be able to assign
themselves as the invigilator to that classroom to perform invigilation
besides performing the duties of CS at the same time. In this case, the
CS shall not be forced logged out of the CS Module after they have
logged in the Invigilator App.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>A search bar shall enable the Classroom CS to filter the
classroom.</mark></p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p><mark>Users shall be able to add additional/wrong centre candidate(s)
to the zone by clicking the ‘+’ button at the candidate list.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall be able to view the assignment result after
applying the settings.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall be able to edit the assignment by clicking the
‘Edit’ button after applying the settings.</mark></p>
</blockquote></li>
<li><blockquote>
<p>Users shall be directed to the ‘Seating Plan’ page by clicking the
[Seating Plan] button.</p>
</blockquote></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="header">
<th>CS</th>
<th>65</th>
<th>13.2.12</th>
<th>Create SEN Seating Plan</th>
<th><ol type="1">
<li><blockquote>
<p><mark>Users shall be able to take photo of the candidate seating plan
or upload the image file of the candidate seating plan to the system at
any time by clicking the [Seating Plan] button on the ‘Invigilator
Assignment’ page, select the ‘Seating Plan’ or ‘Sessional Report’ under
the ‘Reports’ at the left side menu.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>A message shall be displayed if the seating plan has not been
uploaded when users submit the Sessional Report.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>The exam information including exam name, centre name, exam
date and scheduled exam time shall be displayed.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>The exam time, the EP number and name of the invigilators who
report duty and the candidates of each zone shall be
displayed.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall be able to upload the photo of the seating plan by
clicking the upload icon or take a photo using the laptop/tablet camera
by clicking the camera icon.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>After uploading/taking the photo of the seating plan, a
thumbnail shall be displayed to indicate the photo of the seating plan
has been uploaded to the system.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall be able to enlarge the image file by clicking on
the thumbnail.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall be able to remove and re-take/re-upload the photo
of the seating plan by clicking the [Edit] button.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>The name and EP number of the CS who takes/uploads the photo of
the seating plan and the date and time of photo taking/uploading shall
be displayed.</mark></p>
</blockquote></li>
<li><blockquote>
<p>For Classroom CS:</p>
</blockquote>
<ul>
<li><blockquote>
<p>A search bar shall enable the users to filter the classroom.</p>
</blockquote></li>
<li><blockquote>
<p>If the Classroom Invigilators uploaded the seating plan of the
classroom centres through their Invigilator App, a thumbnail, the EP
number, name of the Classroom Invigilator, the date and time of
uploading shall be displayed, Classroom CS shall be able to enlarge it
by clicking on the thumbnail.</p>
</blockquote></li>
</ul></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>CS</th>
<th>68</th>
<th>13.2.13</th>
<th>SEN Invigilator Check-in Status</th>
<th><ol type="1">
<li><blockquote>
<p><mark>Lists of invigilators shall be displayed with the following
fields under the ‘Invigilator Assignment and Check-in Status’
section:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Invigilator name</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>EP number/Application number/account number for ad hoc
invigilator</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Check-in time</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Check-out time</mark></p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p><mark>The following lists shall be included:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>A list of invigilators who have checked-in/reported for
duty</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>A list of invigilators who have checked-out</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>A list of invigilators who did not check in</mark></p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p><mark>Users shall be able to update the attendance status of
invigilators via a ‘Check-out’ button.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>The check-in status and check-out time of the invigilators
concerned shall then be updated accordingly.</mark></p>
</blockquote></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="header">
<th>CS</th>
<th>69</th>
<th>13.2.14</th>
<th>Sessional Report</th>
<th><ol type="1">
<li><blockquote>
<p><mark>Users shall be able to preview, edit and submit the Sessional
Report of the SEN exam centres to VCC.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Following fields shall be displayed in a Sessional
Report:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Exam centre number</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Exam centre name</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Exam date</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Actual exam start time and end time of each zone
(editable)</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Different subject names and paper codes shall be listed under
each zone, including the new created zone</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Packet of exam paper received (editable)</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Number of scripts collected (editable)</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Candidates with script discrepancy - a list of candidate
numbers and name who involves script discrepancy</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Invigilators number and name who involves Special Report on
irregularity</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Candidate number and name who involves Special Report on
irregularity</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Reception mode - applicable to listening test</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Reception quality - applicable to listening test</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>[Seating Plan] button - users shall be directed to the Seating
Plan page by clicking this button.</mark></p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>For Hall CS:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Users shall send the sessional report to an invigilator for
confirmation.</p>
</blockquote></li>
<li><blockquote>
<p>A message shall be displayed if the seating plan has not been
uploaded when submitting the Sessional Report.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall submit the finalized sessional report to VCC within the
designated period of time (i.e. defined as a parameter at the Exam
Support Backend (SEAD) Module) after the exam end time of the last exam
session on the same exam day.</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p><mark>For Classroom CS:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>A search bar shall enable the Classroom CS to filter the
classroom.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>A message shall be displayed if the seating plan</mark> has
<mark>not been uploaded in any classroom centre when submitting the
Sessional Reports.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall also be able to preview and submit the Sessional
Reports of all the classrooms (individual selection, multiple selection
and select all records shall be enabled) to VCC through the classroom
list additionally.</mark></p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to re-edit and re-submit the sessional report
after its first exam data confirmation when there are any exam data
changes.<a href="about:blank"><u>[1]</u></a> <a
href="about:blank"><u>[2]</u></a> </p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall submit all finalized sessional reports to VCC
within the designated period of time (i.e. defined as a parameter at the
Exam Support Backend (SEAD) Module) after the exam end time of the last
exam session among the classroom centres on the same exam
day.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall also be able to view the Summary of Sessional
Report for all classroom centres. Searching and sorting of records shall
be p</mark>rovided. <mark>The following fields of sessional report shall
be displayed in the Summary and the users shall be able to view the
corresponding report by clicking the ‘View’ button:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Centre Code</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Actual Starting Time</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Broadcast Finishing Time (i.e. applicable to listening
test)</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Actual Finishing Time</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Number of Packets of Question Paper Received</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Number of Scripts Collected of Present Candidates</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Number of IRR of Candidates</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Number of IRR of Invigilators</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Reception Mode (i.e. applicable to listening test)</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Reception Quality (i.e. applicable to listening
test)</mark></p>
</blockquote></li>
</ul></li>
</ul></li>
</ol>
<blockquote>
<p> </p>
</blockquote></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>CS</th>
<th>75</th>
<th>13.2.15</th>
<th>Discrepancy Report</th>
<th><ol type="1">
<li><blockquote>
<p><mark>Users shall be able to view the discrepancy report grouped by
the zones in the SEN exam centre.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Heading of each zone shall be shown with its zone name,
scheduled exam start and end time, and exam duration. Each record shall
be shown with the following fields:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Candidate Type (i.e. Allocated or Special Case
Candidates)</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Candidate number or identification document number</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Candidate name</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Seat Number</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Subject name</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Paper code</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Spare barcode number (if any)</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Remarks (i.e. types of discrepancies)</mark></p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p><mark>4 types of discrepancy shall be shown with filtering
function:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p>Missing attendance record(s)</p>
</blockquote></li>
<li><blockquote>
<p>Missing attendance with script collected</p>
</blockquote></li>
<li><blockquote>
<p>Missing script record(s) - for those candidates with script
discrepancy but with reason provided should not be counted</p>
</blockquote></li>
<li><blockquote>
<p>Absent with script collected</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Searching and sorting of records shall be provided.</p>
</blockquote></li>
<li><blockquote>
<p><mark>For Hall CS, users shall be able to select discrepancy reports
on all candidates, allocated candidates and special case candidates in
the assigned exam centre through the tabs.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>A search bar shall enable the Classroom CS to filter the
classroom.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall be able to edit the exam data of the candidates to
clear the discrepancies by clicking the ‘Edit’ button. Candidate number,
candidate name shall be displayed and followings shall be
edited:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Attendance status (i.e. ‘Yes’ - present or ‘No’ -
absent)</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Usage of spare barcode (i.e. Yes or No) and the spare barcode
number if ‘Yes’ is selected. Users shall be able to select the subject
code from a dropdown list and input the last 5 digits. A message shall
be popped up if the combination of the subject code and the last 5
digits are incorrect (applicable to Hall exam Centre).</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Number of scripts collected, for those candidates involved in
script discrepancy, users shall be required to input reason by selecting
one of the following options through the radio buttons and then input
the corresponding information:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Option 1: Candidate has been approved to use other answering
methods.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Option 2: Others: (Please input the special situation in
remarks), a text box shall be provided for the user to input.</mark></p>
</blockquote></li>
</ul></li>
</ul></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="header">
<th>CS</th>
<th>78</th>
<th>13.2.16</th>
<th>Summary Report</th>
<th><ol type="1">
<li><blockquote>
<p><mark>Users shall be able to view the summary report(s) with the
total count of the following information on allocated candidates and
special case candidates in an SEN exam centre(s):</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Centre Code (i.e. applicable to Classroom CS)</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Number of Allocated Candidates</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Present Count</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Number of answer scripts collected / Number of answer scripts
to be collected from Allocated Candidates</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Number of Special Case</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Number of answer scripts collected / Number of answer scripts
to be collected from Special Cases</mark></p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p><mark>By expanding the total count record of each SEN exam centre,
users shall also be able to view the summary report(s) on allocated
candidates and special case candidates that are grouped by the zones of
the exam centre. The information shall includes the
followings:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Zone Name</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Number of Allocated Candidates</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Present Count</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Number of answer scripts collected / Number of answer scripts
to be collected from Allocated Candidates</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Number of Special Case</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Number of answer scripts collected / Number of answer scripts
to be collected from Special Cases</mark></p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p><mark>Searching and sorting of records shall be provided.</mark></p>
</blockquote></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>CS</th>
<th>80</th>
<th>13.2.17</th>
<th>Irregularities (also refer to the functional specifications of SR
form)</th>
<th><ol type="1">
<li><blockquote>
<p><mark>Users shall be able to handle and view the irregularities (e.g.
screenshot events) of all the zones in the SEN exam centre.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>SR Forms Module shall be applied here (see details in SR Form
Module).</mark></p>
</blockquote></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="header">
<th>CS</th>
<th>82</th>
<th>13.2.18</th>
<th>Confirm Attendance and Collected Script Records</th>
<th><ol type="1">
<li><blockquote>
<p><mark>System shall display the confirmation status of an exam session
as ‘Pending Confirmation’ before users confirm the accuracy of the
attendance and collected script data of the exam session.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall be able to confirm the accuracy of the attendance
and collected script data of the exam session by clicking the ‘Pending
Confirmation’ button.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>System shall display the reason of the discrepancy records if
the user has input when submitting the Sessional Report which is pending
for clearance, e</mark>ither the ‘Candidate has been approved to use
other answering methods. Please input the actual number of answer
scripts collected.’ or the ‘Others’ with user input the special
situation.</p>
</blockquote></li>
<li><blockquote>
<p><mark>System shall update the confirmation status as ‘Confirmed’ with
a timestamp after the users confirm the accuracy of the attendance and
collected script data of the exam session.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall be able to re-confirm the exam data accuracy. As
such, a new ‘confirmed’ timestamp will be reflected in the CS and VCC
Exam Centre pages.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>An alert shall be prompted if the users attempt to log out
before confirming the exam data accuracy of the attendance and collected
script data.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall be able to receive a notification after HKEAA
confirmed the accuracy of the attendance and collected script records of
their responsible exam sessions.</mark></p>
</blockquote></li>
</ol>
<blockquote>
<p> </p>
<p><mark><u>For Classroom CS:</u></mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>After all the Classroom invigilators submitted the Sessional
Reports to the Classroom CS, the Classroom CS shall be able to submit
the Sessional Reports to VCC,, then the exam data shall be confirmed to
VCC by the Classroom CS through the Classroom List.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall be able to easily identify classroom centres with
problems through the indicator displayed in the list after the Classroom
invigilator has submitted the sessional report:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Red indicator shall be shown at the row header to indicate that
there is discrepancy.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Green indicator shall be shown at the row header to indicate
that there is no discrepancy.</mark></p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p><mark>Users shall be able to view the remarks of sessional reports
submitted by the CRIs through the ‘Remark’ button.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>After the Classroom invigilator submitted the Sessional Report
and the Classroom CS submitted the Sessional Report to VCC but not yet
confirm the exam data, if the Classroom invigilator changes exam data
and submit the Sessional Report again, Classroom CS shall receive alert
to submit the Sessional Report to VCC again.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Before the 1st time confirmation of the exam data by the
Classroom CS, Classroom invigilator shall be able to re-edit and
re-submit the Sessional Report. Classroom CS shall receive an alert if
the Classroom Invigilator changes the exam data.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall be able to single/multiple select and select all
records to submit the Sessional Reports through the checkbox(es) and
then click the ‘Submit Sessional Report’ button.</mark></p>
</blockquote></li>
<li><blockquote>
<p>[Confirm Exam Data] button shall be enabled for the users to confirm
exam data to VCC at once after the submission of all Sessional Reports
to VCC.</p>
</blockquote></li>
<li><blockquote>
<p>Classroom invigilators shall not be able to edit the exam data after
Classroom CS has confirmed the exam data.</p>
</blockquote></li>
<li><blockquote>
<p>The ‘Edit’ button shall be enabled for Classroom CS to edit the
Sessional Report after Classroom CS’s first time exam data confirmation
or a Classroom Invigilator has checked out before the exam end before
the exam data confirmation</p>
</blockquote></li>
<li><blockquote>
<p>Users shall submit all finalized sessional reports and confirm all
exam data to VCC within the designated period of time (i.e. defined as a
parameter at the Exam Support Backend (SEAD) Module) after the exam end
time of the last exam session among the classroom centres on the same
exam day.</p>
</blockquote></li>
</ul>
<blockquote>
<p> </p>
</blockquote></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>CS</th>
<th>84</th>
<th>13.2.19</th>
<th>M<mark>essage Board</mark></th>
<th><ol type="1">
<li><blockquote>
<p><mark>sers shall be able to retrieve, be notified and read messages
or information from HKEAA.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall be able to disseminate message/information from
HKEAA to one or selected invigilators who have checked-in their
responsible exam sessions.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall be able to exchange messages with VCC staff
instantly. Due to individual schools’ privacy, messaging between CSs of
different exam centres are restricted.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall be able to send messages and images / audios /
videos to the VCC users.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall be able to create invigilator groups and
communicate with particular groups of invigilators.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>System Administration shall be able to extract all the message
logs.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Users shall be able to disseminate the information to
individual/all invigilators directly.</mark></p>
</blockquote></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="header">
<th>CS</th>
<th>85</th>
<th>13.2.20</th>
<th>CS Instruction to Submit Sessional Report and Confirm Exam Data</th>
<th><ol type="1">
<li><blockquote>
<p><mark>There is an instruction in the box of the exam information to
guide the users to submit the Sessional Report and confirm the exam data
after the exam ended.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>For Hall CS:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Before the exam ends, steps of the Sessional Report submission
and the exam data confirmation shall be displayed.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>After the exam ends, the step number of the Sessional Report
submission shall become bigger to remind the user to submit the
sessional report.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>After the users submitted the sessional report, the step number
of the Sessional Report submission shall become a green tick, and the
step number of the exam data confirmation shall become
bigger.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>After users confirm the exam data confirmation, the step number
of the exam data confirmation shall become a green tick.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>If users edit the exam data after confirming the exam data, it
shall be back to point 2.2.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>These steps shall be iterated until both the step numbers
become green ticks that implies that the processes have been
finished.</mark></p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p><mark>For Classroom CS:</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Users need to submit the Sessional Reports of all the classroom
centres before confirming the exam data.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Before the exam ends, steps of the Receiving all classrooms’
Sessional Reports, Sessional Report submission to VCC and the exam data
confirmation shall be displayed.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>After the exam ended, the step number of Receiving all
classrooms’ Sessional Reports shall become bigger.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Until all the classrooms’ Sessional Reports have been received,
the step number of Receiving all classrooms’ Sessional Reports shall be
displayed as a green tick.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>Once all the classrooms’ Sessional Reports have been received,
the step number of Submit Sessional Reports to VCC shall become
bigger.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>After all the classrooms’ Sessional Reports have been submitted
to VCC, the step number of Submit Sessional Reports to VCC shall be
displayed as a green tick and the step number of exam data confirmation
shall become bigger.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>After users confirm the exam data, the step number of the exam
data confirmation shall become a green tick.</mark></p>
</blockquote></li>
<li><blockquote>
<p><mark>If users edit the exam data after confirmation, it should go
back to point 3.5 to remind the users to submit the Sessional Report to
VCC again.</mark></p>
</blockquote></li>
</ul></li>
</ol>
<blockquote>
<p> </p>
<p> </p>
</blockquote></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>VCC</th>
<th>90</th>
<th>13.3</th>
<th>General Requirement</th>
<th><ol type="1">
<li><blockquote>
<p>Data shown on the pages of Dashboard and Exam Centre is refreshed
automatically every 5 seconds throughout the exam session.</p>
</blockquote></li>
<li><blockquote>
<p>Records of Centres without any update on the attendance figures after
a designated period of time (i.e. specified as parameter at Exam Support
Backend (SEAD), e.g. 15 mins) from the scheduled exam start time shall
be floated on top and highlighted in ‘red’ colour in the tables (under
Exam Centres and Dashboard pages) automatically.</p>
</blockquote></li>
<li><blockquote>
<p>Roles of Manager, Officer and Operator are able to view both the hall
centres and classroom centres of an exam school.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to filter the exam data by selecting the criteria
listed below:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Operator - applicable to officer / manager role users</p>
</blockquote></li>
<li><blockquote>
<p>Exam date - default to system date</p>
</blockquote></li>
<li><blockquote>
<p>Centre type</p>
</blockquote></li>
<li><blockquote>
<p>Subject code-paper group - e.g. A020E-1, only provide the subject
papers of the selected exam date for user filtering</p>
</blockquote></li>
<li><blockquote>
<p>Subject name</p>
</blockquote></li>
<li><blockquote>
<p>Centre code</p>
</blockquote></li>
<li><blockquote>
<p>School code</p>
</blockquote></li>
<li><blockquote>
<p>School name</p>
</blockquote></li>
<li><blockquote>
<p>Scheduled exam end time (in the format of hh:mn, there are few exam
end time in the same exam session because of the supervised</p>
</blockquote></li>
<li><blockquote>
<p>CS logged in - Yes/No</p>
</blockquote></li>
<li><blockquote>
<p>Attendance/Scripts Discrepancy - Yes/No</p>
</blockquote>
<ul>
<li><blockquote>
<p>Yes - missing attendance + Missing script + absent with script &gt;
0</p>
</blockquote></li>
<li><blockquote>
<p>No - missing attendance + Missing script + absent with script = 0</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Sessional report submitted - Yes/No</p>
</blockquote></li>
<li><blockquote>
<p>Notified CS - Yes/No</p>
</blockquote>
<ul>
<li><blockquote>
<p>If the CS edited exam data after helpdesk/operator notification, it
should be considered as No.</p>
</blockquote></li>
</ul></li>
</ul></li>
<li><blockquote>
<p>For Subject name, Centre code, School code and School name, the
system shall filter and display relevant data in the dropdown list for
selection according to the character(s) entered by the users.</p>
</blockquote></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="header">
<th>VCC</th>
<th>92</th>
<th>13.3.1</th>
<th>Login</th>
<th><ol type="1">
<li><blockquote>
<p>Only allow VCC Manager, Officer, or Operator role with SEN permission
to view the SEN centre data, and they are restricted to access SEN exam
centres only.</p>
</blockquote></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>VCC</th>
<th>93</th>
<th>13.3.2</th>
<th>Dashboard</th>
<th><ol type="1">
<li><blockquote>
<p>An initial page of the Dashboard shall be displayed after the users
login to the VCC until the selection is made by filtering the event at
the left side menu.</p>
</blockquote></li>
<li><blockquote>
<p>The Dashboard page of a helpdesk/an operator shall display the
overviews of his/her assigned exam centes:</p>
</blockquote>
<ul>
<li><blockquote>
<p>A pie chart of an overview on the CSs Login status(‘CS Login
Status’):</p>
</blockquote>
<ul>
<li><blockquote>
<p>Yes - in blue color: once the CSs logged in the exam session in an
exam day</p>
</blockquote></li>
<li><blockquote>
<p>No - in pink color: CSs have not logged in yet in an exam session in
an exam day</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>A pie chart of an overview on the confirmation status(‘Overall
Submission Situation’):</p>
</blockquote>
<ul>
<li><blockquote>
<p>Pending to confirm - in gray color: the accuracy of the attendance
and collected script data is pending to be confirmed by CS</p>
</blockquote></li>
<li><blockquote>
<p>Confirmed without discrepancy - in green color:</p>
</blockquote>
<ul>
<li><blockquote>
<p>the accuracy of the attendance and collected script data was
confirmed by CS without any discrepancy</p>
</blockquote></li>
<li><blockquote>
<p>Missing attendance + missing script + absent with scripts + pending
special case (i.e. incomplete SR Forms) = 0</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Confirmed with pending special case - in yellow color:</p>
</blockquote>
<ul>
<li><blockquote>
<p>The accuracy of the attendance and collected script data was
confirmed by CS without any discrepancy but with the incomplete SR
Forms</p>
</blockquote></li>
<li><blockquote>
<p>Missing attendance + missing script + absent with scripts = 0 but
pending special case (i.e. incomplete SR Forms) &gt; 0</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Confirmed but with attendance and/or script discrepancy - in red
color:</p>
</blockquote>
<ul>
<li><blockquote>
<p>CS confirmed the accuracy of number of candidates present and the
number of scripts collected but with discrepancy</p>
</blockquote></li>
<li><blockquote>
<p>Missing attendance + missing script + absent with scripts &gt; 0</p>
</blockquote></li>
</ul></li>
</ul></li>
<li><blockquote>
<p>A pie chart showing overall the CSs have been notified by the
operator/helpdesk (‘Notified CS’)</p>
</blockquote>
<ul>
<li><blockquote>
<p>Yes - in cyan color: the notification has been sent to CSs</p>
</blockquote></li>
<li><blockquote>
<p>No - in brown color: the CSs have not been notified yet</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Mouseover the pie shall display the corresponding count number.</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>The Dashboard page of the officer/manager role users shall display
the overviews of the exam centres of all the helpdesks/operators are
responsible for:</p>
</blockquote>
<ul>
<li><blockquote>
<p>A bar chart showing the CSs Login status(‘CS Login Status by
Helpdesk’):</p>
</blockquote>
<ul>
<li><blockquote>
<p>Yes - in blue color: once the CSs logged in the exam session in an
exam day</p>
</blockquote></li>
<li><blockquote>
<p>No - in pink color: CSs have not logged in yet in an exam session in
an exam day</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>A bar chart showing overall discrepancy situation by
helpdesk/operator (‘Overall Submission Status by Helpdesk’)</p>
</blockquote>
<ul>
<li><blockquote>
<p>Pending to confirm - in gray color: the accuracy of the attendance
and collected script data is pending to be confirmed by CS</p>
</blockquote></li>
<li><blockquote>
<p>Confirmed without discrepancy - in green color:</p>
</blockquote>
<ul>
<li><blockquote>
<p>the accuracy of the attendance and collected script data was
confirmed by CS without any discrepancy</p>
</blockquote></li>
<li><blockquote>
<p>Missing attendance + missing script + absent with scripts + pending
special case (i.e. incomplete SR Forms) = 0</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Confirmed with pending special case - in yellow color:</p>
</blockquote>
<ul>
<li><blockquote>
<p>The accuracy of the attendance and collected script data was
confirmed by CS without any discrepancy but with the incomplete SR
Forms</p>
</blockquote></li>
<li><blockquote>
<p>Missing attendance + missing script + absent with scripts = 0 but
pending special case (i.e. incomplete SR Forms) &gt; 0</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Confirmed but with attendance and/or script discrepancy - in red
color:</p>
</blockquote>
<ul>
<li><blockquote>
<p>CS confirmed the accuracy of number of candidates present and the
number of scripts collected but with discrepancy</p>
</blockquote></li>
<li><blockquote>
<p>Missing attendance + missing script + absent with scripts &gt; 0</p>
</blockquote></li>
</ul></li>
</ul></li>
<li><blockquote>
<p>A bar chart showing the status that the CSs have been notified by the
helpdesk (‘Notified CS by Helpdesk’)</p>
</blockquote>
<ul>
<li><blockquote>
<p>Yes - in cyan color: the notification has been sent to CSs</p>
</blockquote></li>
<li><blockquote>
<p>No - in brown color: the CSs have not been notified yet</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Mouseover the bar shall display the corresponding count number.</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>For the result tables, users shall be able to select columns
displayed by toggling the ‘Preferences’ button.</p>
</blockquote></li>
<li><blockquote>
<p>In order to facilitate the operations of the users, the functions of
notifying CSs shall be provided in the Dashboard page.</p>
</blockquote></li>
<li><blockquote>
<p>Following fields shall be displayed in the result table as the exam
data summary according to the selection criteria of the filtering
events:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Operator - the login name of the helpdesk/operator, applicable to the
officer/manager role users</p>
</blockquote></li>
<li><blockquote>
<p>Centre supervisor Logged in at - Centre supervisor name with EP no.
and the post, and the time (hh:mm) of his/her logged in CS Module. E.g.
CHAN TIN NAM(10088-076 CS) 07:24; mouseover the centre supervisor name
shall popup the school telephone no. of the centre supervisor.</p>
</blockquote></li>
<li><blockquote>
<p>Subject code</p>
</blockquote></li>
<li><blockquote>
<p>Subject name</p>
</blockquote></li>
<li><blockquote>
<p>Paper group</p>
</blockquote></li>
<li><blockquote>
<p>Centre code</p>
</blockquote></li>
<li><blockquote>
<p>Centre type</p>
</blockquote></li>
<li><blockquote>
<p>School code; mouseover the school code shall popup the school name
and the address</p>
</blockquote></li>
<li><blockquote>
<p>Missing attendance - no. of candidates that the attendance record
have not been taken yet</p>
</blockquote></li>
<li><blockquote>
<p>Missing script - the total no. of missing scripts that should be
collected from the allocated candidates and the special case present at
the exam centre(except those moved to and at the special room).</p>
</blockquote></li>
<li><blockquote>
<p>Absent with script - rename of absent but with script collected</p>
</blockquote></li>
<li><blockquote>
<p>Remark from CS - remarks inputted by CS when confirming the exam data
accuracy. [View] button shall be displayed if there is a remark and show
‘Nil’ if CS has not input any remarks.</p>
</blockquote></li>
<li><blockquote>
<p>Pending SR Form case - no. of incompleted SR cases over no. of total
SR cases</p>
</blockquote></li>
<li><blockquote>
<p>Notification to CS - for confirming exam data accuracy, users shall
be able to single/multiple select the records or select the checkbox of
‘Select all to notify CS’ and click the [Notify Selected] button or
[Notify All] button, the notification(s) shall be sent to the related
CSs.</p>
</blockquote></li>
<li><blockquote>
<p>Action - popup menu for directing to the individual exam situation
page, message board and downloading message board history.</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>There are 4 types of indicators located at the row header to
facilitate the users to know the exam data confirmation status of the
exam centre after the 1st confirmation of the exam data by the CS.</p>
</blockquote></li>
</ol>
<ul>
<li><blockquote>
<p>Gray color bar - indicates the exam data confirmation status of the
exam centre is pending to confirm by CS</p>
</blockquote></li>
<li><blockquote>
<p>Green color bar - Confirmed without discrepancy:</p>
</blockquote>
<ul>
<li><blockquote>
<p>the accuracy of the attendance and collected script data was
confirmed by CS without any discrepancy</p>
</blockquote></li>
<li><blockquote>
<p>Missing attendance + missing script + absent with scripts + pending
special case (i.e. incomplete SR Forms) = 0</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Yellow color bar - Confirmed with pending special case:</p>
</blockquote>
<ul>
<li><blockquote>
<p>The accuracy of the attendance and collected script data was
confirmed by CS without any discrepancy but with the incomplete SR
Forms</p>
</blockquote></li>
<li><blockquote>
<p>Missing attendance + missing script + absent with scripts = 0 but
pending special case (i.e. incomplete SR Forms) &gt; 0</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Red color bar - Confirmed but with attendance and/or script
discrepancy:</p>
</blockquote>
<ul>
<li><blockquote>
<p>CS confirmed the accuracy of number of candidates present and the
number of scripts collected but with discrepancy</p>
</blockquote></li>
<li><blockquote>
<p>Missing attendance + missing script + absent with scripts &gt; 0</p>
</blockquote></li>
</ul></li>
</ul>
<ol start="8" type="1">
<li><blockquote>
<p>The ‘View Exam Detail’ in the ‘Actions’ column shall direct the VCC
manager / officer to the pages where he/she can:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Manager shall view and edit the attendance and script records of the
candidates and the officer shall view the data only.</p>
</blockquote></li>
<li><blockquote>
<p>View the candidate’s exam information during the exam, e.g. self
check-in time, invigilator’s attendance taking time, no. of scripts
collected, spare barcode, confirmation status of the special room exam
records, toilet request, and SR1 case records.</p>
</blockquote></li>
<li><blockquote>
<p>Manager shall view and edit the special case details and the officer
shall view the data only.</p>
</blockquote></li>
<li><blockquote>
<p>View the CS/deputy CS/invigilator’s check-in/out time and
assignment.</p>
</blockquote></li>
<li><blockquote>
<p>View the Sessional Report of the exam session after the exam data of
the exam centre has been confirmed.</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>For classroom centres, there is an additional item ‘Classroom
Summary’ in the ‘Actions’ column, users shall be able to view the
related figures of each classroom centre and the total number of
corresponding candidates (including both the assigned candidates and
special cases) who sit the exam in the classroom centres of an exam
school shall be shown.</p>
</blockquote></li>
</ol>
<blockquote>
<p> </p>
<p> </p>
<p> </p>
</blockquote></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="header">
<th>VCC</th>
<th>99</th>
<th>13.3.3</th>
<th>Display Examination Session Information (Exam Centres)</th>
<th><ol type="1">
<li><blockquote>
<p>Users shall be able to view a table with the real-time exam
information of all / designated exam centres via a ‘Exam Centres’
page.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to sort the tables by the field labels and select
the field labels through the ‘Preference’ button.</p>
</blockquote></li>
<li><blockquote>
<p>There are 4 types of indicators located at the row header to
facilitate the users to know the exam data confirmation status of the
exam centre after the 1st confirmation of the exam data by the CS.</p>
</blockquote></li>
</ol>
<ul>
<li><blockquote>
<p>Gray color bar - indicates the exam data confirmation status of the
exam centre is pending to confirm by CS</p>
</blockquote></li>
<li><blockquote>
<p>Green color bar - Confirmed without discrepancy:</p>
</blockquote>
<ul>
<li><blockquote>
<p>the accuracy of the attendance and collected script data was
confirmed by CS without any discrepancy</p>
</blockquote></li>
<li><blockquote>
<p>Missing attendance + missing script + absent with scripts + pending
special case (i.e. incomplete SR Forms) = 0</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Yellow color bar - Confirmed with pending special case:</p>
</blockquote>
<ul>
<li><blockquote>
<p>The accuracy of the attendance and collected script data was
confirmed by CS without any discrepancy but with the incomplete SR
Forms</p>
</blockquote></li>
<li><blockquote>
<p>Missing attendance + missing script + absent with scripts = 0 but
pending special case (i.e. incomplete SR Forms) &gt; 0</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Red color bar - Confirmed but with attendance and/or script
discrepancy:</p>
</blockquote>
<ul>
<li><blockquote>
<p>CS confirmed the accuracy of number of candidates present and the
number of scripts collected but with discrepancy</p>
</blockquote></li>
<li><blockquote>
<p>Missing attendance + missing script + absent with scripts &gt; 0</p>
</blockquote></li>
</ul></li>
</ul>
<ol start="4" type="1">
<li><blockquote>
<p>The ‘View Exam Detail’ and ‘Classroom Summary’ (it shall be displayed
at the row of the classroom centre) in the ‘Action’ column provides the
same functions stated in the Dashboard.</p>
</blockquote></li>
<li><blockquote>
<p>The columns displayed in the result tables mainly separated into 2
parts:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Exam data of the exam centre</p>
</blockquote></li>
<li><blockquote>
<p>Exam data confirmation</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Users shall be able to select the Simple mode or Full mode to display
the columns in the ‘Exam Centres’ page by clicking the [Simple Mode] or
[Full Mode] button.</p>
</blockquote></li>
<li><blockquote>
<p>Following fields are listed in different mode:</p>
</blockquote></li>
</ol>
<blockquote>
<p>Part 1 - exam data of the exam centre:</p>
</blockquote>
<table>
<colgroup>
<col style="width: 18%" />
<col style="width: 19%" />
<col style="width: 62%" />
</colgroup>
<thead>
<tr class="header">
<th>Display in Simple/Full Mode</th>
<th>Fields</th>
<th>Description</th>
</tr>
<tr class="odd">
<th>Both</th>
<th>Operator</th>
<th><ul>
<li><p>the login name of the helpdesk/operator</p></li>
<li><p>applicable to the officer/manager role users</p></li>
</ul></th>
</tr>
<tr class="header">
<th>Both</th>
<th>Centre Supervisor Logged In At</th>
<th><ul>
<li><p>Centre supervisor name with EP no. and the post, and the time of
his/her logged in CS Module. E.g. CHAN TIN NAM(10088-076 CS)
07:24</p></li>
<li><p>mouseover the centre supervisor name shall popup the school
telephone no. of the centre supervisor</p></li>
</ul></th>
</tr>
<tr class="odd">
<th>Both</th>
<th>Subject Code</th>
<th>Unique code of the subject as recorded in the HKDSE system</th>
</tr>
<tr class="header">
<th>Both</th>
<th>Paper Group</th>
<th>Paper code of the subject</th>
</tr>
<tr class="odd">
<th>Both</th>
<th>Centre Code</th>
<th>Unique code of the exam centre as recorded in the HKDSE system</th>
</tr>
<tr class="header">
<th>Both</th>
<th>Centre Type</th>
<th>Type of the exam centre as recorded in the HKDSE system, e.g. HALL,
HALL2, SEN CLASSROOM, etc.</th>
</tr>
<tr class="odd">
<th>Both</th>
<th>Assigned Cand</th>
<th><ul>
<li><p>Assigned candidate</p></li>
<li><p>the number of candidates assigned to the exam session</p></li>
</ul></th>
</tr>
<tr class="header">
<th>Both</th>
<th>Present Count</th>
<th>the number of assigned candidates who are present at the exam
session</th>
</tr>
<tr class="odd">
<th>Both</th>
<th>Absent Count</th>
<th>the number of assigned candidates who are absent from the exam
session</th>
</tr>
<tr class="header">
<th>Both</th>
<th>Missing Attendance</th>
<th><ul>
<li><p>the number of assigned candidates whose attendance status have
not been updated as present or absent yet</p></li>
</ul></th>
</tr>
<tr class="odd">
<th>Both</th>
<th>Wrong Centre</th>
<th>the number of special case candidates present at the exam
session</th>
</tr>
<tr class="header">
<th>Both</th>
<th>Absent with Script</th>
<th><ul>
<li><p>the total number of scripts collected that the assigned
candidates who are absent from the exam session</p></li>
</ul></th>
</tr>
<tr class="odd">
<th>Full</th>
<th>Expected Script Count</th>
<th>the total number of scripts to be collected from assigned candidates
and the wrong centre candidates present at the exam session</th>
</tr>
<tr class="header">
<th>Full</th>
<th>Script Collected</th>
<th>the total number of scripts collected from assigned candidates and
the wrong centre candidates present at the exam session</th>
</tr>
<tr class="odd">
<th>Both</th>
<th>Missing Script</th>
<th><ul>
<li><p>the total number of missing scripts that should be collected from
the assigned candidates and the wrong centre candidate present at the
exam session</p></li>
</ul></th>
</tr>
<tr class="header">
<th>Full mode</th>
<th>Total SR Form</th>
<th><ul>
<li><p>the total number of irregularity cases(with SR Form created) of
the assigned candidates and the wrong centre candidate present at the
exam session</p></li>
</ul></th>
</tr>
<tr class="odd">
<th>Both</th>
<th>Pending SR Form</th>
<th><ul>
<li><p>the total number of incomplete irregularity cases, i.e. the SR
Form status not completed yet</p></li>
</ul></th>
</tr>
<tr class="header">
<th>Both</th>
<th>Follow-up</th>
<th><ul>
<li><p>Y/N</p></li>
<li><p>Y when there is pending SR Form, otherwise, N shall be
displayed</p></li>
</ul></th>
</tr>
</thead>
<tbody>
</tbody>
</table>
<blockquote>
<p> </p>
</blockquote>
<ul>
<li><blockquote>
<p>Part 2 - Exam data confirmation</p>
</blockquote></li>
</ul>
<table>
<colgroup>
<col style="width: 15%" />
<col style="width: 13%" />
<col style="width: 70%" />
</colgroup>
<thead>
<tr class="header">
<th>Display in Simple/Full Mode</th>
<th>Fields</th>
<th>Description</th>
</tr>
<tr class="odd">
<th>Both</th>
<th>Remark from CS</th>
<th><ul>
<li><p>remarks inputted by CS when confirming the exam data
accuracy</p></li>
<li><p>[View] button shall be displayed if there is a remark and show
‘Nil’ if remarks are not inputted</p></li>
</ul></th>
</tr>
<tr class="header">
<th>Both</th>
<th>Notification to CS</th>
<th><ul>
<li><p>for confirming exam data accuracy, users shall be able to
single/multiple select the records or select the checkbox of ‘Select all
to notify CS’ and click the [Notify Selected] button or [Notify All]
button, the notification(s) shall be sent to the related CSs</p></li>
</ul></th>
</tr>
<tr class="odd">
<th>Both</th>
<th>Confirm to ESU</th>
<th><ul>
<li><p>for officer/manager role users to notify and confirm the exam
data accuracy for ESU, users shall be able to single/multiple select the
records or select the checkbox of ‘Select All Confirm’ and click the
[Confirm Selected] button or [Confirm All] button</p></li>
</ul></th>
</tr>
<tr class="header">
<th>Both</th>
<th>Confirmed by</th>
<th>the account of the officer/manager role user who confirms the exam
data accuracy for ESU</th>
</tr>
<tr class="odd">
<th>Both</th>
<th>Confirmed Time</th>
<th>the time when the officer/manager role user who confirms the exam
data accuracy for ESU</th>
</tr>
<tr class="header">
<th>Both</th>
<th>Action</th>
<th>A popup menu for directing to the individual exam situation page,
classroom summary (applicable to the row of classroom centre), message
board and downloading message board history</th>
</tr>
</thead>
<tbody>
</tbody>
</table>
<blockquote>
<p> </p>
</blockquote>
<ul>
<li><blockquote>
<p>After CS(s) have confirmed the exam data of the exam centre(s) to
VCC, manager / officer role users can download the Sessional Reports of
the exam centre(s) to the Excel file by clicking the [Sessional Report]
button.</p>
</blockquote></li>
<li><blockquote>
<p>After CS(s) have confirmed the exam data of the exam centre(s) to
VCC, users can single select or multiple select the checkbox(es) of the
‘Notification to CS’ and click the [Notify Selected] button to send
notification to the CS(s) of the selected exam centre(s).</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to select all the exam centres of the filtering
result by ticking the checkbox of the ‘Select All Notification’ and
clicking the [Notify Selected] button for notification to the CSs of all
the exam centres across all the pages of the filtering result.</p>
</blockquote></li>
<li><blockquote>
<p>A notification shall be sent to the message board of the CS.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall receive an alert if the CS changes the sessional report /
attendance / script data.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to single select or multiple select the
checkbox(es) of the ‘Confirm to ESU’ and click the [Confirm Selected]
button to confirm the exam data of the selected exam centre(s) to
ESU.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to select all the exam centres of the filtering
result by ticking the checkbox of ‘Select All Confirm’ button and click
the [Confirm Selected] to confirm the exam data of all exam centres
across all the pages of the filtering result to ESU.</p>
</blockquote></li>
<li><blockquote>
<p>Once the VCC manager / officer has confirmed the exam data to ESU,
his/her username and the confirmation time shall be displayed.</p>
</blockquote></li>
<li><blockquote>
<p>Confirmation to ESU is iterative, the username and the confirmation
time shall be kept updating.</p>
</blockquote></li>
<li><blockquote>
<p>CS shall be able to re-confirm the exam data to VCC if there is any
change in the exam data. If the VCC manager / officer has confirmed the
exam data to ESU after 1st exam data confirmation by CS, the VCC manager
/ officer shall receive an alert and be reminded to confirm the exam
data to ESU again.</p>
</blockquote></li>
</ul>
<blockquote>
<p> </p>
<p> </p>
</blockquote></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>VCC</th>
<th>105</th>
<th>13.3.4</th>
<th>Sessional Report</th>
<th><ol type="1">
<li><blockquote>
<p>After the CS(s) confirms the exam data of the exam centre(s), the
manager/officer role users shall be able to download the Sessional
Report(s) in CSV/Excel format by clicking the [Sessional Report] button
from the menu bar of the ‘Exam Centres’ page.</p>
</blockquote></li>
<li><blockquote>
<p>The filename starts with ‘sessional-report-summary’ followed by
yyyymmdd and 6 digit serial number.</p>
</blockquote></li>
</ol>
<blockquote>
<p>The export file shall be provided are listed as below:</p>
</blockquote>
<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 86%" />
</colgroup>
<thead>
<tr class="header">
<th>Report</th>
<th>Description</th>
</tr>
<tr class="odd">
<th>Hall-Details</th>
<th><p>Export file content:</p>
<p>centre code, school code, school name, subject code, subject name,
paper code, exam date, location, actual starting time, actual finishing
time, number of packets, number of answer scripts collected, listening
test mode (paper 3), reception of the listening component (paper 3),
remark (paper 3), report verified by invigilator 1, ep no./application
no./account no. of invigilator 1, name of invigilator 1, school name of
invigilator 1, invigilator 1’s verification time, report verified by
invigilator 2, ep no./application no./account no. of invigilator 2, name
of invigilator 2, school name of invigilator 2, invigilator 2’s
verification time, CS name, ep no. of CS, report submission time to
HKEAA, with IRR candidate record (Y/N), with IRR invigilator record
(Y/N)</p></th>
</tr>
<tr class="header">
<th>Classroom-Details</th>
<th><p>Export file content:</p>
<p>centre code, school code, school name, subject code, subject name,
paper code, exam date, location, actual starting time, actual finishing
time, number of packets, number of answer scripts collected, listening
test mode (paper 3), reception of the listening component (paper 3),
remark (paper 3), report submitted by CRI, ep no./application
no./account no. of CRI, name of CRI, school name of CRI, report
submission time to classroom CS, CS name, ep no. of CS, report
submission time to HKEAA, with IRR candidate record (Y/N), with IRR
invigilator record (Y/N)</p></th>
</tr>
<tr class="odd">
<th>Candidates with Irregularities (IRR)</th>
<th><p>Export file content:</p>
<p>centre code, school code, subject code, paper code, exam date,
candidate no. and name involved IRR</p></th>
</tr>
<tr class="header">
<th>Invigilators with Irregularities (IRR)</th>
<th><p>Export file content:</p>
<p>centre code, school code, subject code, paper code, exam date, ep
no./application no./account no. and name of invigilator involved
IRR</p></th>
</tr>
<tr class="odd">
<th>Invigilators</th>
<th><p>Export file content:</p>
<p>centre code, school code, subject code, paper code, exam date, ep
no./application no./account no. and name of invigilators, invigilator
type(TECH, SRI, DCS, AD HOC, INV, CS), last check-in time, last
check-out time</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>
<blockquote>
<p> </p>
<p> </p>
</blockquote></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="header">
<th>VCC</th>
<th>106</th>
<th>13.3.5</th>
<th>Display Individual Exam Centre Situation (View Exam Detail)</th>
<th><ol type="1">
<li><blockquote>
<p>Users shall be able to view the detailed examination, candidate, CS
and invigilator information of each of the (assigned) exam centres by
clicking the ‘View Exam Detail’ hyperlink under the ‘Action’ button in
the ‘Dashboard’ or ‘Exam Centre’ page.</p>
</blockquote></li>
<li><blockquote>
<p>Through the ‘View Exam Detail’ link, users shall be able to view
the:</p>
</blockquote></li>
</ol>
<ul>
<li><blockquote>
<p>Exam Information</p>
</blockquote>
<ul>
<li><blockquote>
<p>Exam Type and Year, e.g. DSE 2022</p>
</blockquote></li>
<li><blockquote>
<p>Exam Date</p>
</blockquote></li>
<li><blockquote>
<p>Centre Code and Name of Centre School</p>
</blockquote></li>
<li><blockquote>
<p>Centre Type</p>
</blockquote></li>
<li><blockquote>
<p>Subject Code and Subject Name</p>
</blockquote></li>
<li><blockquote>
<p>Paper Group</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>CS and Invigilator Assignment</p>
</blockquote>
<ul>
<li><blockquote>
<p>For CS:</p>
</blockquote>
<ul>
<li><blockquote>
<p>display CS’s name, EP number, school name and telephone number of the
school as recorded in the HKDSE system.</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>For Invigilator:</p>
</blockquote>
<ul>
<li><blockquote>
<p>display allocated invigilator’s name and EP number / Application
number as recorded in the HKDSE system.</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>For the absent invigilator, ‘(Absent)’ shall be displayed after the
information of the invigilator.</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Attendance and Script Records - a list of allocated candidates of the
exam centre shall be displayed.</p>
</blockquote>
<ul>
<li><blockquote>
<p>Candidate number</p>
</blockquote></li>
<li><blockquote>
<p>Candidate name</p>
</blockquote></li>
<li><blockquote>
<p>Case number</p>
</blockquote></li>
<li><blockquote>
<p>Seat number</p>
</blockquote></li>
<li><blockquote>
<p>Subject code</p>
</blockquote></li>
<li><blockquote>
<p>Paper group</p>
</blockquote></li>
<li><blockquote>
<p>Zone assigned in the exam centre</p>
</blockquote></li>
<li><blockquote>
<p>Present status</p>
</blockquote>
<ul>
<li><blockquote>
<p>‘- -’ means attendance record not yet taken</p>
</blockquote></li>
<li><blockquote>
<p>Present</p>
</blockquote></li>
<li><blockquote>
<p>ABS - absent</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Number of collected script(s) / number of scripts to be collected
from each candidate</p>
</blockquote></li>
<li><blockquote>
<p>Discrepancy related to the candidate case (missing attendance,
missing script, absent with script collected or missing attendance with
script collected, if any)</p>
</blockquote></li>
<li><blockquote>
<p>A ‘magnifying’ button for display information of candidate during the
exam (self check-in time, invigilator’s attendance taking time, number
of scripts collected, spare barcode, toilet request, and SR1 case
records)</p>
</blockquote></li>
<li><blockquote>
<p>An ‘pencil’ button for editing the attendance and Script records
(applicable to Manager role only)</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Special Case</p>
</blockquote>
<ul>
<li><blockquote>
<p>Candidate number</p>
</blockquote></li>
<li><blockquote>
<p>Identification document number or Candidate name</p>
</blockquote></li>
<li><blockquote>
<p>Case number</p>
</blockquote></li>
<li><blockquote>
<p>Zone assigned in the exam centre, similar to the Centre Supervisor,
users shall be able to create new zone by clicking the ‘+’ icon</p>
</blockquote></li>
<li><blockquote>
<p>Spare barcode assigned to each candidate</p>
</blockquote></li>
<li><blockquote>
<p>Number of collected script(s) / number of scripts to be collected
from each candidate</p>
</blockquote></li>
<li><blockquote>
<p>Discrepancy related to the candidates (e.g. Missing script)</p>
</blockquote></li>
<li><blockquote>
<p>The ‘Add Special Case’ button for creating special case, users shall
be able to add special case by candidate number, candidate’s
identification number and candidate name.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to create a new zone in the existing exam centre,
assign an invigilator of that exam centre to it. Then assign the worng
centre candidate to the new zone.</p>
</blockquote></li>
<li><blockquote>
<p>An ‘pencil’ button for editing the collected script record of each
candidate (applicable to Manager role only)</p>
</blockquote></li>
<li><blockquote>
<p>An ‘eraser’ button for removing the special case record (applicable
to Manager role only)</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>CS / Invigilator Assignment and Check-in Status</p>
</blockquote>
<ul>
<li><blockquote>
<p>EP number / Application number / ad hoc invigilator number of CS /
invigilator</p>
</blockquote></li>
<li><blockquote>
<p>English name</p>
</blockquote></li>
<li><blockquote>
<p>Post (CS / DCS / Invigilator / AD HOC)</p>
</blockquote></li>
<li><blockquote>
<p>Assignment (exam centre code of CS, DCS and classroom invigilator /
seat number range of hall invigilator)</p>
</blockquote></li>
<li><blockquote>
<p>Check-in date and time</p>
</blockquote></li>
<li><blockquote>
<p>Check-out date and time</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Discrepancy Report</p>
</blockquote>
<ul>
<li><blockquote>
<p>Candidate type</p>
</blockquote>
<ul>
<li><blockquote>
<p>Allocated</p>
</blockquote></li>
<li><blockquote>
<p>Special case</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Candidate number / candidate’s identification number</p>
</blockquote></li>
<li><blockquote>
<p>Candidate name</p>
</blockquote></li>
<li><blockquote>
<p>Case number</p>
</blockquote></li>
<li><blockquote>
<p>Seat number</p>
</blockquote></li>
<li><blockquote>
<p>Subject code</p>
</blockquote></li>
<li><blockquote>
<p>Paper group</p>
</blockquote></li>
<li><blockquote>
<p>Zone assigned in the exam centre</p>
</blockquote></li>
<li><blockquote>
<p>Spare barcode number</p>
</blockquote></li>
<li><blockquote>
<p>Remarks - discrepancy type:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Missing attendance record(s)</p>
</blockquote></li>
<li><blockquote>
<p>Missing attendance with script(s) collected</p>
</blockquote></li>
<li><blockquote>
<p>Missing script record(s)</p>
</blockquote></li>
<li><blockquote>
<p>Absent with script(s) collected</p>
</blockquote></li>
</ul></li>
</ul></li>
<li><blockquote>
<p>Sessional reports of the selected exam session</p>
</blockquote></li>
</ul>
<ol start="3" type="1">
<li><blockquote>
<p>Users shall be able to sort the tables (2.3 and 2.4 mentioned above)
by the field labels and select the field labels through the ‘Preference’
button.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to filter the list of candidates displayed by the
attendance and script status (2.3 mentioned above).</p>
</blockquote></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>VCC</th>
<th>115</th>
<th>13.3.6</th>
<th>School Assignment</th>
<th><ul>
<li><p>By filtering the Centre Type of an exam school, VCC manager shall
be able to reassign the operator to be responsible for the exam
centres.</p></li>
</ul></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="header">
<th>ESB (SEAD)</th>
<th>115</th>
<th>13.4.1</th>
<th>Login</th>
<th><ol type="1">
<li><blockquote>
<p>Users shall be able to enter their username and password to identify
their role, and the access to specific functions and data are set by the
IT Admin.</p>
</blockquote></li>
<li><blockquote>
<p>Function access is limited to the SEN system only.</p>
</blockquote></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>ESB (SEAD)</th>
<th>116</th>
<th>13.4.2</th>
<th>Attendance Record</th>
<th><ol type="1">
<li><blockquote>
<p>Searching fields include exam date, exam start and end time, subject
code, paper, school code, school name, centre code and centre type.</p>
</blockquote></li>
<li><blockquote>
<p>Related exam centre(s) of the filtering result shall be listed
according to the user’s selection.</p>
</blockquote></li>
<li><blockquote>
<p>By clicking the ‘right arrow’ of the exam centre, each exam session
of the corresponding exam centre shall be displayed at the right
side.</p>
</blockquote></li>
<li><blockquote>
<p>By clicking the ‘right arrow’ of the exam session, the attendance
records related to allocated candidates and special cases shall be
displayed. Users shall be able to select among two types of cases by
clicking the corresponding tabs.</p>
</blockquote></li>
<li><blockquote>
<p>Searching fields shall include attendance status(e.g. ‘- -’
attendance record not yet taken, present and absent), location (centre
type, such as HALL, SEN CLASSROOM), answer script collection status, and
keywords such as candidate no., candidate name and spare barcode no.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to sort the table by the field labels.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to select columns displayed by toggling the
‘Preferences’ button.</p>
</blockquote></li>
<li><blockquote>
<p>Allocated Candidates</p>
</blockquote>
<ul>
<li><blockquote>
<p>The exam data of allocated candidates shall be displayed in a table,
such as:</p>
</blockquote>
<ul>
<li><blockquote>
<p>School name</p>
</blockquote></li>
<li><blockquote>
<p>Subject name</p>
</blockquote></li>
<li><blockquote>
<p>Subject code</p>
</blockquote></li>
<li><blockquote>
<p>Paper group</p>
</blockquote></li>
<li><blockquote>
<p>Centre code</p>
</blockquote></li>
<li><blockquote>
<p>Centre type (HALL, SEN CLASSROOM)</p>
</blockquote></li>
<li><blockquote>
<p>Mode (applicable to the listening paper)</p>
</blockquote></li>
<li><blockquote>
<p>Zone</p>
</blockquote></li>
<li><blockquote>
<p>Candidate number</p>
</blockquote></li>
<li><blockquote>
<p>Candidate name</p>
</blockquote></li>
<li><blockquote>
<p>Seat number</p>
</blockquote></li>
<li><blockquote>
<p>Case number</p>
</blockquote></li>
<li><blockquote>
<p>Attendance status (‘- -’ - attendance record not yet taken, present,
absent)</p>
</blockquote></li>
<li><blockquote>
<p>Answer script collection status (answer script collected / answer
script to be collected)</p>
</blockquote></li>
<li><blockquote>
<p>Location (applicable to the normal exam centre )</p>
</blockquote></li>
<li><blockquote>
<p>Self check-in time</p>
</blockquote></li>
<li><blockquote>
<p>Invigilator’s taking attendance time</p>
</blockquote></li>
<li><blockquote>
<p>Spare barcode number</p>
</blockquote></li>
</ul></li>
</ul></li>
<li><blockquote>
<p>Special Cases</p>
</blockquote>
<ul>
<li><blockquote>
<p>The special cases of the exam centre shall be displayed with the
information of the:</p>
</blockquote>
<ul>
<li><blockquote>
<p>School name</p>
</blockquote></li>
<li><blockquote>
<p>Subject name</p>
</blockquote></li>
<li><blockquote>
<p>Subject code</p>
</blockquote></li>
<li><blockquote>
<p>Paper group</p>
</blockquote></li>
<li><blockquote>
<p>Centre code</p>
</blockquote></li>
<li><blockquote>
<p>Centre type</p>
</blockquote></li>
<li><blockquote>
<p>Mode (applicable to the listening paper)</p>
</blockquote></li>
<li><blockquote>
<p>Candidate number</p>
</blockquote></li>
<li><blockquote>
<p>Candidate name</p>
</blockquote></li>
<li><blockquote>
<p>Candidate’s identification number</p>
</blockquote></li>
<li><blockquote>
<p>Zone</p>
</blockquote></li>
<li><blockquote>
<p>Spare barcode number</p>
</blockquote></li>
<li><blockquote>
<p>Case number </p>
</blockquote></li>
<li><blockquote>
<p>CS creates special case time</p>
</blockquote></li>
<li><blockquote>
<p>Answer script collection status (answer script collected / answer
script to be collected)</p>
</blockquote></li>
</ul></li>
</ul></li>
<li><blockquote>
<p>The exam data shall be downloaded as CSV by single/multiple selecting
the records or select the check box next to the ‘Export’ button to
select all records in the result table of all pages, and then click the
‘Export’ button.</p>
</blockquote></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="header">
<th>ESB (SEAD)</th>
<th>119</th>
<th>13.4.3</th>
<th>Discrepancy Report</th>
<th><ol type="1">
<li><blockquote>
<p>4 situations shall be covered in the discrepancy report:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Missing attendance record(s)</p>
</blockquote></li>
<li><blockquote>
<p>Missing attendance but with script collected</p>
</blockquote></li>
<li><blockquote>
<p>Missing script records</p>
</blockquote></li>
<li><blockquote>
<p>Absent but with script(s) collected</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Discrepancy records related to allocated candidates and special cases
shall be displayed. Users shall be able to select among two types of
cases by clicking the corresponding tabs.</p>
</blockquote></li>
<li><blockquote>
<p>Records with discrepancy shall be displayed:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Candidate number</p>
</blockquote></li>
<li><blockquote>
<p>Candidate name</p>
</blockquote></li>
<li><blockquote>
<p>Subject name</p>
</blockquote></li>
<li><blockquote>
<p>Subject code, paper group</p>
</blockquote></li>
<li><blockquote>
<p>School name</p>
</blockquote></li>
<li><blockquote>
<p>School code</p>
</blockquote></li>
<li><blockquote>
<p>Centre code</p>
</blockquote></li>
<li><blockquote>
<p>Centre type</p>
</blockquote></li>
<li><blockquote>
<p>Zone</p>
</blockquote></li>
<li><blockquote>
<p>Mode (applicable to the listening paper)</p>
</blockquote></li>
<li><blockquote>
<p>Spare barcode number</p>
</blockquote></li>
<li><blockquote>
<p>Seat number</p>
</blockquote></li>
<li><blockquote>
<p>Case number</p>
</blockquote></li>
<li><blockquote>
<p>Attendance status (present, absent, ‘- -’ means attendance record not
yet taken)</p>
</blockquote></li>
<li><blockquote>
<p>Answer script collection status (answer script collected / answer
script to be collected)</p>
</blockquote></li>
<li><blockquote>
<p>Remarks (4 types of discrepancy situation listed above)</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>The information shall be downloaded as CSV by single/multiple
selecting the records or select the check box next to the ‘Export’
button to select all records in the result table of all pages, and then
click the ‘Export’ button.</p>
</blockquote></li>
<li><blockquote>
<p>Information can be viewed by filtering the exam date, exam start and
end time, subject code, paper group, school code, school name, centre
code, centre type, and candidate number..</p>
</blockquote></li>
<li><blockquote>
<p>Information of the tables shall be sorted by different columns.</p>
</blockquote></li>
</ol>
<ol start="7" type="1">
<li><blockquote>
<p>Users shall be able to select columns displayed by toggling the
‘Preferences’ button.</p>
</blockquote></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>ESB (SEAD)</th>
<th>120</th>
<th>13.4.4</th>
<th>Event Log</th>
<th><ol type="1">
<li><blockquote>
<p>Users shall be able to view the actions of Candidate App, Invigilator
App, CS Module and VCC Module.</p>
</blockquote></li>
<li><blockquote>
<p>The events logged shall be displayed by filtering the exam date, exam
time period, subject code, paper, school code, school name, centre code,
centre type, CS/invigilator no. and candidate number.</p>
</blockquote></li>
<li><blockquote>
<p>The Information Result table should include:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Event date and time (in dddd-mm-yy hh:mn:ss format)</p>
</blockquote></li>
<li><blockquote>
<p>Centre code</p>
</blockquote></li>
<li><blockquote>
<p>School code</p>
</blockquote></li>
<li><blockquote>
<p>Candidate number / EP no. of CS or invigilator</p>
</blockquote></li>
<li><blockquote>
<p>Actor type (candidate, CS, DCS, VCC)</p>
</blockquote></li>
<li><blockquote>
<p>Event</p>
</blockquote></li>
<li><blockquote>
<p>Location (HALL, SEN CLASSROOM)</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Users shall be able to select columns displayed by toggling the
‘Preferences’ button.</p>
</blockquote></li>
<li><blockquote>
<p>Records of event log shall be downloaded as CSV. The existing list of
event / access / activity logs is pending enhancement and further update
by taking into account the possible actions related to SEN Module.</p>
</blockquote></li>
<li><blockquote>
<p>The list of event logs covered in PESS2 are provided below, (it shall
be kept on update during implementation in phase 3 if needed):</p>
</blockquote></li>
</ol>
<table>
<colgroup>
<col style="width: 11%" />
<col style="width: 25%" />
<col style="width: 63%" />
</colgroup>
<thead>
<tr class="header">
<th><strong> </strong></th>
<th><strong>Event</strong></th>
<th><strong>Sample</strong></th>
</tr>
<tr class="odd">
<th><strong>VCC</strong></th>
<th> </th>
<th> </th>
</tr>
<tr class="header">
<th>1</th>
<th>Update school assignment</th>
<th>VCC Manager nmanager assigns school 10001 centre D1000 with subject
A080C paper 2 to VCC Operator B1400-help03.</th>
</tr>
<tr class="odd">
<th>2</th>
<th>Delete school assignment by Excel</th>
<th>VCC Manager nmanager deletes 3 school assignments by uploading
excel.</th>
</tr>
<tr class="header">
<th>3</th>
<th>Update school assignment by Excel</th>
<th>VCC Manager nmanager updates 9 school assignments by uploading
excel.</th>
</tr>
<tr class="odd">
<th>4</th>
<th>Modify assigned candidate script</th>
<th>VCC Manager nmanager modifies the collected script count of assigned
candidate 929393040 into 1 at exam school 10066 centre B1400 with
subject A010C paper 3.</th>
</tr>
<tr class="header">
<th>5</th>
<th>Modify assigned candidate attendance</th>
<th>VCC Manager nmanager modifies attendance status of assigned
candidate 924224030 into present at exam school 10066 centre B1400 with
subject A010C paper 3.</th>
</tr>
<tr class="odd">
<th>6</th>
<th>Log out</th>
<th>VCC User nmanager logs out.</th>
</tr>
<tr class="header">
<th>7</th>
<th>Send dismissal message</th>
<th>VCC User nmanager sends dismissal message to exam school 10058
centre D1350 with subject A010C paper 2.</th>
</tr>
<tr class="odd">
<th>8</th>
<th>Create special case</th>
<th>VCC Manager nmanager creates special case 225398945 at exam school
10058 centre D1350 with subject A010C paper 3.</th>
</tr>
<tr class="header">
<th>9</th>
<th>Update special case</th>
<th>VCC Manager nmanager updates special case my-test-nov-6 script count
from 0 into 1 at exam school 30740 centre S1750 with subject A010C paper
2.</th>
</tr>
<tr class="odd">
<th>10</th>
<th>Delete special case</th>
<th>VCC Manager nmanager deletes special case Tai Chan Man at exam
school 10058 centre D1350 with subject A010C paper 3.</th>
</tr>
<tr class="header">
<th>11</th>
<th>Add helpdesk user</th>
<th>VCC Manager nmanager adds helpdesk user mc-new-opera as Normal
Officer &amp; Normal Operator.</th>
</tr>
<tr class="odd">
<th>12</th>
<th>Update helpdesk user</th>
<th>VCC Manager nmanager updates helpdesk user mc-new-opera Normal
Officer role from false into true, Normal Operator role from true into
false, English name from mc-operator into mc-officer, Chinese name from
mv-operator into mc-officer.</th>
</tr>
<tr class="header">
<th>13</th>
<th>Update manager</th>
<th>VCC Manager nmanager updates information of VCC Manager nmanager
English name from normal-manager into nmanager2022, Chinese name from
normal-manager into nmanager2022.</th>
</tr>
<tr class="odd">
<th>14</th>
<th>Delete helpdesk user</th>
<th>VCC Manager nmanager deletes helpdesk user mc-new-opera.</th>
</tr>
<tr class="header">
<th>15</th>
<th>Confirm to ESU</th>
<th>VCC User nmanager confirms exam school 10058 centre D1350 with
subject A010C paper 2 to ESU.</th>
</tr>
<tr class="odd">
<th>16</th>
<th>Download exam session excel</th>
<th>VCC User nmanager downloads excel of 30 exam sessions.</th>
</tr>
<tr class="header">
<th>17</th>
<th>Download school assignment excel</th>
<th>VCC Manager nmanager downloads excel of 9635 school
assignments.</th>
</tr>
<tr class="odd">
<th>18</th>
<th>Log in</th>
<th>VCC User nmanager logs in.</th>
</tr>
<tr class="header">
<th>19</th>
<th>Send a broadcast message to selected candidates</th>
<th>VCC User nmanager sends a broadcast message to 847 candidates.</th>
</tr>
<tr class="odd">
<th>20</th>
<th>Send a broadcast message to selected invigilators</th>
<th>VCC User nmanager sends a broadcast message to 10100
invigilators.</th>
</tr>
<tr class="header">
<th>CS</th>
<th> </th>
<th> </th>
</tr>
<tr class="odd">
<th>1</th>
<th>Create Ad Hoc invigilator</th>
<th>Centre supervisor 10058-059 creates Ad Hoc invigilator 10034-087 at
exam school 10058 centre D1350 with subject A010C paper 3.</th>
</tr>
<tr class="header">
<th>2</th>
<th>Modify assigned candidate script</th>
<th>Centre supervisor 10058-059 modifies the collected script count of
assigned candidate 928949270 into 2 at exam school 10058 centre D1350
with subject A010C paper 3.</th>
</tr>
<tr class="odd">
<th>3</th>
<th>Create centre invigilator assignment</th>
<th>Centre supervisor 10058-059 creates invigilator assignment of exam
centre at exam school 10058 centre D1350 with subject A010C paper
3.</th>
</tr>
<tr class="header">
<th>4</th>
<th>Create special room invigilator assignment</th>
<th>Centre supervisor 10058-059 creates invigilator assignment of 3
special room(s) at exam school 10058 centre D1350 with subject A010C
paper 3.</th>
</tr>
<tr class="odd">
<th>5</th>
<th>Delete invigilator assignment</th>
<th>Centre supervisor 30692-005 deletes invigilator assignment at exam
school 30692 centre P1150 with subject A010C paper 3.</th>
</tr>
<tr class="header">
<th>6</th>
<th>Replace invigilator assignment</th>
<th>Centre supervisor 30701-029 replaces the assignee of Seat Number
1-41 with invigilator 30701-052 at exam school 30701 centre S1600 with
subject A010C paper 3.</th>
</tr>
<tr class="odd">
<th>7</th>
<th>Modify assigned candidate attendance</th>
<th>Centre supervisor 10073-004 modifies attendance status of candidate
923503910 into absent using spare barcode 0A010C0030A135065336 at exam
school 10073 centre A1350 with subject A010C paper 3.</th>
</tr>
<tr class="header">
<th>8</th>
<th>Log in</th>
<th>Centre supervisor 10058-059 logs in at exam school 10058 centre
D1350 with subject A010C paper 3.</th>
</tr>
<tr class="odd">
<th>9</th>
<th>Log out</th>
<th>Centre supervisor 10066-004 logs out at exam school 10066 centre
B1400 with subject A010C paper 3.</th>
</tr>
<tr class="header">
<th>10</th>
<th>Create chat group</th>
<th>Centre supervisor 30740-061 creates chat group classroom_1025 with
invigilator(s) 30740-045, 30740-041, 30740-020 at exam school 30740
centre S1750 with subject A010C paper 3.</th>
</tr>
<tr class="odd">
<th>11</th>
<th>Remove chat group</th>
<th>Centre supervisor 30740-061 removes chat group (classroom_1025) at
exam school 30740 centre S1750 with subject A010C paper 3.</th>
</tr>
<tr class="header">
<th>12</th>
<th>Save sessional report</th>
<th>Centre supervisor 20355-044 saves sessional report at exam school
20355 centre E1980 with subject A010C paper 3.</th>
</tr>
<tr class="odd">
<th>13</th>
<th>Submit sessional report</th>
<th>Centre supervisor 20355-044 submits sessional report at exam school
20355 centre E1980 with subject A010C paper 3.</th>
</tr>
<tr class="header">
<th>14</th>
<th>Create special room</th>
<th>Centre supervisor 10058-059 creates special room LTSR-2 (MC-201) at
exam school 10058 centre D1350 with subject A010C paper 3.</th>
</tr>
<tr class="odd">
<th>15</th>
<th>Delete special room</th>
<th>Centre supervisor 10058-059 deletes special room LTSR-2 (MC-201) at
exam school 10058 centre D1350 with subject A010C paper 3.</th>
</tr>
<tr class="header">
<th>16</th>
<th>Move assigned candidate to special room</th>
<th>Centre supervisor 10058-059 moves assigned candidate 922569630 to
special room at exam school 10058 centre D1350 with subject A010C paper
3.</th>
</tr>
<tr class="odd">
<th>17</th>
<th>Move wrong centre candidate to special room</th>
<th>Centre supervisor 10058-059 moves wrong centre candidate 227563142
to special room at exam school 10058 centre D1350 with subject A010C
paper 3.</th>
</tr>
<tr class="header">
<th>18</th>
<th>Undo moving candidate to special room</th>
<th>Centre supervisor 10058-059 undoes moving 928949270 to special room
at exam school 10058 centre D1350 with subject A010C paper 3.</th>
</tr>
<tr class="odd">
<th>19</th>
<th>Create special case</th>
<th>Centre supervisor 10058-059 creates special case Channnnnn using
spare barcode 0A010C0030D135073530 at exam school 10058 centre D1350
with subject A010C paper 3.</th>
</tr>
<tr class="header">
<th>20</th>
<th>Update special case</th>
<th>Centre supervisor 10058-059 updates special case 227563142 candidate
name from [empty] into 考生227563142, identity document from [empty]
into 22756314(2), spare barcode from 0A010C0030D135062435 into
0A010C0030D135030444, script count from 2 into 3 at exam school 10058
centre D1350 with subject A010C paper 3.</th>
</tr>
<tr class="odd">
<th>21</th>
<th>Delete special case</th>
<th>Centre supervisor 10058-059 deletes special case Yo with spare
barcode 0A010C0030D135088910at exam school 10058 centre D1350 with
subject A010C paper 3.</th>
</tr>
<tr class="header">
<th>22</th>
<th>Confirm exam status</th>
<th>Centre supervisor 10058-059 confirms exam status to Virtual Command
Centre at exam school 10058 centre D1350 with subject A010C paper
3.</th>
</tr>
<tr class="odd">
<th>23</th>
<th>Check invigilator out</th>
<th>Centre supervisor 10058-059 checks invigilator 2972615 out at exam
school 10058 centre D1350 with subject A010C paper 3.</th>
</tr>
<tr class="header">
<th>24</th>
<th>Start timer</th>
<th>Centre supervisor 10058-059 starts timer at 2022-10-28 00:00 with
duration 1380 minutes at exam school 10058 centre D1350 with subject
A010C paper 3.</th>
</tr>
<tr class="odd">
<th>25</th>
<th>Switch to another subject or paper at the same exam centre</th>
<th>Centre supervisor 10066-004 switches to another subject or paper
from exam school 10066 centre B1400 with subject A010C paper 3.</th>
</tr>
<tr class="header">
<th>26</th>
<th>Send notification message to invigilator</th>
<th>Centre Supervisor 10066-004 sends a notification message to
invigilator 3642469 at exam school 10058 centre D1350 with subject A010C
paper 3.</th>
</tr>
<tr class="odd">
<th>27</th>
<th>Request confirm sessional report</th>
<th>Centre supervisor 10066-004 requests invigilator 3642469 and
invigilator 5187641's confirmation of the sessional report of exam
school 10058 centre D1350 with subject A010C paper 3.</th>
</tr>
<tr class="header">
<th>Candidate App</th>
<th> </th>
<th> </th>
</tr>
<tr class="odd">
<th>1</th>
<th>Request passcode</th>
<th>Candidate 229442562 requests passcode.</th>
</tr>
<tr class="header">
<th>2</th>
<th>Log in</th>
<th>Candidate 229442562 logs in.</th>
</tr>
<tr class="odd">
<th>3</th>
<th>Log out</th>
<th>Candidate 923515474 logs out.</th>
</tr>
<tr class="header">
<th>4</th>
<th>Self check-in</th>
<th>Candidate 925736630 succeeds to self check-in at exam school 10058
centre D1350 with subject A010C paper 3.</th>
</tr>
<tr class="odd">
<th>5</th>
<th>Scan wrong barcode</th>
<th>Candidate 226177594 scans a wrong barcode
0A010C00392573663049z.</th>
</tr>
<tr class="header">
<th>6</th>
<th>Confirm at special room reason and arrival time</th>
<th>Candidate 925736630 confirms reason and arrival time in special room
Special Room at exam school 10058 centre D1350 with subject A010C paper
3.</th>
</tr>
<tr class="odd">
<th>7</th>
<th>Read a message from HKEAA</th>
<th>Candidate 226177594 reads a message from HKEAA, "Hello4".</th>
</tr>
<tr class="header">
<th>8</th>
<th>Launch application as a logged-in user</th>
<th>Candidate 226177594 launches the application as a logged-in
user.</th>
</tr>
<tr class="odd">
<th>9</th>
<th>Capture Screenshot</th>
<th>Candidate 226177594 captures screenshot at exam school 10058 centre
D1350 with subject A010C paper 3.</th>
</tr>
<tr class="header">
<th>Invigilator App</th>
<th> </th>
<th> </th>
</tr>
<tr class="odd">
<th>1</th>
<th>Log out</th>
<th>Invigilator 3642469 logs out.</th>
</tr>
<tr class="header">
<th>2</th>
<th>Mark present at centre</th>
<th>Invigilator 5187641 marks candidate 927790210 present at exam school
10037 centre A1000 with subject A010C paper 3.</th>
</tr>
<tr class="odd">
<th>3</th>
<th>Create candidate flag</th>
<th>Invigilator 8548870 creates a flag for assigned candidate CANDIDATE
NAME 929701546 at exam school 10058 centre D1350 with subject A010C
paper 3.</th>
</tr>
<tr class="header">
<th>4</th>
<th>Add candidate remark</th>
<th>Invigilator 7813095 adds a remark to the flag for assigned candidate
923038470 at exam school 10058 centre D1350 with subject A010C paper
3.</th>
</tr>
<tr class="odd">
<th>5</th>
<th>Create check-out record</th>
<th>Invigilator 7813095 creates a check-out record for assigned
candidate 923038470 at exam school 10058 centre D1350 with subject A010C
paper 3.</th>
</tr>
<tr class="header">
<th>6</th>
<th>Create check-in record</th>
<th>Invigilator 30701-015 creates a check-in record for assigned
candidate 922415239 at exam school 30701 centre S1600 with subject A010C
paper 3.</th>
</tr>
<tr class="odd">
<th>7</th>
<th>Collect script</th>
<th>Invigilator 30701-015 collects script from assigned candidate
927026601 at exam school 30701 centre S1600 with subject A010C paper
3.</th>
</tr>
<tr class="header">
<th>8</th>
<th>Assgin spare barcode to candidate</th>
<th>Invigilator 8548870 registers spare barcode 0A010C0030D135068318 for
assigned candidate 929922120 at exam school 10058 centre D1350 special
room LTSR-1 (SR1) with subject A010C paper 3.</th>
</tr>
<tr class="odd">
<th>9</th>
<th>Create special case</th>
<th>Invigilator 8548870 creates special case 222102709 at exam school
10058 centre D1350 with subject A010C paper 3.</th>
</tr>
<tr class="header">
<th>10</th>
<th>Assign wrong centre candidate (Hall special Case) to special
room</th>
<th><p><strong>Candidate Name is inputted:</strong></p>
<p>Invigilator 8548870 assigns wrong centre candidate CCCCCCCC to
special room LTSR-1 (SR1) at exam school 10058 centre D1350 with subject
A010C paper 3.</p>
<p>/</p>
<p><strong>Candidate No. is inputted:</strong></p>
<p>Invigilator 8548870 assigns wrong centre candidate 229551349 to
special room LTSR-1 (SR1) at exam school 10058 centre D1350 with subject
A010C paper 3.</p></th>
</tr>
<tr class="odd">
<th>11</th>
<th>Assign candidate special room</th>
<th>Invigilator 8548870 assigns assigned candidate 928541456 to special
room LTSR-1 (SR1) at exam school 10058 centre D1350 with subject A010C
paper 3.</th>
</tr>
<tr class="header">
<th>12</th>
<th>Update spare barcode</th>
<th>Invigilator 30701-015 updates spare barcode from
0A010C0030A105011263 to 0A010C0030S160077074 for candidate 927790210 at
exam school 30701 centre S1600 special room LTSR-1 (A001) with subject
A010C paper 3.</th>
</tr>
<tr class="odd">
<th>13</th>
<th>Modify candidate script</th>
<th>Invigilator 30701-015 modifies the collected script count of
candidate 927790210 into 1 at exam school 30701 centre S1600 special
room LTSR-1 (A001) with subject A010C paper 3.</th>
</tr>
<tr class="header">
<th>14</th>
<th>Modify candidate confirmation SR4g</th>
<th>Invigilator 30701-015 modifies the confirmation status of candidate
220011944 into SR4g at exam school 30701 centre S1600 special room
LTSR-1 (A001) with subject A010C paper 3.</th>
</tr>
<tr class="odd">
<th>15</th>
<th>Create special room sessional report</th>
<th>Invigilator 30701-015 creates special room sessional report at exam
school 30701 centre S1600 special room LTSR-1 (A001) with subject A010C
paper 3.</th>
</tr>
<tr class="header">
<th>16</th>
<th>Update special room sessional report</th>
<th>Invigilator 30701-015 updates special room sessional report at exam
school 30701 centre S1600 special room LTSR-1 (A001) with subject A010C
paper 3.</th>
</tr>
<tr class="odd">
<th>17</th>
<th>Complete special room sessional report</th>
<th>Invigilator 30701-015 completes special room sessional report at
exam school 30701 centre S1600 special room LTSR-1 (A001) with subject
A010C paper 3.</th>
</tr>
<tr class="header">
<th>18</th>
<th>Confirm discrepancy record</th>
<th>Invigilator 30701-015 confirms discrepancy record(s) at exam school
30701 centre S1600 special room LTSR-1 (A001) with subject A010C paper
3.</th>
</tr>
<tr class="odd">
<th>19</th>
<th>Check in</th>
<th>Invigilator 3642469 checks in at exam school 10037 centre A1000 with
subject A010C paper 3.</th>
</tr>
<tr class="header">
<th>20</th>
<th>Check out</th>
<th>Invigilator 3642469 checks out at exam school 10037 centre A1000
with subject A010C paper 3.</th>
</tr>
<tr class="odd">
<th>21</th>
<th>Mark present at special room</th>
<th>Invigilator 9084306 marks candidate 225507716 present at exam school
10058 centre D1350 special room LTSR-1 (1) with subject A010C paper
3.</th>
</tr>
<tr class="header">
<th>22</th>
<th>SR update reason, SR arrival time</th>
<th>Invigilator 8548870 marks reason at special room as B and arrival
time as 2022-10-30 16:19 for assigned candidate 924525711 goes to
special room LTSR-1 (SR1) at exam school 10058 centre D1350 with subject
A010C paper 3.</th>
</tr>
<tr class="odd">
<th>23</th>
<th>SRI timer</th>
<th>Invigilator 8002055 starts timer at 2022-10-30 20:26 with duration
75 minutes at exam school 10058 centre D1350 special room LTSR-1 (aaa)
with subject A010C paper 3.</th>
</tr>
<tr class="header">
<th>24</th>
<th>Pause timer / Resume timer</th>
<th>Invigilator 8002055 pauses/resumes timer at 2022-10-30 20:26 with
duration 75 minutes at exam school 10058 centre D1350 special room
LTSR-1 (aaa) with subject A010C paper 3.</th>
</tr>
<tr class="odd">
<th>25</th>
<th>Log in by scanning a QR code</th>
<th>Invigilator 5317598 logs in by scanning a QR code.</th>
</tr>
<tr class="header">
<th>26</th>
<th>View information of candidate displayed withou completing indentity
verfication or attendance taking</th>
<th>Invigilator 30740-020 views information of candidate 920763210
displayed without completing identity verification or attendance taking
at exam school 30740 centre S1750 with subject A010C paper 3.</th>
</tr>
<tr class="odd">
<th>27</th>
<th>Verify identity of candidates</th>
<th>Invigilator 30740-020 verifies identity of candidate 925307441
present at exam school 30740 centre S1750 with subject A010C paper
3.</th>
</tr>
<tr class="header">
<th>28</th>
<th>Take attendance for candidates</th>
<th>Invigilator 30740-020 takes attendance for candidate 927752250
present at exam school 30740 centre S1750 with subject A010C paper
3.</th>
</tr>
<tr class="odd">
<th>29</th>
<th>Launch application as a logged-in user</th>
<th>Invigilator 30740-020 launches the application as a logged-in
user.</th>
</tr>
</thead>
<tbody>
</tbody>
</table>
<blockquote>
<p> </p>
<p> </p>
</blockquote></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="header">
<th>ESB (SEAD)</th>
<th>128</th>
<th>13.4.5</th>
<th>Report List</th>
<th><ol type="1">
<li><blockquote>
<p>More report types may be developed / available for downloading in the
Exam Support Backend (SEAD) after the SR Forms Module was developed.</p>
</blockquote></li>
<li><blockquote>
<p>In order to prevent a huge volume of information from being loaded,
the ‘No Data’ page shall be displayed at first.</p>
</blockquote></li>
<li><blockquote>
<p>Sessional Report</p>
</blockquote>
<ul>
<li><blockquote>
<p>By filtering, a list of the centre related to the completion of the
sessional reports shall be displayed, such as:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Exam date (in yyyy-mm-dd format)</p>
</blockquote></li>
<li><blockquote>
<p>Exam time (in hh:mn format)</p>
</blockquote></li>
<li><blockquote>
<p>School code</p>
</blockquote></li>
<li><blockquote>
<p>School name</p>
</blockquote></li>
<li><blockquote>
<p>Centre code</p>
</blockquote></li>
<li><blockquote>
<p>Centre type</p>
</blockquote></li>
<li><blockquote>
<p>Exam date (in yyyy-mm-dd format)</p>
</blockquote></li>
<li><blockquote>
<p>Exam time (in hh:mn format)</p>
</blockquote></li>
<li><blockquote>
<p>Report completion status (Y/N)</p>
</blockquote></li>
<li><blockquote>
<p>Exam data confirmation status by CS (Y/N)</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Searching fields shall include exam date, exam start and end time,
subject code, paper group, school code, school name, centre code, and
centre type.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to select columns displayed by toggling the
‘Preferences’ button.</p>
</blockquote></li>
<li><blockquote>
<p>[View] button shall be available for the completed Sessional Reports
and exam data has been confirmed by CS. Click [View] button shall
display the Sessional Report of the corresponding exam session.</p>
</blockquote></li>
<li><blockquote>
<p>Click the check box on the column header of the result table to
select all records and click the [Export] button to export all records
on all pages or single/multiple select the row(s) and click the [Export]
button to export the selected records in csv or excel.</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Irregularities - Screenshot events (More reports shall be provided
after the implementation of the SR Forms Module)</p>
</blockquote>
<ul>
<li><blockquote>
<p>By filtering, a list of filtering results shall be displayed with the
information of:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Subject name</p>
</blockquote></li>
<li><blockquote>
<p>Subject code</p>
</blockquote></li>
<li><blockquote>
<p>Paper group</p>
</blockquote></li>
<li><blockquote>
<p>School name</p>
</blockquote></li>
<li><blockquote>
<p>School code</p>
</blockquote></li>
<li><blockquote>
<p>Centre code</p>
</blockquote></li>
<li><blockquote>
<p>Centre type</p>
</blockquote></li>
<li><blockquote>
<p>Exam date (in yyyy-mm-dd format)</p>
</blockquote></li>
<li><blockquote>
<p>Exam time (in hh:mn:ss format)</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Number of abnormal case</p>
</blockquote></li>
<li><blockquote>
<p>Searching fields shall include exam date, exam start and end time,
subject code, paper group, school code, school name, centre code, and
centre type.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to select columns displayed by toggling the
‘Preferences’ button.</p>
</blockquote></li>
<li><blockquote>
<p>[View] button in the ‘Action’ column shall be available for the
detailed records of irregularities in the corresponding exam session.
Following fields shall be displayed:</p>
</blockquote></li>
<li><blockquote>
<p>Candidate no./ID no., candidate name, normal or special case, seat
no., and the screenshot event time in yyyy-mm-dd hh:mn:ss format.</p>
</blockquote></li>
<li><blockquote>
<p>Click the check box on the column header of the result table to
select all records and click the [Export] button to export all records
on all pages or single/multiple select the row(s) and click the [Export]
button to export the selected records in csv or excel.</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>CS / Invigilator Check in / out records</p>
</blockquote>
<ul>
<li><blockquote>
<p>By filtering, a list of the exam session shall be displayed
including:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Exam date (in yyyy-mm-dd format)</p>
</blockquote></li>
<li><blockquote>
<p>Exam time (in hh:mn format)</p>
</blockquote></li>
<li><blockquote>
<p>School code</p>
</blockquote></li>
<li><blockquote>
<p>School name</p>
</blockquote></li>
<li><blockquote>
<p>Centre code</p>
</blockquote></li>
<li><blockquote>
<p>Centre type</p>
</blockquote></li>
<li><blockquote>
<p>Subject code</p>
</blockquote></li>
<li><blockquote>
<p>Subject name</p>
</blockquote></li>
<li><blockquote>
<p>Paper group</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Searching fields shall include exam date, exam start and end time,
subject code, paper group, school code, school name, centre code, and
centre type.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to select columns displayed by toggling the
‘Preferences’ button.</p>
</blockquote></li>
<li><blockquote>
<p>[View] button shall be available for the detailed check in / out
records of exam personnel in the corresponding exam session. Following
fields shall be displayed:</p>
</blockquote>
<ul>
<li><blockquote>
<p>EP no./Application no./Ad hoc invigilator no.</p>
</blockquote></li>
<li><blockquote>
<p>English name of invigilator</p>
</blockquote></li>
<li><blockquote>
<p>Post (INV, SRI, CS)</p>
</blockquote></li>
<li><blockquote>
<p>Assignment (centre code or seat no. range if assignment created, ‘--’
for those assignments not yet created)</p>
</blockquote></li>
<li><blockquote>
<p>Checked in time (in yyyy-mm-dd hh:mn:ss format)</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Checked out time (in yyyy-mm-dd hh:mn:ss format)</p>
</blockquote></li>
<li><blockquote>
<p>Click the check box on the column header of the result table to
select all records and click the [Export] button to export all records
on all pages or single/multiple select the row(s) and click the [Export]
button to export the selected records into csv or excel.</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Candidate toilet request records</p>
</blockquote>
<ul>
<li><blockquote>
<p>By filtering, a list of the exam session shall be displayed including
subject name, subject code, paper, school name, school code, centre
code, centre type, exam date and exam time.</p>
</blockquote></li>
<li><blockquote>
<p>Searching fields shall include exam date, exam start and end time,
subject code, paper group, school code, school name, centre code, and
centre type.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to select columns displayed by toggling the
‘Preferences’ button.</p>
</blockquote></li>
<li><blockquote>
<p>[View] button shall be available for the detailed toilet request
records in the corresponding exam session. Following fields shall be
displayed:</p>
</blockquote></li>
<li><blockquote>
<p>Candidate No./ID No., candidate name, normal or special case, action
(IN/OUT), recording time in hh:mm:ss format and recorded by (EP no. and
name of CS/invigilator)</p>
</blockquote></li>
<li><blockquote>
<p>Click the check box on the column header of the result table to
select all records and click the [Export] button to export all records
on all pages or single/multiple select the row(s) and click the [Export]
button to export the selected records into csv or excel.</p>
</blockquote></li>
</ul></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>ESB (SEAD)</th>
<th>134</th>
<th>13.4.6</th>
<th>Suspend Session</th>
<th><ol type="1">
<li><blockquote>
<p>By filtering the Centre Type of an exam school, a list of suspended
records shall be displayed.</p>
</blockquote></li>
<li><blockquote>
<p>Suspend an exam session</p>
</blockquote>
<ul>
<li><blockquote>
<p>Click the [Add] button</p>
</blockquote></li>
<li><blockquote>
<p>Search an exam session by selecting the exam date, subject, paper,
centre type of an exam school.</p>
</blockquote></li>
<li><blockquote>
<p>a list of the centres shall be displayed.</p>
</blockquote></li>
<li><blockquote>
<p>Click the check box on the column header of the result table to
select all records and click the [Suspend] button to suspend all the
exam sessions of all pages or single/multiple select the exam session(s)
to suspend the selected exam session(s)..</p>
</blockquote></li>
<li><blockquote>
<p>Suspended result(s) shall be displayed.</p>
</blockquote></li>
<li><blockquote>
<p>Suspended information shall be displayed in the CS page and the
invigilator app.</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Unsuspend an exam session</p>
</blockquote>
<ul>
<li><blockquote>
<p>By filtering the Centre Type of an exam school, a list of suspended
exam session(s) shall be displayed.</p>
</blockquote></li>
<li><blockquote>
<p>Click the [Edit] button for unsuspend exam session(s).</p>
</blockquote></li>
<li><blockquote>
<p>Single / multiple select the suspended exam session(s) to unsuspend
the selected exam session(s), or click the check box on the column
header to select all the exam sessions to unsuspend the exam
sessions.</p>
</blockquote></li>
<li><blockquote>
<p>Confirm to unsuspend the selected exam session.</p>
</blockquote></li>
<li><blockquote>
<p>Unsuspended information shall be displayed in the CS page and the
invigilator app.</p>
</blockquote></li>
</ul></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="header">
<th>ESB (ESU)</th>
<th>136</th>
<th>13.5.1</th>
<th>Login</th>
<th><ol type="1">
<li><blockquote>
<p>Users shall be able to enter their username and password to identify
their role, and the access to specific functions and data are set by the
IT Admin.</p>
</blockquote></li>
<li><blockquote>
<p>Function access is limited to the SEN system only.</p>
</blockquote></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>ESB (ESU)</th>
<th>137</th>
<th>13.5.2</th>
<th>Dashboard</th>
<th><ol type="1">
<li><blockquote>
<p>Users shall be able to view the records by filtering VCC
<mark>confirmation</mark> status, exam date, operator, school code,
school name, centre code, centre type, subject code, subject name, and
paper code.</p>
</blockquote></li>
<li><blockquote>
<p>Pie charts shall be able to reflect the statistics of the filtering
result:</p>
</blockquote></li>
</ol>
<ul>
<li><blockquote>
<p>Attendance discrepancy</p>
</blockquote>
<ul>
<li><blockquote>
<p>Unverified</p>
</blockquote></li>
<li><blockquote>
<p>Present and Absent</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Overall situation</p>
</blockquote>
<ul>
<li><blockquote>
<p>Pending to Confirm</p>
</blockquote></li>
<li><blockquote>
<p>Confirmed without Discrepancy</p>
</blockquote></li>
<li><blockquote>
<p>Confirmed but with Attendance and/or Script Discrepancy</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Irregularity by Helpdesk</p>
</blockquote>
<ul>
<li><blockquote>
<p>Confirmed but with Attendance and/or Script Discrepancy</p>
</blockquote></li>
</ul></li>
</ul>
<ol start="3" type="1">
<li><blockquote>
<p>A table displaying the real-time exam information of all /
designated:</p>
</blockquote></li>
</ol>
<table>
<colgroup>
<col style="width: 23%" />
<col style="width: 76%" />
</colgroup>
<thead>
<tr class="header">
<th>Field Name</th>
<th>Description</th>
</tr>
<tr class="odd">
<th>VCC confirmed time</th>
<th>The timestamp of confirmation of exam data accuracy by VCC</th>
</tr>
<tr class="header">
<th>Operator</th>
<th>The helpdesk account assigned to monitor the exam session</th>
</tr>
<tr class="odd">
<th>Subject Code</th>
<th>Unique code of the subject as recorded in the HKDSE system</th>
</tr>
<tr class="header">
<th>Paper Group</th>
<th>Paper code of the subject</th>
</tr>
<tr class="odd">
<th>Centre Code</th>
<th>Unique code of the exam centre as recorded in the HKDSE system</th>
</tr>
<tr class="header">
<th>Centre Type</th>
<th>Type of teh exam centre, such as HALL, CLASSROOM, etc.</th>
</tr>
<tr class="odd">
<th>Assigned Candidate</th>
<th>No. of candidates assigned to the exam centre.</th>
</tr>
<tr class="header">
<th>Present Count</th>
<th>No. of candidate with attendance status ‘Present’</th>
</tr>
<tr class="odd">
<th>Absent Count</th>
<th>No. of candidate with attendance status ‘Absent’</th>
</tr>
<tr class="header">
<th>Moved to SR Count</th>
<th><p>No. of candidates who were moved by the CS from the assigned exam
centre to the special room.</p>
<p>For SEN, it should be zero.</p></th>
</tr>
<tr class="odd">
<th>Unverified Attendance</th>
<th><p>The total number of assigned candidates whose attendance status
have not yet been updated as present or absent</p>
<p>i.e. missing attendance</p></th>
</tr>
<tr class="header">
<th>Absent but with script collected</th>
<th>The total number of scripts collected that the assigned candidates
who are absent from the exam session</th>
</tr>
<tr class="odd">
<th>Special Case Count</th>
<th>Total no. of special cases in the exam centre, i.e. wrong centre
candidate</th>
</tr>
<tr class="header">
<th>Special Case At Hall/Classroom</th>
<th>No. of special case created by the CS in the exam centre</th>
</tr>
<tr class="odd">
<th>Special Case at SR</th>
<th><p>No. of special cases created by the special room invigilator in
the special room of the exam centre.</p>
<p>For SEN, it should be zero.</p></th>
</tr>
<tr class="header">
<th>Total Script to be Collected</th>
<th>Total no. of script to be collected of the subject paper multiply
(assigned candidate and the special case).</th>
</tr>
<tr class="odd">
<th>Missing Script</th>
<th>Total no. of missing scripts that should be collected of the
assigned candidates (with present status) + Total no. of missing scripts
that should be collected of the special cases (wrong centre
candidates)</th>
</tr>
<tr class="header">
<th>Script Collected from Present Candidate</th>
<th>The total number of scripts collected that the assigned candidates
whose attendance status is present + Total number of scripts collected
from the special cases(wrong centre candidates)</th>
</tr>
<tr class="odd">
<th>Remarks from CS</th>
<th>Written remarks inputted by a CS when confirming the exam data
accuracy</th>
</tr>
<tr class="header">
<th>Notification to CS</th>
<th>The CS of the exam centre was notified for exam
dismissal(Yes/No)</th>
</tr>
<tr class="odd">
<th>Confirm to ESU</th>
<th>Confirm status from VCC to ESU (Pending to Confirm/Confirmed to
ESU)</th>
</tr>
<tr class="header">
<th>Confirmed by</th>
<th>VCC staff who confirm the exam data to ESU</th>
</tr>
<tr class="odd">
<th>VCC Confirmation Remark</th>
<th>VCC’s input remark when confirm exam data to ESU</th>
</tr>
</thead>
<tbody>
</tbody>
</table>
<blockquote>
<p> </p>
</blockquote>
<ol start="4" type="1">
<li><blockquote>
<p>Users shall be able to sort the table by the field labels.</p>
</blockquote></li>
</ol>
<ol start="5" type="1">
<li><blockquote>
<p>Users shall be able to select columns displayed by toggling the
‘Preferences’ button.</p>
</blockquote></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="header">
<th>ESB (ESU)</th>
<th>139</th>
<th>13.5.3</th>
<th>Attendance Records</th>
<th><ol type="1">
<li><blockquote>
<p>Users shall be able to select to display the attendance record
between the allocated candidates and the special case by clicking the
corresponding tabs.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to view the records by filtering the exam year,
exam date range, centre code, subject code, paper group, candidate no.,
seat no., attendance status (i.e. present, absent, not yet taken),
answer script collection status and the special room (centre type).</p>
</blockquote></li>
<li><blockquote>
<p>Exam data shall be displayed in the result table, such as:</p>
</blockquote>
<ul>
<li><blockquote>
<p>School name</p>
</blockquote></li>
<li><blockquote>
<p>Subject name</p>
</blockquote></li>
<li><blockquote>
<p>Paper group</p>
</blockquote></li>
<li><blockquote>
<p>Centre code</p>
</blockquote></li>
<li><blockquote>
<p>Mode (applicable to listening paper)</p>
</blockquote></li>
<li><blockquote>
<p>Candidate number</p>
</blockquote></li>
<li><blockquote>
<p>Candidate surname</p>
</blockquote></li>
<li><blockquote>
<p>Candidate name</p>
</blockquote></li>
<li><blockquote>
<p>Seat number</p>
</blockquote></li>
<li><blockquote>
<p>Attendance status (U - attendance record not yet taken, present,
absent)</p>
</blockquote></li>
<li><blockquote>
<p>Answer script collection status (answer scripts collected / answer
scripts to be collected)</p>
</blockquote></li>
<li><blockquote>
<p>Location (applicable to normal exam centre)</p>
</blockquote></li>
<li><blockquote>
<p>Number of answer script collected by ESU</p>
</blockquote></li>
<li><blockquote>
<p>Subject code</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Exam data displayed in the result table shall be sorted by the
fields.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to select columns displayed by toggling the
‘Preferences’ button.</p>
</blockquote></li>
<li><blockquote>
<p>Exam data displayed in the result table shall be able to be exported
as a CSV file.</p>
</blockquote></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>ESB (ESU)</th>
<th>140</th>
<th>13.5.4</th>
<th>Discrepancy Report</th>
<th><ol type="1">
<li><blockquote>
<p>Users shall be able to view the discrepancy records by filtering the
exam date, exam time, centre code, centre type, subject code, paper
group and the candidate no.</p>
</blockquote></li>
<li><blockquote>
<p>Discrepancy records related to allocated candidates and special cases
shall be displayed. Users shall be able to select among two types of
cases by clicking the corresponding tabs.</p>
</blockquote></li>
<li><blockquote>
<p>Discrepancy records shall be displayed in the result table, such
as:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Candidate number</p>
</blockquote></li>
<li><blockquote>
<p>Candidate name</p>
</blockquote></li>
<li><blockquote>
<p>Subject name</p>
</blockquote></li>
<li><blockquote>
<p>Subject code</p>
</blockquote></li>
<li><blockquote>
<p>Paper group</p>
</blockquote></li>
<li><blockquote>
<p>School name</p>
</blockquote></li>
<li><blockquote>
<p>School code</p>
</blockquote></li>
<li><blockquote>
<p>Centre code</p>
</blockquote></li>
<li><blockquote>
<p>Centre type</p>
</blockquote></li>
<li><blockquote>
<p>Mode (applicable to the listening paper)</p>
</blockquote></li>
<li><blockquote>
<p>Spare barcode number</p>
</blockquote></li>
<li><blockquote>
<p>Seat number</p>
</blockquote></li>
<li><blockquote>
<p>Attendance status (‘- -’ means attendance record not yet taken,
present, absent)</p>
</blockquote></li>
<li><blockquote>
<p>Answer script collection status (answer scripts collected / answer
scripts to be collected)</p>
</blockquote></li>
<li><blockquote>
<p>Remarks - there are 4 types of discrepancy</p>
</blockquote>
<ul>
<li><blockquote>
<p>Missing attendance record(s)</p>
</blockquote></li>
<li><blockquote>
<p>Missing attendance but with script collected</p>
</blockquote></li>
<li><blockquote>
<p>Missing script records</p>
</blockquote></li>
<li><blockquote>
<p>Absent but with script(s) collected</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Location (applicable to the normal exam centre)</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Discrepancy records displayed in the result table shall be sorted by
the fields.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to select columns displayed by toggling the
‘Preferences’ button.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to export the discrepancy records displayed in
the result table to a CSV file.</p>
</blockquote></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="header">
<th>ESB (ESU)</th>
<th>142</th>
<th>13.5.5</th>
<th>Event Log</th>
<th><ol type="1">
<li><blockquote>
<p>Users shall be able to view the event log by filtering the exam date,
exam time, school code, centre code, centre type, subject code, paper
group and the candidate no.</p>
</blockquote></li>
<li><blockquote>
<p>Event log shall be displayed in the result table, such as:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Event date and time (in yyyy-mm-dd hh:mn:ss format)</p>
</blockquote></li>
<li><blockquote>
<p>Centre code</p>
</blockquote></li>
<li><blockquote>
<p>School code</p>
</blockquote></li>
<li><blockquote>
<p>Candidate number / EP no. of CS or invigilator</p>
</blockquote></li>
<li><blockquote>
<p>Actor type (candidate, CS, DCS, VCC)</p>
</blockquote></li>
<li><blockquote>
<p>Event</p>
</blockquote></li>
<li><blockquote>
<p>Location (HALL, SEN CLASSROOM)</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>The event log displayed in the result table shall be sorted by the
fields.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to select columns displayed by toggling the
‘Preferences’ button.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to export the event log displayed in the result
table to a CSV file.</p>
</blockquote></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
<tr class="odd">
<th>ESB (ESU)</th>
<th>142</th>
<th>13.5.6</th>
<th>Report List</th>
<th><ol type="1">
<li><blockquote>
<p>Different report types shall be developed and selected for
downloading.</p>
</blockquote></li>
<li><blockquote>
<p><mark>Audit Report</mark></p>
</blockquote>
<ul>
<li><blockquote>
<p><mark>Users</mark> shall be able to retrieve the data by filtering
candidate no., subject code, paper group, attendance status and the exam
data range.</p>
</blockquote></li>
<li><blockquote>
<p>Records shall be displayed with:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Action (event)</p>
</blockquote></li>
<li><blockquote>
<p>Action time (in yyyy-mm-dd hh:mn:ss format)</p>
</blockquote></li>
<li><blockquote>
<p>Exam year</p>
</blockquote></li>
<li><blockquote>
<p>Subject code</p>
</blockquote></li>
<li><blockquote>
<p>Paper group</p>
</blockquote></li>
<li><blockquote>
<p>Centre code</p>
</blockquote></li>
<li><blockquote>
<p>Seat number</p>
</blockquote></li>
<li><blockquote>
<p>Exam date (in yyyy-mm-dd format)</p>
</blockquote></li>
<li><blockquote>
<p>Candidate number</p>
</blockquote></li>
<li><blockquote>
<p>Candidate name</p>
</blockquote></li>
<li><blockquote>
<p>Invigilator number</p>
</blockquote></li>
<li><blockquote>
<p>Attendance status (present, absent, not yet taken)</p>
</blockquote></li>
<li><blockquote>
<p>Scanning status</p>
</blockquote></li>
<li><blockquote>
<p>Remarks</p>
</blockquote></li>
<li><blockquote>
<p>Last update by</p>
</blockquote></li>
<li><blockquote>
<p>Last update date</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Function of quick download shall be provided without showing the data
on screen.</p>
</blockquote></li>
</ul></li>
</ol>
<ol start="3" type="1">
<li><blockquote>
<p>Attendance Summary Report</p>
</blockquote>
<ul>
<li><blockquote>
<p>Users shall be able to retrieve the data by filtering the exam date
range.</p>
</blockquote></li>
<li><blockquote>
<p>Records shall be displayed with:</p>
</blockquote>
<ul>
<li><blockquote>
<p>Subject code</p>
</blockquote></li>
<li><blockquote>
<p>Paper group</p>
</blockquote></li>
<li><blockquote>
<p>Centre code</p>
</blockquote></li>
<li><blockquote>
<p>Centre type</p>
</blockquote></li>
<li><blockquote>
<p>Centre name (school name)</p>
</blockquote></li>
<li><blockquote>
<p>No. of candidates unverified (attendance record not yet taken)</p>
</blockquote></li>
<li><blockquote>
<p>No. of candidates present</p>
</blockquote></li>
<li><blockquote>
<p>No. of candidates absent</p>
</blockquote></li>
<li><blockquote>
<p>No. of candidates move to SR (applicable to the nomal exam
centre)</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Function of quick download shall be provided without showing the data
on screen.</p>
</blockquote></li>
</ul></li>
<li><blockquote>
<p>Data displayed in the result table shall be sorted by the fields.</p>
</blockquote></li>
<li><blockquote>
<p>Users shall be able to export the data displayed as CSV file.</p>
</blockquote></li>
</ol>
<ol start="6" type="1">
<li><blockquote>
<p>SR Form shall be added (Details will be synced with the SR Form
Modules)</p>
</blockquote></li>
</ol></th>
<th><blockquote>
<p>Out Scope</p>
</blockquote></th>
</tr>
</thead>
<tbody>
</tbody>
</table>
