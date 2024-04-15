# Evaluation Form - Tech Skills - Coding Task - BE Dev
\<Name\>

## Overview
The purpose of this interview is to determine the coding expertise of the candidate, including his experience with Software Development good practices.  
The task is fairly simple, but provides opportunities to discuss deep topics and see how the candidate addresses topics like code style, refactoring, testing, etc.   
Before the interview - ask the candidate to prepare his IDE and install any necessary 3rd party software - ex. JDK 17.  
During the interview - ask the candidate to share a screen or use IntelliJ Code With Me.  

## Time - 45-60 minutes


## Guidance for Interviewers
The final outcome is not as important as the process itself - if the candidate does not completely finish the task in the given timeframe, but exhibits good skills and behaviours, they would still be eligible for hire.  
Take note of how easy it is to work with the candidate, how collaborative they are, do they listen to feedback or suggestions, etc. If we hire the person, you will have to work with them on a daily basis, so it is important to have synergy.  
Do ask questions, especially why the candidate is doing something the way they are doing it.  
If the candidate is stuck, try to help them with guiding questions - interviews can be stressful.  
Mistakes are ok, as long as the candidate accepts feedback / guidance and corrects.  
On writing tests - if there is not enough time, it is ok to ask the candidate to write 1-2 full tests, and then just write the descriptions of the rest of the tests they would do.  
Avoid giving direct pointers - prefer asking leading questions and see if the candidate would get there on their own.  


## Scoring Criteria

Criteria - Asking the right questions  
Score Guide:  
0 - Strong No Hire - did not ask any questions, resulting in not properly understanding the task  
1 - No Hire - noticed an ambiguity in the requirements, but did not ask questions, made assumptions and continued on.  
2 - Hire - after starting the task, they noticed unclear requirements, and managed to correct on time  
3 - Strong Hire - pro-actively asked the right questions, before starting on the task, and received clarification.  
Score - \<please fill in\>  
  
Criteria - Mastery of Tools (IDE, etc.)  
Score Guide:  
0 - Strong No Hire - not comfortable using the tools - not knowing how to do simple things, or where the buttons are  
1 - No Hire - only basic familiarity with the IDE, not familiar with advanced setup, not using shortcut keys  
2 - Hire - good familiarity with the IDE, some shortcut usage  
3 - Strong Hire - using the IDE feels like a second nature, most actions performed with the keyboard, very fast to perform different actions  
Score - \<please fill in\>
  
Criteria - Mastery of the Programming Language / Framework  
Score Guide:  
0 - Strong No Hire - not knowing basic stuff like variable types, access modifiers, etc.  
1 - No Hire - some theoretical knowledge, but no proper application  
2 - Hire - feels confident in using modern language constructs - ex. streams  
3 - Strong Hire - in-depth familiarity with the language syntax and possibilities, usage of advanced constructs.  
Score - \<please fill in\>  
  
Criteria - Code Style  
Score Guide:  
0 - Strong No Hire - several WTF moments  
1 - No Hire - produces hard to read and maintain code, does not realise it, does not know how to correct or what good code is  
2 - Hire - produces readable and maintainable code, might not fully understand why it is so, though; if bad code is produced, can correct after feedback or questions.  
3 - Strong Hire - knows the best practices, when and how to apply them.  
Score - \<please fill in\>  
  
Criteria - Refactoring  
Score Guide:  
0 - Strong No Hire - did not want to refactor old code at all  
1 - No Hire - reluctant to make changes in code, they did not write.  
2 - Hire - properly refactored pre-existing code, perhaps after some discussion about it.  
3 - Strong Hire - proactively noticed and refactored existing code, effectively making the code base better; Explained why they are doing it.  
Score - \<please fill in\>  
  
Criteria - Data Structures / Algorithms / Patterns  
Score Guide:  
0 - Strong No Hire - no knowledge of data structures, patterns, etc. Could not produce any algorithm to solve the task  
1 - No Hire - some basic knowledge of data structures, produced a slow algorithm, ex. O(n2), to solve the task  
2 - Hire - good knowledge of data structures and produced a good algorithm to solve the task.  
3 - Strong Hire - detailed explanation of the advantages and disadvantages of the chosen data structures and algorithm, produced the best algorithm to solve the task  
Score - \<please fill in\>  
  
Criteria - Testing  
Score Guide:  
0 - Strong No Hire - no testing experience, did not want to write tests  
1 - No Hire - some testing experience, but could not write meaningful tests  
2 - Hire - wrote the minimum amount of meaningful tests, perhaps needed to be reminded to do so  
3 - Strong Hire - proactively started using tests, without even asking about it, may be even used TDD  
Score - \<please fill in\>  
  
Total: \<please fill in\>  
  
Total Score:  
0  - 3 -> Strong No Hire  
4  - 10 -> No Hire  
11 - 17 ->  Hire  
18 - 21 -> Strong Hire  
  
\* A score of “1 - Strong No Hire”, on any of the criteria, should yield a “No Hire” result overall.  
\*\* The score guide might change with the seniority level of the position. The provided guide is for mid-senior dev.  
  



## Notes
Any additional notes from the interview:  






## Coding Task - Java Dev
We are given two logs files, containing money transaction information in a string text format.  
Each log entry contains the following info:  
Customer ID  
Transaction Timestamp  
Transaction Amount (euro)  
Store ID  
  
We want to print on the console a list of all “Loyal” customers.  
A loyal customer is a customer, who:  
made purchases on 2 separate days  
made purchases at 2 different stores  
spent a minimum of 100 euro  
  

[Link to the GitHub repo](https://github.com/manevpe/coding-task-dev-be)  

  
## Guide for interviewers:
Requirements - There is some ambiguity in the task requirements. A strong candidate should be able to notice this and proactively ask questions to clarify the requirements.  
Example questions:  
Do the 2 purchases at different stores need to happen on 2 different days? (The more interesting problem is if they can be on the same day)  
The min amount spent - is this total, or a min for a single transaction?  
How big is the data? Does it fit into memory? (For the purpose of this task it can fit into memory, but this could be a good topic to discuss after the coding is complete)  
  
Algorithm - there are several different approaches here. A good candidate would ask if we value performance or memory usage more. Also, note what data structure the candidate uses. Less experienced ones would go for arrays or lists, while more experienced candidates would choose to use a Map, making the tradeoff more memory, but better performance. If the candidate goes with a Map, it is also important to notice what they use for key and value. And if they store the storeId in a collection, do they use a Set or a List? Notice other small optimizations - ex. If a customer has been determined as loyal, do we skip all records with their id?; or do they only keep 2 stores in the Set, and save some memory?; or do they use the contains method of Set?  

Refactoring - in the provided code base, there are a few methods that are not written in the best way possible. See if the candidate would rewrite it.  
