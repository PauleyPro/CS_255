# CS 255 – System Analysis and Design

## Project Overview

The DriverPass project focused on designing a web-based system for a client who wanted to improve how students prepare for their driving examinations. DriverPass needed a platform that would allow customers to purchase training packages, complete online practice examinations, and schedule driving lessons with instructors. The system also needed to support administrative operations, including managing appointments, tracking student progress, and maintaining accurate training information.

Throughout this course, I approached the project from two perspectives: understanding the client's business requirements and translating those requirements into a technical system design.

**Portfolio Artifacts:**
- **Project One – Business Requirements Document:**
  
  ```Documents the client's needs, functional and nonfunctional requirements, system objectives, and operational expectations.```
  
- **Project Two – System Design Document:**
  
  ```Translates those requirements into a proposed technical architecture, including UML diagrams, system components, user interactions, and security considerations.```

Together, these documents demonstrate the relationship between identifying a business problem and designing a software solution that addresses it.

## Reflection

### What did I do particularly well?

I believe one of my strongest contributions was recognizing the importance of designing around business operations rather than immediately focusing on the technology. Throughout the DriverPass project, I worked to understand not only what the client requested but also how customers, instructors, and administrative personnel would interact with the system.

I was particularly pleased with how I approached role separation, system security, and the relationships between different components. My UML diagrams helped me visualize how users would interact with the application, how information would move through the system, and where responsibilities needed to be clearly defined.

I also considered how the proposed architecture could support future growth without introducing unnecessary complexity. My goal was to develop a design that was technically practical, maintainable, and aligned with the client's operational needs.

### What would I revise or improve?

If I could revisit one area of my work, I would focus on refining the UML diagrams to improve their readability and consistency.

One of the challenges I encountered was balancing technical completeness with clear communication. As additional actors, relationships, and system behaviors were introduced, some diagrams became more complicated than necessary.

I would improve these diagrams by organizing related functionality more deliberately, reducing unnecessary crossing connectors, and reviewing each diagram from the perspective of its intended audience. A diagram should communicate how a system works without requiring someone to decipher the design before understanding it.

This experience reinforced an important lesson: a technically accurate design is only valuable when the people responsible for reviewing, approving, and implementing it can understand it.

### How did I interpret user needs and incorporate them into the design?

My approach began with examining the client's interviews and identifying the underlying business objectives. Rather than treating every statement as an isolated feature request, I looked at how the requirements related to the overall operation of DriverPass.

For example, allowing customers to schedule driving lessons required more than creating an appointment form. The system needed to consider instructor availability, appointment conflicts, customer permissions, and the administrative responsibilities associated with managing those appointments.

I translated these operational needs into functional requirements, user roles, system interactions, and UML diagrams. I also considered nonfunctional requirements such as accessibility, security, reliability, and maintainability.

Understanding user needs is essential because software can function exactly as programmed and still fail to solve the problem it was intended to address. Effective system design requires understanding the people who will use the application, the challenges they face, and the outcomes the organization expects.

### How do I approach designing software?

My approach to software design is **problem-first rather than technology-first**.

I prefer to begin by identifying the problem, understanding the existing workflow, and determining what a successful solution should accomplish. From there, I examine the requirements, identify dependencies and constraints, and begin developing a system architecture.

I find that visual modeling is particularly valuable during this process. Use case, activity, sequence, and class diagrams each provide a different perspective on the system. Together, they help identify missing requirements, clarify responsibilities, and reveal potential design issues before implementation begins.

In future projects, I intend to continue using an iterative approach that incorporates stakeholder feedback, requirements validation, and design reviews. I also want to place greater emphasis on traceability between business requirements and technical decisions so that each major design element has a clear purpose.

One of the most important lessons I am taking from this course is that software design is not simply about determining how to build an application. It is about understanding **what should be built, why it matters, and how to communicate that solution to the people who will ultimately develop, maintain, and use it.**
