java cThe University of Sydney
School of Computer Science
Senior Lecturer - Security
INFO3616/CSEC3616/CSEC5616 — S2 2024
Assignment - 1
This is an individual assignment.
This assignment worths 10% of the final marks of the course.
Submit your final report as a PDF and codes as a zip file in Canvas.
You should explain any details of how to run your code in report.
Final Report and Code: Due by Week 5, Sunday the 1st of September, 2024 11:59 PM
*** IMPORTANT ***: In your answer sheet DO NOT repeat the questions. Simply include
the question number and your answer only. If you include question text in your answer sheet,
your TurnItIn score will be high and there will be additional checks. This will cause a delay in
releasing your marks. We will also impose a penalty of 10% of the total marks.
1 Security Goals (20 marks)
Analyse the following real-world IT-related incidents and data breaches where specific security goals
were compromised. For each scenario, identify the compromised security goal (e.g., Confidentiality,
Data/Message Integrity, Authenticity, Authorisation, Accountability, Non-repudiation, Deniability,
Availability, Privacy) and explain how the incident compromised that goal.
You will have to do your research by referring to various news articles and incident reports to
understand what happened in each incident. We have given some sample links to get you started but
feel free to investigate more and understand what happened in each incident. Most of the questions
will have more than one correct answer, depending on how you look at them. We will accept them if
your explanation is correct and related to the incident.
Provide clear and concise explanations for each scenario, as shown in the example.
Example 1 - CrowdStrike Falcon update failure 2024 - Link
Compromised Security goal: Availability
Explanation: Windows machines with the CrowdStrike Falcon Sensor installed went into
the boot loop with BSOD (Blue Screen of Death), making them unusable and compromising
availability.
1
Example 2 - Optus data breach 2022 - Link
Compromised Security goal: Confidentially
Explanation: Personal information of the Optus customers, such as driver’s licence number,
passport number, and address, was harvested by an attacker using an unauthenticated API
endpoint. Optus was in breach of keeping their customer’s data confidential. Here, arguments
can be made for security goals such as authorisation and privacy - but they are secondary to
confidentiality.
2 marks for each. 1 mark for correctly naming the security goal and one mark for the
explanation.
i Twitter account hijacking, 2020, Link.
ii Struxnet, 2010, Link.
iii Medicare and Pharmaceutical Benefits Scheme (PBS) data released by the Australian Department
of Health, 2016, Link 1, Link 2.
iv SolarWinds Supply Chain Attack, 2020, Link.
v Attack on Dyn DNS Provider, 2016 Link.
vi Poly Network Hack, 2021, Link 1, Link 2.
vii Silk Road Takedown, 2013, Link 1, Link 2.
viii Colonial Pipeline Cyberattack, 2021, Link.
ix Ashley Madison Breach, 2015, Link.
x Unisuper Google Could Incident, 2024, Link 1, Link 2, Link 3.
2 Social Engineering (20 marks)
ZenithTech, a prominent financial services firm, has been experiencing a surge in activity due to the
launch of a new investment platform. During this time, Sarah, an operations manager, receives a call
from someone claiming to be Chris, a representative from their external auditing firm. Shortly after,
she also receives an email supposedly from the company’s internal audit department.
Chris: "Hello Sarah, I’m Chris from your external audit firm. We’re conducting a quick review
of the new investment platform’s security protocols. Could you provide the access logs and system
architecture diagrams?”
Sarah: "I wasn’t aware of this audit. Shouldn’t this request come through our IT security team?”
Chris: "I understand your concern, Sarah. Due to the urgency of this review, we’ve been asked to
directly contact key personnel. I’ve already spoken to Michael from your internal audit team, and he’ll
send you an email confirming my request.”
2
Email:
Subject: Verification of External Auditor Request
Dear Sarah,
This is to verify that Chris is an authorized member of our external audit firm and is requesting
the necessary information for a security review. Please assist him with the requested documents.
Best regards,
Michael Johnson - Internal Audit Department
Later, Sarah discusses this situation with her colleague, James.
Sarah: "James, I got a call from an external auditor named Chris and an email from Michael
confirming it. But something doesn’t feel right. What do you think?”
James: "That’s odd. Did you verify the email’s authenticity? Maybe it’s best to check with Michael
directly.”
i Identify and describe two cognitive biases the attacker is attempting to exploit. (6 marks)
ii What additional indicators should Sarah look for to recognize this as a potential vishing attack?
List and explain two red flags. (4 marks)
iii As a security manager, what steps would you implement at ZenithTech to p代 写INFO3616、Python
代做程序编程语言revent such vishing
attempts? Provide two recommendations. (4 marks)
iv If Sarah had shared the sensitive information, what immediate actions should ZenithTech take to
mitigate potential risks? Explain three steps. (6 marks)
3 Social Engineering in Practice (20 marks)
You are a given a Twitter profile of a fictitious person.
https://x.com/frankgraphicsGP
Your task is to conduct some reconnaissance on the profile and guess the password used by this
subject to zip a file. Write a Python program that takes keyword list as the input create a list of
possible word combinations that may be used by this subject as a password.
For example, if you find possible keywords to be “blue”, “car”, the Python program should be able
to generate a list like and programmatically try to unzip the given file by entering generated passwords.
blue
car
blueblue
bluecar
carblue
carcar
3
Hint: The correct password contains lower case letters and digits. The length of the password is less
than 20 characters.
Include any details of how to run your code and the contents of the unzipped file in the PDF report
and submit your code in the code submission link given in Canvas.
4 Access Control (20 marks)
a) Definitions
i Explain: is authentication a necessary ingredient for authorisation? Give an example that proves
your argument. (2 marks)
ii It is conventional wisdom that passwords to encrypt a hard drive should be longer than passwords
for online login to websites. Explain why. (2 marks)
iii Explain what a Security Policy Model is. 1-2 sentences are enough. (2 marks)
iv Access control is often categorised into two general forms (which we called two ends of a spectrum).
What are they, and how are they different from each other? (2 marks)
v Modern CPUs have support for access control. Explain two key ideas of the common x86
architecture. (2 marks)
b) Security Policy Models
Figure 1 shows a mapping between users and clearances, and between required clearances and objects.
The clearance level increases as Basic, Confidential, Secret, Top Secret, and Ultimate Secret. Only
these mappings are defined; no other rule sets exist.
Explain if the the following statements are right or wrong, and say why.
i “In a Bell LaPadula model, Bob can read the file battle_plans.txt.” (2 marks)
ii “In a Biba model, Bob can read the file mars_habitat_plan.txt.” (2 marks)
iii “In a Bell LaPadula model, Alice can enlist the help of Elise to obtain the content of the
mars_habitat_plan.txt.” (2 marks)
iv “In a Bell LaPadula model, Alice can write to all the files as she wishes.” (2 marks)
v “In a Biba model, Elise can write to all the files as she wishes.” (2 marks)
4
ClearanceUser
BasicAlice
ConfidentialBob
SecretCharlie
Top SecretDavid
Ultimate SecretElise
Required ClearanceObject
Confidentialweekly_threat_report.txt
Ultimate Secretmars_habitat_plan.txt
Basicnext_week_press_brief.txt
Top Secretbattle_plans.txt
Figure 1: Access Tables
5 Linux Access Control (20 marks)
Below questions are associated with the provided Azure VM.
a) Basic Access Control
Below questions can be answers by Linux One liners. Provide the answer to each question and
include the command you used. Make sure that you include the command as letters/characters
(than screenshots/images), so that the markers can copy/paste command and check whether it is
working.
i What is the User ID (UID) of the user gimly. (1 mark)
ii What is the Group ID (GID) of the group hobbits. (1 mark)
iii Find which group the user legolas belongs to. (1 mark)
iv Find all the users in the group humans. (1 mark)
v Does the user frodo have sudo access? There are multiple ways to do this. Answers requiring
more than one command is also accepted. (1 mark)
b) File Permissions
For i-iii, use the linux find command with correct options and make sure that you command do not
generate any permission denied messages or other error messages. Include the commands you used in
your answer.
i Find all the files owned by user legolas. (1 mark)
ii Find all the files associated with the group elves. (1 mark)
iii Find all the files owned by user gimly. (1 mark)
iv In ii) you will find a file owned by legolas and having the group as elves. Is the next statement
is true about the file. “arwen can write to the file”. Explain your answer. (2 marks)
v In iii) you will find a file owned by gimly and having the group as dwarves. Is the next statement
is true about the file. “isildur can write to the file”. Explain your answer. (2 marks)
c) SUID Bit
5
i Find all the files own by root and having the group as humans. Similar to above your command
must not generate any permission denied messages or other error messages. (2 marks)
ii The search in i) will return two files. Explain the difference in permission strings of these two files.
(3 marks)
iii Explain and demonstrate how the permission setting in one of the files can create a security
vulnerability. (Hint: You will have to run the files and use the whoami command.) (3 marks)

         
加QQ：99515681  WX：codinghelp
