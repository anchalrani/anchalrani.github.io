---
layout: post
title: Introduction to Databases
description:
modified: 2013-05-31
category: Database
tags: atomicity integrity redundancy inconsistency ATM data isolation
imagefeature: cover6.jpg
comments: true
share: true
---
# Database

A Database is a collection of interrelated data and set of programs to access those data.

It provides a way to store and retrieve database information that is both convenient and efficient.

Do you know that you directly or indirectly access atleast one database daily.
You must be wondering when

1. when you withdraw money from ATM, you are acceding bank's database.
2. when you are doing reservation on IRCTC website.
3. when you are booking your air ticket online.
4. when you register for courses in any university.
5. when you are shopping online you are aaccessing the sellers database.

You must be thinking why do we need to use database when we can store information in files. It is because we want some anomalies to be removed which exists in file system. These anomalies include

1. Data redundancy and inconsistency
2. Difficulty in accessing data
3. Data Isolation
4. Integrity problems
5. Atomicity problems
6. Concurrent access anomalies
7. Security problems


We will study why do these problems arise individually.

Let us start with first one


- **Data redundancy and inconsistency**


Different programmers may create several files and same information may be duplicated in several places.This redundancy may lead to higher storage and cost. And also it creates inconsistency that is all files copies may have different values, which must be equal.



- **Difficulty in accessing data**

Let us assume that we have information about each student in one text file each in a system. Now if we want to access names of students who study in 5 class and who have paid there fees. For this we will have to open each file and note down the name of the students who satisfy the above condition. It becomes very difficult to perform such operations on 100s and 1000s of students.

- **Data Isolation** 

Because data are scattered in various files , and files may be in different formats and due to this writing new application programs to retrieve the appropriate data is difficult.



- **Integrity Problems**

The data values stored in the database must abide by certain consistency constraints. For example, we want that minimum balance in a account must be Rs. 2000, it must never get below the specified amount. Developers enforce these constraints using various application programs. But if new constraints are added it becomes complex to change the code when it is for different types of file having different formats.



- **Atomicity**

Let us take example of a transaction to explain this property. Suppose we want to transfer Rs.400 from account A to account B. If an execution failure occurs in between the transaction, system must assure that either the transaction occurs completely or it must restore the values as were before in both the accounts. Otherwise it might happen that account A is debited Rs.400 but account B is not credited with it. It means that the transaction must happen in its entirety or not at all. It is difficult to maintain atomicity in file system.



- **Concurrent access anomalies**

When two users access the same file, there is possibility that the file may be left in an incorrect or inconsistent state. For example, two files are being edited by two users say quantity of a product is 200 . Now at the same time user A reduces it by 10 and user B reduces it by 20. In such a case if the system edits for only user A quanity becomes 190 or if it takes user B quantity becomes 180. But in either case only one transaction is read by the system. The value for quantity must have been 170 because actually the product quantity is reduced by 30.

- **Security**

Each user must not be able to view all the details of the database for it may be irrelevant for him and it may lead to unauthorised access. For example, a student must be able to see information regarding his course and marks, but not the salary status of the faculties on a university website. But since application programs are added to the file processing systems in an ad hoc manner, enforcing such security constraints is diificult.


Next we are going to study some basic terminologies in DBMS
