![Maven Compiler Plugin](https://img.shields.io/badge/maven--compiler--plugin-8-blue.svg)

### Table of Contents
- [Features](#features)
- [Regular expression](#regular-expression)
- [Extracted Resume Sections](#extracted-resume-sections)
- [Screenshots](#screenshot)
- [Sample Output](#sample-output)
- [Dependencies](#dependencies)
- [Usage](#usage)

## Features
1. Support PDF, MS word, and text files.
2. Extract important information such as skills, education, experiences, email, phone number, etc.
3. Process multiple files at the same time.
4. Saving extracted data in JSON file.
    - Sample: [candidate.json](https://github.com/tramyardg/CVparser/blob/master/src/main/resources/candidates.json).
5. Saving extracted date in CSV file.
    - Sample: [candidate.csv](https://github.com/tramyardg/CVparser/blob/master/src/main/resources/candidates.csv).

### Regular expression
Regular expression was used to extract a section of a resume. For instance, an experience section might 
contain multiple instances of the word experience. Therefore, a strict regular expression for extracting experience 
section must be used. The solution was to get the index of the word experience 
that matches exactly to the following
```
 EXPERIENCE ("\\b(Experience(s?)|EXPERIENCE(S?))\\b")
```
The parser ignores lowercase experience or experiences after the section heading. The same notion applies for other 
section.

## Extracted Resume Sections
- Profile: contains candidate name, phone numbers, emails, objective, summary
- Experiences: candidate work experiences
- Education: candidate education
- Skills: candidate skills and/or expertise

## Screenshot
![image](https://user-images.githubusercontent.com/5623994/53571858-e30c8780-3b37-11e9-89c6-e0cc7aca0031.png)

## Sample Output
Unformatted output of three candidates. 
```
[CandidateBean [
profile=Ernani Joppert P Martins Software Engineer / Lead Architect , email=[], phoneNumber=[], links=[], objective=My professional experience is related to software development, architecture, design and performance tuning. I've also worked on data warehousing projects and business intelligence projects using commercial products such as PowerCenter and PowerDesigner. I am involved into JEE (former J2EE) Architecture, .Net, Flex, AIR, PHP Web based solutions and Mobile. Also develop on client side and webservices. I've worked on health, banking and insurance and EAI projects, along as with an internet solution provider, which tended to provide entertainment to end customers through quality of life, news, games, etc. I've worked abroad in Germany, to a small software development company in a Car insurance and Car Leasing Configuration System, using EuroTAX/Schwacke data model, Struts and Java Server Faces presentation Tier, along with Persistence using Hibernate framework and IBatis. My professional goals are to work abroad, acquire experience living and working in different countries and expand my knowledge as well as challenges. Specialties: JEE (former J2EE) framework, Java, JSP, JSF, SOAP, Axis, PHP, XML, SAML, Rest, Websphere, Jboss, BEA Weblogic, Tomcat, Struts, Eclipse, SWT, Swing, Hibernate, AMF, Flex, Adobe AIR, ActionScript development as well as DB2, Oracle, MySQL, SQL Server and other development solutions to achieve customer needs. ], 
education= Universidade Paulista Bachelor of Business Administration (B.B.A.), Business Administration and Management, General, 1999 - 2001 Interests, 
experiences= Application Integration / Web Identity at IBM Global Services January 2005 - Present (10 years 2 months) Technical consultant for Web Identity project at IBM Global Services, support and manage application integration with SSO (Tivoli Access Manager/WebSEAL) and custom based SOA Profiling for internal and external adopters, Business Partners profiling, authentication and entitlement, SAAJ and Federation also involved. 5 recommendations available upon request PHP Consultant at PHPSP - PHP User Group in São Paulo 2001 - Present (14 years) Founded the php-sp list on yahoo groups by answering their questions, also contributed to the PHP group fixing a few bugs as well as the PHP documentation translation to Brazilian Portuguese, attended some events and tried to help the users to share their knowledge. Also done some free lances here and there related to PHP, such as Wordpress setup, a blog commenting system and OSCommerce personalization. 1 recommendation available upon request Open Source App Development (Community Developer) at Spare Time Open Source Developer 2009 - 2011 (2 years) Independant Sr. Java EE/J2SE Consultant at Java/JEE Architect / Consultant 1999 - 2010 (11 years) Provided several development solutions using the Java2SE and JEE technologies, both as an Architect Role as well as a lead developer. The variations included Web Applications, j2me applications (mobile), desktop applications using SWT, Swing and AWT, Unit Testing and Batch Applications to run at scheduled periods of time to process loads of information with or without JDBC, JMS, RMI, IIOP, JBoss and MQ systems. Business Intelligence/ETL Developer at BI and DW Consultant 1999 - 2009 (10 years) Provided solutions and adjustments on several DW projects, ensuring Data Quality through ETL and BI concepts both based on relational data models and OLAP, using the common Data Warehousing techniques such as SnowFlake and StarSchema, Ad Hoc Queries and Data Quality in small and big data sets. Websphere specialist at Websphere/Java Consultant 2004 - 2004 (less than a year) Provided Advices on Java Development, training, recommendations, advices, articles and suggestions to a wide variety of friends and co-workers alike 1 recommendation available upon request System Architect and J2EE Developer at Savista Corporation (former NewPOS International) 2002 - 2004 (2 years) I've adjusted an existing reporting tool that was responsible for providing a KPI reporting, Fraud detection and other features for Domino Pizza in US. After that, transitioned to the NewPOS team which I've assisted in the development of the Java/J2EE Version of the POS at the version 8.X, also worked in a TDD environment, multi-threading Java Development and Raw TCP/IP communication mechanism. 1 recommendation available upon request Java Software Architect (Consultant) at Ericsson 2002 - 2002 (less than a year) Developed a integration between Ericsson's EHTP Setler for Interconnection and Brazil's tax rules to provide a way to calculate interconnection fees based off on call types. Worked with BMP (Billing Mediation Platform) with TCL/TK and C/C++ for file processing of CDR (Call Data Records) Also worked on a Java2 solution to address fixes of CDR's. Also worked on a project where it had the ability to process measurement of usage and critical analysis and fraud detection of measured services on telephony. Senior Web Developer at Internet Group do Brasil 2000 - 2001 (1 year) 1 recommendation available upon request Web Developer at iG 2000 - 2001 (1 year) I was responsible for the Development and Improvement of Árvore da Vida website, and then transitioned to the Software Factory Team which began developing paid services, such as numerology reports, astrology maps, and other paid services alike. 1 recommendation available upon request Technical Support and Intranet Software Development at Sudameris Corretora de Cambio e Valores Mobiliários 1996 - 2000 (4 years) Provided User Technical Support, Intranet web development, Home Broker web development with Java Applets, Ticket Emission System using MS Visual Basic, Lotus Notes and Network Administration. 1 recommendation available upon request Languages , 
skills= JSP Eclipse Tomcat Hibernate Struts MySQL Java JSF SOAP Websphere Flex JBoss XML PHP Swing AMFPHP SWT Axis EJB J2EE Web Services UML Scrum AJAX Design Patterns JavaScript SAML Subversion Spring PL/SQL Delphi CVS Servlets jQuery Ant Apache JSON Linux SOA Maven DB2 REST CSS SQL Server Weblogic C++ Git J2ME Objective-C Java Enterprise Edition Education Universi], CandidateBean [
profile=Maria E. Parker Campus Address mepnd@nd.edu Permanent Address 256 Fitzpatrick Hall 1060 W. Addison St. Notre Dame, IN 46556 Chicago, IL 60613 (574) 631- 6039 (773) 404-2827 Github: https://github.com/tramyardg , email=[mepnd@nd.edu], phoneNumber=[(574) 631- 6039, (773) 404-2827], links=[ https://github.com/tramyardg], objective=To obtain a summer internship in Mechanical Engineering. ], 
education= University of Notre Dame Bachelor of Science in Mechanical Engineering GPA: 3.1/4.0, to be awarded May 2006 Dean's List: Spring 2004 Study Abroad Program London, England COURSEWORK Engineering Graphics (Pro-E) Thermodynamics Mechanical Design Computing & Programming Control Systems I, II Heat Transfer COMPUTER Languages, 
experiences= Alivaf Technology Corporation, San Antonio, TX, June-September 2004 Engineering Intern: Design widgets using Pro-Engineer to meet design specifications. Selected and tested appropriate materials to optimized strength-to-weight ratio. Tested widgets using IBRAKEM testing apparatus. University of Notre Dame, Notre Dame, IN, Fall 2004 Undergraduate Research Assistant: Conducted preliminary research on fuel cells. Assisted in setting up apparatus for rheology experiments using polymers and fiber composites. Took permeability measurements of deformed fabrics. MEMBERSHIP, 
skills= Systems: MS-DOS, UNIX, Macintosh, Windows: 9x, XP, 2000, & NT Software: ProEngineer Wildfire, AutoCAD, MS Word, MS Excel EXPERI], CandidateBean [
profile=Alex Dubinchyk Pleasant Hill, CA alexs.dbk@gmail.com Status:Green Card Holder , email=[alexs.dbk@gmail.com, leo@gmail.com], phoneNumber=[], links=[ http://www.actuate.com/,  http://www.bloomsky.com,  http://www.telecontact.ru/, (http://www.rozumsoft.com/).,  http://www.a-h.by;, (http://www.mogu.by;,  http://www.a-h.by).,  https://github.com/aldb,  https://www.linkedin.com/pub/alex-dubinchyk/a0/54b/760/en], objective=Seeking a challenging position to use my software Web development and process optimization skills. SUMMARY I worked on a wide range of products including building advanced dynamic multi language web sites, internal and external API's, well as creating new internal workflows. My goal is to work in a passionate team, that loves their work and the products they are creating together, supporting, mentoring, optimizing workflows and creating high quality software. I'm energenic, solution oriented team-player, constantly learning and growing as a team, and bringing high spirits along with me. Technology Server side PHP programming, REST, OPP, MVC, Yii framework. SQL Database programming: MySQL, SQL, MSSQL. Client-side programming: JavaScript, AJAX, jQuery. Smarty Template Engine, HTML5, CSS3. leo@gmail.com Webserver installation and configuration: Apache, Nginx, IIS. Source control: SVN/Subversion, GIT. Platforms: Linux, Mac, Windows. ], 
education= Belarusian University of Informatics and Radioelectronics, BS in Modeling and computer-aided design of radioelectronics devices. Profiles https://github.com/aldb https://www.linkedin.com/pub/alex-dubinchyk/a0/54b/760/en skype: cool-skype-id, 
experiences= Actuate http://www.actuate.com/ Full stack PHP Developer San Manteo, CA. November 2014 - current Implemented web service(API, MVC, Php) Introduced Git to the team BloomSky http://www.bloomsky.com Backend Developer Sunnyvale, CA. October 2014 - November 2014 Integrated APIs (PHP, Python, Django, Nginx) Set up PHPUnit and functional testing Deploy merge DB script (MSSQL>MySQL) Rozumsoft LLC, / Telecontact LLC http://www.telecontact.ru/ Full stack PHP Developer Belarus, Minsk. February 2012 - September 2014 Programming modules of dynamically building statistics for quality control assessment project. Designed and developed project quality control assessment that estimated effective work of operators in callcenters from different regions. Includes modules separation mapping based on more 20 users roles(RBAC), online editors(logs, statistical formulas, projects rules and etc) for more 10k clients. Finalization coding script of internal protection algorithm authorization and validation. Programming API service for quality control assessment. Interact with user interface(AJAX) with fast load up JSON data, audio files and extract large data in excel. API data exchange integrated with data parse, merge, view in table linkage, send emails. Support more 100 source, near 1000 onlineusers, more 10 servers. Codes cross-browsers users interfaces in project quality control assessment, using Javascript, jQuery, JSON, Bootstrap. Developed JavaScript audio player with individual custom design, hardware acceleration, deceleration and the order to play audio files. Designed and developed the company website (http://www.rozumsoft.com/). Implemented 3 domain zones(ru/by/com) algorithm. Codes contents editor for 3 languages Fixed and support custom seo map logic. Developed scripts products to callcenters operators Development of сomplex reports and statistical summaries by Cisco data telephony. Redesigned and reimplemented projects using MVC approach and strong OOP design Designed and conversion of scripts database, extensive SQL query optimization. Real Estate Agency Assistant heals LLC, Full stack PHP Developer Belarus, Minsk, http://www.a-h.by; May 2011 - January 2012 Dynamic website design and programming using PHP, MySQL, HTML, CSS. Setup and administration of web servers and server software. Business consulting of securing/ planning project. Development to online marketing, search engine placement and promotion (http://www.mogu.by; http://www.a-h.by). EDUCATION , 
skills=null]]
```

## Dependencies
- SWT: graphical widget toolkit used for building GUI
- Apache PDFBox: for reading PDF files
- Apache POI: for reading Microsoft Word files
- JSON-java: library also known as org.json
- OpenCSV: for writing/reading CSV files
- JavaFaker: for unit testing
- Log4j: for logging

## Usage
1. Clone or download CVparser repo.
2. Add a sample resume in public folder.
3. Make sure you have Maven installed.
4. Minimum JDK requirement: JavaSE-1.8 (JDK 8).
5. Update/Install Maven dependencies.
6. Run the main program located at `CVparser/src/main/java/com/cv/parser/CVParserMain.java`
7. CVParser window opens up
- 1) Click the button `Read from public`
- 2) Click the button `Extract contents`
- 3) Finally, click the button `Save in JSON file` and/or `Save in CSV file`.
8. Extracted cv(s) can be found at `CVparser/public` as `candidates.json` and/or `candidates.csv`
