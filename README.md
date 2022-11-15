# idp-LectureSchedular

Introduction

This report aims to explain the project which assigned for Applied AI: Academic Perpectives lecture, module of Applied Knowledge Representation. In the scope of project, team has planned to realize a lecture scheduler. Via IDP and FO(.) language, knowledge representation of example lecture scheduling has been explained and coded logically.

Situation

In the example used, there are 3 lectures and 3 academic staff who are responsible for those lectures. According to Belgian worker law, there are 5 business days and 3 time slots (namely morning, afternoon and evening lectures) that academic staff are able to teach their lectures. Each lecture has their own course time indicating that how many time slots that a lecture is needed to be given. (I.e.: Lecture2 can have 2 slots needed to be given on Monday morning and Tuesday evening or on Friday evening and Thursday evening). With given all the lectures and academic staffs, there are lectures, time slots and academic staff to be chosen.


Good & Bad Situations

Bad Situations:
-	Lecture Program overlaps.
-	One academic staff gives lecture all day (exhaustingly).
-	Contradicted constraints occur.

Good Situations:
-	All the lectures and all the staff have been matched correctly according to constraints.
-	All limitations about lectures and staff are sorted. 

Domain Knowledge

	There are some rules (constraints) that are set accordingly to lectures and academic staff. The rules are:

-	Each lecture has exact one academic staff to be given. 
-	Each academic staff has exact one lecture to give.
-	Academic staff must not give classes all day (morning, afternoon, evening at the same day).
-	Lectures of academic staff must not overlap.
-	Each lecture have a time slot that must be fulfilled.
-	Each lecture must be given the exact amount of time slots that they have been assigned.


Users/Domain Experts

	Users of such system would be program coordinators at universities who schedule all of the lectures manually. Using this system allows users to ease their complex task, by reasoning and eliminating all of the bad situations.

	Domain Experts of such system would be academic staff, program coordinators and people who are responsible to place/assign the date of these lectures. The fundamental reason why they are experts is that they are aware of the all of the rules. Even, some rules are established and oriented according to them. “Academic staff must not give lectures all day.” is a valid example for that situation. They are domain experts, since they are all informed about the rules, even sometimes they set the rules.   

Expected Logical Inference Tasks

	In the example there are 7 lectures with their dates which are given by academic staff.	
Given 7 lectures, our team’s prototype is able to reason about lectures and staff, if they are match. Namely, the reasoning about lectures whether they are schedulable or academic staffs’ availability is the main expected logical inference task from our prototype model.

![Alt Text](https://github.com/eremkaralar/idp-LectureSchedular/blob/main/images/conflict_demo.gif)

Functionality

	Our prototype is able to reason about the lecture – academic staff matching. Model has the functionalities such as follows:

-	After the lecture selection, model is able to eliminate all the unavailable academic staff candidates.
o	Namely, only available staff can be seen.

-	While placing/assigning academic staff to lectures (Lectures have their own dates naturally.), If there is conflict in constraints such as one staff is available for the lecture slot but his schedule for the day will be full in that way (morning, afternoon and evening), candidate staff gets eliminated reasonably.

-	If there is any conflict, model is able to reason about it.
o	Namely, the reason why academic staff is unavailable to choose is explained accordingly. 


![Alt Text](https://github.com/eremkaralar/idp-LectureSchedular/blob/main/images/selection_demo.gif)

Evaluation & Discussion

	In this project, it was carried out by the team with the reasoning of matching the lecture and academic staff based on the constraints given. Vocabulary was created first as a requirement of the problem definition, and then theories were defined accompanied by quantifiers as required by the constraints in the problem. In order to reveal a logical situation and solution, it was paid attention that there were no contradictions in the theories and tests were carried out on it.

There are the following sections in the Interface, which the IDE automatically creates after code execution:

isfree: Demonstrates which academic staff is available for which particular time slot (i.e. Monday morning, Friday afternoon) to give lecture.

Courses Part;
courstime:  Timeslot requirement of each lecture.
teacher/academicstaff: Course/Academic staff matches can be seen.
scheduled: Finalized/Concluded scheduled of academic staff and lectures (if there are no inconsistency error) correspondingly.

If domain experts indicate the constraints, users are able to make a schedule without conflict or overlapping. If any conflict occurs, they are able to investigate why such violation of constraint occured.

To discuss, with the assumption of augmented number of academic staff and lectures, “classes” section might be added and extended for a future work. Since there will be numerous of teaching staff and lectures, it is possible that more than one class should be prerequisite.

Although it is a time limitation, the program in the created project can be the basis for various scheduling problems due to its future work and expandability. Ultimately, even tough the problems’ constraints are different, the fundamental approximation to the solution is similar. Plus, this program is able to be adapted to many different scheduling problems.






