# CS 255 – System Analysis and Design

## Project Overview

The DriverPass project was a system analysis and design exercise completed as part of CS 255 at Southern New Hampshire University. The client, DriverPass, wanted to develop a web-based platform that would help students prepare for their driving examinations by combining educational resources, practice testing, and behind-the-wheel instruction into a centralized system.

DriverPass needed more than a customer-facing training website. The proposed solution also had to support the business operations required to manage customers, training packages, instructors, vehicles, driving appointments, and administrative responsibilities.

The project was completed through two primary phases:

- **Project One – Business Requirements:**

  ```
  Analyze the client's interview, identify business objectives,
  document functional and nonfunctional requirements,
  and establish the scope and limitations of the proposed system.
  ```
  
- **Project Two – System Design:**

  ```
  Translate the business requirements into a proposed technical architecture,
  define system interactions through UML diagrams, and document the software,
  hardware, infrastructure, and security considerations needed for implementation.
  ```

The resulting documents demonstrate how business requirements can be translated into a structured technical design while maintaining a clear relationship between stakeholder expectations, system functionality, and implementation decisions.

**Project Scope:** This repository contains analysis, design, and presentation artifacts. DriverPass was an academic design project; the proposed application was not developed or deployed as part of this coursework.

---

## Portfolio Artifacts

This repository contains four documents representing different aspects of the system analysis and design process.

### 1. Business Requirements Document

**File:** `CS 255 Business Requirements - Jeremy Pauley.docx`

The Business Requirements Document establishes the foundation for the DriverPass system by identifying the client's operational needs and translating them into documented requirements.

Key areas include:

```
- Business objectives, system purpose, and project scope.
- Functional and nonfunctional requirements.
- Customer registration and account management.
- Training package administration and student progress tracking.
- Driving lesson scheduling and resource coordination.
- Role-based access and security requirements.
- System assumptions, limitations, and implementation constraints.
- A Gantt chart illustrating the proposed project schedule.
```

This document demonstrates the ability to interpret stakeholder requirements and establish a foundation for subsequent system design decisions.

### 2. System Design Document

**File:** `CS 255 System Design.docx`

The System Design Document translates the identified business requirements into a proposed technical solution.

The document includes:

- **Use Case Diagram:** Identifies system actors, their responsibilities, and their interactions with DriverPass.
- **Activity Diagrams:** Model the processes for completing practice examinations and scheduling driving lessons, including decision points and alternative outcomes.
- **Sequence Diagram:** Illustrates communication between the user interface, scheduling controller, and application records during lesson scheduling.
- **Class Diagram:** Defines the primary system objects, their attributes, methods, and structural relationships.
- **Technical Architecture:** Recommends the application technologies, database, cloud infrastructure, and supporting services.
- **Security Design:** Addresses authentication, authorization, customer data protection, payment processing, and operational accountability.
- **Design Assumptions:** Identifies decisions that require client confirmation before implementation.

This document demonstrates the ability to move from business analysis into system architecture while accounting for operational requirements, technical dependencies, and future maintainability.

### 3. Model Application Short Paper

**File:** `CS 255 Model Application Short Paper - Jeremy Pauley.docx`

This paper examines process modeling and object modeling as complementary approaches to analyzing and designing the DriverPass system.

Process modeling focuses on how activities and information move through a system, making it useful for examining customer registration, appointment scheduling, practice examinations, and other operational workflows.

Object modeling focuses on the system's structure, including the objects, attributes, responsibilities, and relationships necessary to support those workflows.

The paper compares the advantages and limitations of each approach and explains why both perspectives are valuable.

**Demonstrated Skill:** Evaluating modeling techniques and selecting approaches that communicate both system behavior and structural design.

### 4. DriverPass Client Presentation

**File:** `CS_255_DriverPass_Client_Presentation.pptx`

The DriverPass Client Presentation communicates the proposed system design from a stakeholder-facing perspective.

Rather than focusing exclusively on technical implementation, the presentation explains how the proposed system addresses DriverPass's business needs.

Topics include:

- System requirements and operational objectives.
- User roles and system interactions.
- Driving lesson scheduling and availability validation.
- Security, accountability, and customer data protection.
- System limitations and decisions requiring client approval.

The presentation emphasizes communicating technical decisions in language that business stakeholders can understand.

**Demonstrated Skill:** Translating technical architecture and system requirements into clear, business-focused communication.

---

## Proposed Technical Architecture

The DriverPass design recommends a centralized web application supported by managed cloud services.

| Component | Proposed Technology | Purpose |
|---|---|---|
| Frontend | React with TypeScript | Responsive customer and employee interfaces |
| Backend | Node.js with TypeScript | Application services, business rules, and system operations |
| Cloud Infrastructure | Microsoft Azure | Application hosting, storage, monitoring, and recovery |
| Database | Azure SQL Database | Centralized storage of relational business records |
| Authentication | Microsoft Entra services | Employee and customer identity management |
| Payment Processing | Stripe Checkout | Secure hosted payment processing |
| System Modeling | Lucidchart / UML | Documentation of system structure and behavior |

The architecture separates the user interface from the application services responsible for enforcing business rules.

For example, driving lesson scheduling must verify that a customer has sufficient training hours and that an instructor and vehicle are available before confirming a reservation. These rules must be enforced consistently whether the appointment is created by a customer or an authorized employee.

The design also separates business administration from technical administration through role-based access controls.

**Architecture Considerations:** The proposed Microsoft environment assumes DriverPass uses Microsoft 365 and maintains an appropriate Microsoft Entra tenant. These assumptions, along with cloud licensing, implementation costs, expected usage, and the availability of DMV integration methods, require confirmation before development.

The technology selections represent design recommendations rather than an implemented production environment.

---

## Course Reflection

### 1. Briefly summarize the DriverPass project. Who was the client, and what type of system did they want you to design?

The client was DriverPass, a business seeking to improve how students prepare for their driving examinations. DriverPass wanted a centralized web-based system that would combine educational resources, online practice examinations, and behind-the-wheel driving lessons.

The system also needed to support the administrative side of the business, including customer registration, training packages, instructor and vehicle scheduling, employee access, and reporting.

My responsibility was to interpret the client's business requirements and develop a proposed system design that could support those operations. The project required moving beyond identifying individual features and considering how the entire system would function as a coordinated solution.

### 2. What did you do particularly well?

I believe one of my strongest areas was identifying the relationships between business operations and technical requirements.

Rather than treating each feature as an independent function, I examined how the different parts of DriverPass depended on one another. Scheduling a driving lesson, for example, involves more than selecting an available appointment. The system must verify customer eligibility, account for purchased training hours, coordinate instructor and vehicle availability, and maintain an accurate reservation history.

I was also particularly pleased with my approach to separating user responsibilities. The business owner, IT officer, secretary, instructor, and customer each have different operational needs. Designing around those responsibilities helped establish clearer access boundaries and a more organized system structure.

Another area I felt I handled well was considering maintainability and implementation practicality. My proposed architecture was intended to provide a foundation that could support the client's immediate needs without unnecessarily complicating future development.

### 3. If you could choose one part of your work on these documents to revise, what would you pick? How would you improve it?

If I could revisit one area of the project, I would focus on improving the readability and organization of the UML diagrams.

One challenge I encountered was balancing technical completeness with clear communication. As additional system actors, relationships, and alternative workflows were introduced, some diagrams became more complicated than necessary.

I would improve them by organizing related functions more deliberately, reducing unnecessary connector crossings, and reviewing each diagram from the perspective of its intended audience.

I would also evaluate whether some of the more complex diagrams would benefit from being separated into smaller, focused views.

This experience reinforced an important lesson: a technically accurate diagram is not necessarily an effective diagram. The purpose of system modeling is to communicate design decisions clearly enough that stakeholders, developers, and future maintainers can understand them.

### 4. How did you interpret the user's needs and implement them into your system design? Why is it important to consider the user's needs when designing?

I began by examining the DriverPass interview and identifying the business objectives behind the client's requests.

Rather than treating each statement as an isolated requirement, I considered how it related to the broader workflow and the people responsible for performing it.

For example, the client wanted customers to schedule driving lessons online. That request introduced several additional design considerations, including customer eligibility, remaining training hours, instructor availability, vehicle assignments, appointment conflicts, and administrative scheduling support.

I translated those needs into functional requirements and then used UML diagrams to model how the system should behave and how its components would interact.

I also considered nonfunctional requirements such as security, accessibility, reliability, and maintainability. These requirements are important because a system must do more than perform the requested functions; it must perform them in a way that is dependable and appropriate for the people using it.

Understanding user needs is essential because software can operate exactly as programmed and still fail to solve the underlying business problem. Effective system design requires understanding the intended outcomes, the operational environment, and the challenges users encounter before determining how the technology should work.

### 5. How do you approach designing software? What techniques or strategies would you use in the future to analyze and design a system?

My approach to software design is **problem-first rather than technology-first**.

I prefer to begin by understanding the problem, examining the existing workflow, identifying stakeholders, and determining what a successful solution should accomplish.

Once those objectives are established, I organize the requirements, identify constraints and dependencies, and begin developing the proposed system architecture.

Visual modeling plays an important role in this process. I use different UML diagrams to examine the system from multiple perspectives:

- **Use Case Diagrams:** Identify who interacts with the system and what they need to accomplish.
- **Activity Diagrams:** Explain operational workflows, decisions, and alternative paths.
- **Sequence Diagrams:** Illustrate how system components communicate during specific operations.
- **Class Diagrams:** Establish the structural relationships and responsibilities of system objects.

I believe these techniques are most effective when used together because no single diagram communicates every aspect of a system.

In future projects, I intend to continue using an iterative design approach that incorporates stakeholder feedback, requirements validation, and technical reviews. I also want to place greater emphasis on requirements traceability so that major design decisions can be connected directly to the business needs they support.

One of the most valuable lessons I am taking from CS 255 is that software design is not simply about determining how to build an application.

It is about understanding **what should be built, why it matters, how the components should work together, and how to communicate that solution to the people responsible for developing, maintaining, and using it.**

---

## Skills Demonstrated

Through the DriverPass project, I developed and applied skills in:

- Business requirements gathering and analysis.
- Functional and nonfunctional requirements documentation.
- Stakeholder and user-role analysis.
- UML behavioral and structural modeling.
- Software architecture and technology evaluation.
- Role-based access control and security planning.
- Workflow analysis and business rule identification.
- Technical documentation and stakeholder communication.
- System assumptions, constraints, and risk identification.
- Translating business objectives into proposed technical solutions.

---

## Project Conclusion

The DriverPass project strengthened my understanding of the relationship between business analysis and software design.

The Business Requirements Document established what the client needed the system to accomplish, while the System Design Document explored how those requirements could be supported through an organized technical architecture.

The additional modeling paper and client presentation reinforced two equally important aspects of system design: selecting appropriate methods for analyzing a system and communicating the resulting design to stakeholders.

Together, these artifacts represent my approach to systems analysis and design: understand the problem, establish clear requirements, evaluate the available options, and develop a solution that supports both the people using the system and the teams responsible for implementing it.

---

## Academic Information

**Course:** CS 255 – System Analysis and Design  
**Institution:** Southern New Hampshire University  
**Program:** Bachelor of Science in Computer Science, Software Engineering Concentration  
**Author:** Jeremy R. Pauley  
**Completed:** October 2026

*This repository contains academic coursework developed for educational and professional portfolio purposes. The DriverPass system and its proposed architecture are conceptual designs and do not represent a deployed production application.*
