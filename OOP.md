# OOP

## TABLE OF CONTENTS

- [PRINCIPLES](#principles)
    - SOLID

<a name="principles" />

## PRINCIPLES

### SOLID

These are five important design principles for OOP. They encourage us to create more maintainable and flexible code.

- **SINGLE RESPONSABILITY**: "a class should have one and only one reason to change".
    - Example: do not combine in a class the logic of fetching data and the one that parses it and the one that uses it. Instead, separate them in three different sections.
- **OPEN/CLOSED**: "software entities should be open for extensions and closed for modifications". So, new functionalities could be added with minimum change in the existing code.
    - Example: you have a User class and you wanna add the possibility of having premium stuff. So, you should create the UserPremium class that extends from User and then write here the new methods and properties.
- **LISKOV SUBTITUTION**: "derived classes must be sustitable for their base class".
    - Example: if Dog is a subtype of Animal, we should be able to replace Dog by Animal without crashing the program.
- **INTERFACE SEGREGATION**: "make fine grained interfaces that are client specific". Clients should not be forced to implement interfaces they do notuse. So, many client specific interfaces are better than one big general interface.
- **DEPENDENCY INVERSION**: "depend on abstractions, not on concretions". This refers to decoupling modules. So, when some classes interacts with each other, they should not know the details of the others.
    - Example: if you have an Authentication service with Google or Twitter, the idea is to create an AuthService interface and then implement it in each service. Finally, you interact with those methods in  your Authentication logic.
