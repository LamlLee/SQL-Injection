# What is SQL Injection?

Structured Query Language (SQL) is a textual language used by a      database server. SQL commands used to perform operations on the      database include INSERT, SELECT, UPDATE, and DELETE. These commands  are used to manipulate data in the database server.
      SQL injection attacks use a series of malicious SQL queries or SQL    statements to manipulate the database directly. An application    often    uses SQL statements to authenticate users to the    application,    validate roles and access levels, store and obtain    information for    the application and user, and link to other data    sources. SQL    injection attacks work because the application does    not properly    validate an input before passing it to an SQL    statement.

# Examples of SQL Injection
An SQL injection query exploits the normal execution of SQL. The attacker uses various SQL commands to modify the values in the databases.
The following table lists some examples of SQL injection attacks:
![Screenshot 2024-05-16 094930](https://github.com/LamlLee/SQL-Injection/assets/108409882/5f7a8e09-1bd1-4761-96b9-dcfa584ef813)


## Types of SQL Injection


There are three main types of SQL injection:

- In-band SQL Injection: An attacker uses the same communication    channel to perform the attack and retrieve the results. In-band    attacks are commonly used and easy-to- exploit SQL injection attacks.    The most commonly used in-band SQL injection attacks are error-based    SQL injection and UNION SQL injection.
- Blind/Inferential SQL Injection: In blind/inferential injection, the attacker has no error messages from the system to work on.    Instead, the attacker simply sends a malicious SQL query to the    database. This type of SQL injection takes a longer time to execute    because the result returned is generally in Boolean form. Attackers    use true or false results to determine the structure of the database    and the data. In the case of inferential SQL injection, no data is    transmitted through the web application, and it is not possible for    an attacker to retrieve the actual result of the injection;    therefore, it is called blind SQL injection.
- Out-of-Band SQL Injection: Attackers use different communication    channels (such as database email functionality or file writing and      loading functions) to perform the attack and obtain the results. This    type of attack is difficult to perform because the attacker needs to     communicate with the server and determine the features of the       database server used by the web application.

The diagram below shows the different types of SQL injection:
![image](https://github.com/LamlLee/SQL-Injection/assets/108409882/3c156a09-d222-4a09-b78f-37aa1d520b93)

## SQL Injection Methodology 


The SQL injection methodology consists of the following steps:
- Information gathering and SQL injection vulnerability detection 
- Launching SQL injection attacks
- Compromising the entire target network (Advanced SQL injection)



## Evasion Techniques


Firewalls and intrusion detection systems (IDS) can detect SQL injection attempts based on predefined signatures. Even if networks include these network security perimeters, attackers use evasion techniques to perform SQL injection without being detected. Such evasion techniques include hex encoding, manipulating white spaces, in-line comments, sophisticated matches, char encoding, and so on. 

Different types of signature evasion techniques are listed below:
- In-line Comment: Obscures input strings by inserting in-line comments between SQL keywords.
- Char Encoding: Uses a built-in CHAR function to represent a character.
- String Concatenation: Concatenates text to create an SQL keyword using DB-specific instructions.
- Obfuscated Code: Obfuscated code is an SQL statement that has been made difficult to understand.
- Manipulating White Spaces: Obscures input strings by inserting a white space between SQL keywords.
Hex Encoding: Uses hexadecimal encoding to represent an SQL query string.
- Sophisticated Matches: Uses alternative expression of "OR 1=1".
- URL Encoding: Obscures an input string by adding the percent sign (%) before each code point.
- Null Byte: Uses the null byte (%00) character prior to a string to bypass the detection mechanism.
- Case Variation: Obfuscates SQL statement by mixing it with upper and lower case letters.
- Declare Variables: Uses variables to pass a series of specially crafted SQL statements and bypass the detection mechanism.
- IP Fragmentation: Uses packet fragments to obscure the attack payload, which goes undetected by the signature mechanism.
- Variations: Uses a WHERE statement that is always evaluated as "true", so that any mathematical or string comparison can be used.

## SQL Injection Countermeasures


To defend against SQL injection, the developer needs to take proper care in configuring and developing an application to create one that is robust and secure. The developer should use the best practices and countermeasures to prevent applications from becoming vulnerable to SQL injection attacks.

Some countermeasures to defend against SQL injection attacks are listed below:
- Make no assumptions about the size, type, or content of the data that is received by your application.
- Test the size and data type of the input and enforce appropriate limits to prevent buffer
overruns.
- Test the content of string variables and accept only expected values.
- Reject entries that contain binary data, escape sequences, and comment characters.
- Never build Transact-SQL statements directly from user input and use stored procedures to validate user input.
- Implement multiple layers of validation and never concatenate user input that is not validated.
- Avoid constructing dynamic SQL with concatenated input values.
- Ensure that the web config files for each application do not contain sensitive information.
- Use the most restrictive SQL account types for applications.
- Use network, host, and application intrusion detection systems to monitor injection attacks.
- Perform automated black box injection testing, static source code analysis, and manual penetration testing to probe for vulnerabilities.
- Keep untrusted data separate from commands and queries.
- In the absence of parameterized API, use specific escape syntax for the interpreter to eliminate special characters.
- Use a secure hash algorithm such as SHA256 to store user passwords rather than plaintext.
- Use the data access abstraction layer to enforce secure data access across an entire application.
- Ensure that the code tracing and debug messages are removed prior to deploying an application.
- Design the code such that it traps and handles exceptions appropriately.
- Apply least privilege rules to run the applications that access the DBMS.
- Validate user-supplied data as well as data obtained from untrusted sources on the server side.


## SQL Injection Tools


Some additional SQL injection tools are listed below:
- Blind-sql-bitshifting (https://github.com)
- Splmap (https://sqlmap.org)
- Mole (https://sourceforge.net)
- NoSQLMap (https://github.com)
- SQL Power Injector (http://www.sqlpowerinjector.com)
- Tyrant SQL (https://sourceforge.net)
- SQL Brute (https://www.gdssecurity.com)


Some additional mobile-based SQL injection tools are listed below:
- DH HackBar (https://github.com)
- AndroHackbar (https://github.com)


# Module Summary

This module covered the basics and types of SQL injection, including the methodology for detecting and executing attacks. We discussed various tools and evasion techniques used by attackers, along with essential countermeasures to prevent these threats. Finally, we demonstrated tools for detecting SQL injection vulnerabilities.


