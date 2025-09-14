### [cite_start]Project Title: Campus Course & Records Manager (CCRM) [cite: 1]

#### [cite_start]1. Project Overview & How to Run [cite: 1, 3, 4]

[cite_start]The Campus Course & Records Manager (CCRM) is a console-based Java application to administer student and course records for an academic institution[cite: 1, 3, 4]. [cite_start]The application supports the administration of students, courses, enrollments, and grades using a menu-driven interface[cite: 4, 16, 20, 24].

[cite_start]The project illustrates core Java SE principles, such as Object-Oriented Programming (OOP), solid exception handling, contemporary I/O with NIO.2, the Streams API, and design patterns[cite: 12].

**Requirements:**
* Java Development Kit (JDK) 21 or higher.
* An Integrated Development Environment (IDE) such as Eclipse for convenient project management and running.

**How to Run:**
1. Clone the Git repository.
2. Load the project in Eclipse.
3. [cite_start]The main class of the project is `edu.ccrm.cli.CCRMApp`[cite: 48].
4. Execute the application from Eclipse by right-clicking `CCRMApp.java` and clicking "Run As > Java Application".

#### [cite_start]2. Evolution of Java, Editions & Architecture [cite: 42, 43, 44, 132, 133, 134]

* **Evolution of Java:**
    * [cite_start]Java 1.0 (1996): First release, "Write Once, Run Anywhere"[cite: 42].
    * [cite_start]Java 5 (2004): Major release with introduction of generics, enums, annotations, and autoboxing[cite: 42].
* [cite_start]Java 8 (2014): Added lambdas, the Stream API, and the Date/Time API, which are utilized in this project[cite: 42].
    * [cite_start]Java 11 (2018): Added long-term support (LTS) and modularity features[cite: 42].
    * [cite_start]Java 17 (2021): Latest LTS release with features such as sealed classes[cite: 42].

* **Java ME vs. SE vs. EE:**
* [cite_start]**Java SE (Standard Edition):** The base Java platform for developing desktop and console applications[cite: 43]. [cite_start]This is a Java SE application[cite: 11].
    * [cite_start]**Java EE (Enterprise Edition):** A platform for developing large-scale, enterprise-level applications and web services[cite: 43].
    * [cite_start]**Java ME (Micro Edition):** A platform to develop applications for mobile and embedded devices[cite: 43].

* **Java Architecture: JDK, JRE, JVM:**
    * **JDK (Java Development Kit):** The full software package used for creating Java applications. [cite_start]It contains the JRE plus the development tools needed, such as the compiler (`javac`) and the debugger[cite: 44].
    * [cite_start]**JRE (Java Runtime Environment):** Offers the required libraries and the JVM to execute Java applications[cite: 44].
* **JVM (Java Virtual Machine):** The part that runs Java bytecode. [cite_start]It serves as a bridge between the operating system and the Java application, providing platform independence[cite: 44].

#### [cite_start]3. Setup & Eclipse Configuration [cite: 45, 46, 135]

* **Windows Java Install:**
    1.  Obtain the JDK installer from the official Oracle or OpenJDK website.
2.  Run the installer and follow the on-screen instructions.
    3.  Set the `JAVA_HOME` environment variable to the JDK installation path.
    4.  Add `%JAVA_HOME%\bin` to your system's `Path` variable.
    5.  Verify the installation by opening a command prompt and typing `java -version`.
* [cite_start]*[Insert Screenshot of `java -version` output here]* [cite: 139]

* **Eclipse Project Setup:**
    1.  [cite_start]Launch Eclipse and choose "File > New > Java Project"[cite: 46].
    2.  [cite_start]Type "CampusCourseRecordsManager" in the project name field and choose your installed JDK as the JRE[cite: 46].
    3.  Press "Finish".
4. [cite_start]Develop the necessary packages by right-clicking the `src` folder and going to "New > Package"[cite: 49].
    * [cite_start]*[Insert Eclipse project creation and package hierarchy screenshots here]* [cite: 46]

#### [cite_start]4. Mapping of Project Concepts [cite: 136]

[cite_start]The following table maps required syllabus topics to their illustration in the project code[cite: 12].

| Syllabus Topic | File(s) / Class(es) / Method(s) |
|---|---|
| **OOP Pillars** | |
| Encapsulation | [cite_start]`Person.java`, `Student.java`, `Course.java` (private fields with getters/setters) [cite: 59] |
| Inheritance & Abstraction | [cite_start]`Person.java` (abstract class), `Student.java` & `Instructor.java` (extend `Person`) [cite: 60, 61] |
| Polymorphism | [cite_start]`getRole()` method override in `Student.java` & `Instructor.java` [cite: 62] |
| **Advanced Concepts** | |
| Singleton Pattern | [cite_start]`AppConfig.java` (private constructor, static `getInstance()` method) [cite: 80] |
| Builder Pattern | [cite_start]`Transcript.java` (static nested `Builder` class, private constructor) [cite: 81] |
| Checked & Unchecked Exceptions | [cite_start]`EnrollmentService.java` (throws `DuplicateEnrollmentException`, `MaxCreditLimitExceededException`) [cite: 84, 87, 88] |
| Custom Exceptions | [cite_start]`DuplicateEnrollmentException.java`, `MaxCreditLimitExceededException.java` [cite: 86] |
| NIO.2 & Streams | [cite_start]`ImportExportService.java`, `BackupService.java` (using `Path`, `Files`, `Stream`) [cite: 91, 92] |
| Recursion | [cite_start]`BackupService.java` (`listFilesByDepth` method using `Files.walk()`) [cite: 33] |
| Enums with Constructors | [cite_start]`Grade.java` (constants with grade points) [cite: 27, 74] |

#### [cite_start]5. How to Enable Assertions & Sample Commands [cite: 89, 137]

Internal self-checks in a program are done using assertions. They are turned off by default.
Running the program with assertions turned on involves using the `-ea` option when running from the command line:

`java -ea -p out -m edu.ccrm.main/edu.ccrm.cli.CCRMApp`
