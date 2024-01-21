# TESTING

## TABLE OF CONTENTS

- [BASICS](#basics)
  - 1 What is Software Testing?
  - 2 What are the benefits of software testing?
  - 3 What are the principles of software testing?
- [TYPES OF SOFTWARE TESTING](#types_of_software_testing)
  - 4 Manual VS Automated
  - 5 Functional VS Non Functional
  - 6 Functional Testing
  - 7 Non Functional Testing

<a name="basics"/>

## BASICS

### 1. What is Software Testing?

Software testing is a process of software development that consists on verifying software correctness, quality, and performance.

It can be said that testing enhances the quality of the product by preventing bugs, reducing development costs, and reducing performance issues.

### 2. What are the benefits of software testing?

- Customer Satisfaction
- Cost Effective
- Quality Product
- Low Failure
- Security
- Early Defect Detection

### 3. What are the principles of software testing?

1. **Absence of errors fallacy**: software needs to be bug-free 99% of the time, and it must also meet all customer requirements.
2. **Testing shows the presence of errors**: but it cannot guarantee that the software is defect-free. Testing can minimize the number of defects, but it can't remove them all.
3. **Exhaustive testing is not possible**.
4. **Defect clustering**: the majority of defects are typically found in a small number of modules in a project. According to the Pareto Principle, 80% of software defects arise from 20% of modules.
5. **Pesticide Paradox**: it is impossible to find new bugs by re-running the same test cases over and over again. Thus, updating or adding new test cases is necessary in order to find new bugs.
6. **Early testing**: in the early stages of development, defects will be detected more easily and at a lower cost.
7. **Testing is context-dependent**: software needs to be tested differently depending on its type.

<a name="types_of_software_testing"/>

## TYPES OF SOFTWARE TESTING

There are different ways to clasify the types of software testing. One clasification could be **Manual VS Automated** that is based on how the test is done, and another clasification could be **Functional VS Non Functional** that is based on what is the focus of the test.

### 4. Manual VS Automated

- **Manual**: a team or individual will manually operate a software product and ensure it behaves as expected.
- **Automated**: many different tools checks to simulating a full human-driven manual testing experience.

### 5. Functional VS Non Functional

- **Functional**: it has the goal to validate software **actions**. For example, checking the login functionality of an app.
- **Automated**: has the goal to validate the **performance** of the software. For example, checking that the dashboard should load in 2 seconds.

### 6. Functional Testing

1. **Unit Testing**

A unit test is a way of testing a unit: the smallest piece of code that can be logically isolated in a system. In most programming languages, that is a function, a subroutine, a method or property. The isolated part of the definition is important. Typically, Unit testing is done by the developer at the application development phase. Unit testing is important because we can find more defects at the unit test level.

2. **Integration Testing**

Integration testing is a type of software testing where two or more modules of an application are logically grouped together and tested as a whole. The focus is to find the defect on interface, communication, and data flow among modules. The approaches used are *top-down* or *bottom-up*.

3. **System Testing**

System testing is types of testing where tester evaluates the whole system against the specified requirements.

- **End to End Testing.** It involves testing a complete application environment in a situation that mimics real-world use, such as interacting with a database, using network communications, or interacting with other hardware, applications, or systems if appropriate.
- **Black Box Testing**. Blackbox testing is a software testing technique in which testing is performed without knowing the internal structure, design, or code of a system under test. Testers should focus only on the input and output of test objects.
- **Smoke Testing**. Smoke testing is performed to verify that basic and critical functionality of the system under test is working fine at a very high level.
- **Sanity Testing**.  It is performed on a system to verify that newly added functionality or bug fixes are working fine.
- **Happy path Testing**. The objective is to test an application successfully on a positive flow.
- **Monkey Testing**. It is carried out by a tester, assuming that if the monkey uses the application, then how random input and values will be entered by the Monkey without any knowledge or understanding of the application. The objective of Monkey Testing is to check if an application or system gets crashed by providing random input values/data.

4. **Acceptance Testing**

Acceptance testing is a type of testing where the client test the software with real time business scenarios. This is the last phase of testing, after which the software goes into production. This is also called User Acceptance Testing (UAT).

- a) **Alpha Testing**-. It is performed by the team in an organization to find as many defects as possible before releasing software to customers.
- b) **Beta Testing**. It is performed in the Real Environment before releasing the product to the market for the actual end-users. It is carried out to ensure that there are no major failures in the software or product, and it satisfies the business requirements from an end-user perspective.
- c) **Operational acceptance testing (OAT)**. It is performed by operations or system administration staff in the production environment. The purpose of operational acceptance testing is to make sure that the system administrators can keep the system working properly for the users in a real-time environment. For example, it tests: backup and restore, installing, uninstalling, upgrading software, maintenance of the software.

### 7. Non Functional Testing

1. **Security Testing**

It is done to check how the software, application, or website is secure from internal and/or external threats. This testing includes how much software is secure from malicious programs, viruses and how secure and strong the authorization and authentication processes are. Example: Penetration Testing

2. **Performance Testing**

It tests the application stability (the ability of the application to withstand in the presence of load) and response time (how quickly an application is available to users) by applying load. Performance testing is done with the help of tools such as Loader.IO, JMeter, LoadRunner, among others.

3. **Usability Testing**

It test the application from the user’s perspective. It includes:

  - a) Exploratory testing (finding defects)
  - b) Cross browser testing
  - c) Accessibility Testing

4. **Compatibility testing**

It validates how software behaves and runs in a different environment, web servers, hardware, and network environment. Compatibility testing ensures that software can run on different configuration, different databases, different browsers, and their versions.
