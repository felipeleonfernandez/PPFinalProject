# Prepaid-System

The  goal  of  this  practical  assignment  is  the  development  of  a  Java  project  (including  graphical  user interface) 
to manage a system based on credit cards and all the operations and movements that can be done with them.

## JUnit5
This project is tested by using a list of JUnit 5 tests that check the correct functioning of the program including exception cases.

     ` @Test 
     public void testChangePin() throws IncorrectPinException 
     { 
    	 CreditCard cc=new CreditCard("Pedro","Lopez","1333",(float)1000.0,"999999000000","12/2010"); 
    	 ps.getCardHistory().getList().add(cc); 
    	 assertTrue(ps.getCardHistory().getList().get(ps.getCardHistory().getList().size()-1).changePIN("1333", "0000")); 
     } `

## Continuous Integration
Continuous Integration is included in this project by creating  a " .gitlab-ci.yml" that executes a script with a mvn test 
instruction.

     maven_build:
     script: "mvn test" 

## GUI (View and Controller packages)
A graphical user interface is included in this project formed by a "View" package that contains all the frames created 
and the different messages of the tickets printed by the system. 
This package also includes **"System.java"** to use the GUI.
A "Controller" package is also included and contains the controller of the system.

## Resources
Includes the icon of the system

## Model 

- **PrepaidSystem.java**
Mehods defined in this class are specified in the interface "PrepaidSystemInterface.java".
- **CreditCard.java**
Defines an object type with attributes: String name, String surname, String pin, String number, float amount, String date
Also includes getters / setters to access or modified this attributes.
- **CardHistory.java**
Contains the list of credit cards created during a session and methods to check atributtes and search an specific card but also
two methods to save and read into the **"DataBase.txt"** file all the credit cards.

## Exceptions
- **IncorrectPinException.java**
Defines a type of exception
- **NotEnoughMoneyException.java**
Defines a type of exception
- **CreditCardUnknownException.java**
Defines a type of exception
- **CardExpiredException.java**
Defines a type of exception
- **CreditCardNumberOutOfRangeException.java**
Defines a type of exception

**Authors:**
Juan Bernal Mencía (z170277),  Felipe León Fernández (z170308) , Julen Pérez Álvarez (z170049)