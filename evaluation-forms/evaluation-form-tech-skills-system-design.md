# Evaluation Form - Tech SKills - System Design
\<Name\>

## Overview
The purpose of this interview is to determine the system design expertise of the candidate, including their experience with cloud technologies. The task is fairly simple, but provides opportunities to discuss deep topics and see how well the candidate understands DB design, DevOps, Microservices, Intra-service communication, Scalability, High-Availability, API Design, Git, etc.  
Before the interview - ask the candidate to prepare a free account with the design tool of their choice - ex. Excalidraw, draw.io, google drawings, etc. and a blank project.  
During the interview - ask the candidate to share a screen or in the case of ExcaliDraw to share a collaboration link.  

## Time - 45-60 minutes


## Guidance for Interviewers
The final outcome is not as important as the process itself - if the candidate does not completely finish the task in the given timeframe, but exhibits good skills and behaviours, they would still be eligible for hire.  
Take note of how easy it is to work with the candidate, how collaborative they are, do they listen to feedback or suggestions, etc. If we hire the person, we will have to work with them on a daily basis, so it is important to have synergy.  
Do ask questions, especially why the candidate is making particular decisions.  
If the candidate is stuck, try to help them with guiding questions - interviews can be stressful.  
Avoid giving direct pointers - prefer asking leading questions and see if the candidate would get there on their own.  
Mistakes are ok, as long as the candidate accepts feedback / guidance and corrects.  
On choosing technologies - avoid limiting the candidate to the tools that we use - ex. only to AWS. Let them choose the technologies they feel familiar with, but do ask them to defend their choices - “I’m familiar with this tool” is not a good argument most of the time.  


## Scoring Criteria
0 - Strong No Hire - The candidate cannot design a simple system; they are not familiar with basic concepts like Horizontal Scaling, DB design, APIs, CI/CD, etc.  
1 - No Hire - The candidate has some basic understanding of a particular system type and would always try to use it. They cannot make strong arguments why they are choosing a particular tool, they are not familiar with the strong and weak points, they do not know the alternatives - ex. SQL vs NoSQL DB, REST vs RPC vs GraphQL, etc.  
2 - Hire - The candidate has a good understanding of system design and can design a simple system with no guidance. They have some gaps in their knowledge, but with some guidance they can make good decisions. Might be lacking some real production experience with large scale highly available systems.  
3 - Strong Hire - the candidate has a deep understanding of system design and has practical experience applying it in large scale highly available production systems.

Final Result: \<please fill in\>

\* The score guide might change with the seniority level of the position. The provided guide is for senior developer.


## Notes
Any additional notes from the interview:  
Database design -  

API design -  

Auth -  

Microservices -  

Message Brokers -  

Scalability -  

High-Availability -  

Deployment -  

Monitoring & Alerting -  

Service Discovery -  

Logging -  

  
## System Design Task
Design a system for processing gift vouchers.  
We have clients, who want to distribute gift vouchers to their own end-users.  
We need to store all vouchers on the system.  
We need to provide an API to request 1 voucher of a particular type and denomination - ex. ChristmassSpecial 50 euro. The API will return the unique voucher code.  
The vouchers are created in 2 ways - from the UI or by importing a file. For every voucher we have the following info:  
Company name  
Campaign name  
Denomination  
Voucher Code  
We must not provide one voucher multiple times. Once returned, it is considered used and needs to be marked like so. We must not provide more vouchers than have been entered in the system.  
Ideally, we would like to be able to provide some analytics in the system in the future.  
The system must be highly available - uptime 99.999%.  
  
  
## Guide for interviewers:
Requirements - There is some ambiguity in the task requirements. A strong candidate should start by asking a lot of questions, clarifying the requirements, and building more knowledge about the needs.  
Be prepared to answer the questions.  
Example:  
How many vouchers do we plan to store? - On average 1m per client per month, 30+ clients  
What is the expected system load? - On average 1m requests per day  
Is there a difference in the information stored for different clients? - Right now no, but could be in the future  
How long do we need to keep old vouchers? - 12 months  
