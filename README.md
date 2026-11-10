# IUT-Opportunity-HUB
A Java-based, terminal-driven platform connecting IUT students, alumni, and faculty through academic opportunities, research collaboration, mentorship, and skill-based recommendations.
# IUT Opportunity Hub

A Java-based, terminal-driven platform connecting IUT students, alumni, and faculty through academic opportunities, research collaboration, mentorship, and skill-based recommendations.

## Overview

IUT Opportunity Hub is a proposed platform for the IUT community. It aims to make academic and professional opportunities easier to discover, help students find people with similar interests, and make it easier to approach potential mentors and research collaborators.

The idea originated from a practical difficulty: students who want to begin research may not know which faculty members or seniors work in their area of interest, how to find potential teammates, or how to approach someone who could guide them. The application aims to make relevant people, projects, and opportunities easier to discover in one place.

**Application type:** Terminal-based Java application  
**Primary users:** Students, Alumni, Faculty  
**Data storage:** SQL relational database (PostgreSQL is the current proposal)

## Target users

- **Students:** Discover opportunities, search for mentors and collaborators, explore research projects, and submit applications or requests.
- **Alumni:** Share professional and academic experience, publish opportunities, connect with students, and provide mentorship.
- **Faculty:** Publish research projects and assistantship opportunities, identify interested students, and manage supervision or collaboration requests.

## Main modules

### 1. Opportunity Management
Handles job, internship, scholarship, and research-assistantship opportunities.

- Alumni can publish professional opportunities.
- Faculty can publish research and academic opportunities.
- Students can view, search, and filter opportunities.
- Students can apply and track application status.
- Planned application statuses: Pending, Accepted, Rejected, Withdrawn.

### 2. Alumni and Mentorship
Helps students find alumni who can guide them.

- Search and view alumni profiles.
- Send connection requests.
- Send mentorship requests.
- Alumni can respond to mentorship requests.
- Users can manage their connections.

A connection request is intended to establish a professional network connection; a mentorship request specifically asks for guidance.

### 3. Research Collaboration
Allows faculty and alumni to publish research projects and students to discover projects that interest them.

- Publish research projects.
- Browse and search projects by research domain and required skills.
- Request to join a project.
- Project owners can accept or reject participation requests.
- Students can look for supervisors and potential teammates.

### 4. Recommendation System
Recommends opportunities and mentors using information from a student's profile.

**Opportunity matching factors**
- Skills matching the opportunity's required skills.
- Relevant completed courses.
- Previous projects and experience.
- Mandatory eligibility requirements.

**Mentor matching factors**
- Shared skills.
- Shared research interests.
- Relevant academic background.
- The student's stated goals.

The system is intended to rank relevant results and explain why an item was recommended. Mandatory eligibility checks should be performed separately from relevance ranking.

## User profiles

### Student profile
Proposed attributes:
- Name
- Email (private)
- Student ID
- Department
- Academic level
- Year and batch
- Completed courses
- Skills
- Research interests
- Projects and experience

Planned operations:
- View and update profile; add or remove skills.
- Search opportunities, alumni, and faculty.
- Track application status.
- Send connection and mentorship requests.
- Browse research projects and request to join one.
- View recommended opportunities and mentors.

### Alumni profile
Proposed attributes:
- Name
- Email
- Previous student ID
- Department and batch
- Degree
- Current workplace
- Country
- Skills and experience
- Research interests
- Research/publication history

Planned operations:
- View and update profile.
- Publish job and interview notices.
- Share higher-study opportunities.
- Share professional and academic experience.
- Connect with students.
- Receive and respond to mentorship requests.

### Faculty profile
Proposed attributes:
- Name
- Email
- Faculty ID
- Designation
- Degree and qualifications
- Skills and expertise
- Research interests
- Research/publication history
- Supervision availability

Planned operations:
- View and update profile.
- Publish research projects.
- Announce research-assistantship opportunities.
- Receive and respond to mentorship and connection requests.
- Accept or reject research participation requests.
- Update supervision availability.

## Registration and login workflow

1. The application displays Register, Log in, and Exit options.
2. During registration, the user enters common information and selects Student, Alumni, or Faculty.
3. The application collects role-specific profile information.
4. The application validates the supplied information and applies the verification rules.
5. User and profile information are saved to the database.
6. During login, the application validates credentials.
7. Successful login opens the appropriate role-specific dashboard; invalid credentials produce an error.

The exact institutional verification process must be finalized. Selecting a role alone should not be treated as proof of institutional identity.

## Recommendation workflow

1. Student requests recommendations.
2. Retrieve the student's profile.
3. Retrieve available opportunities.
4. Check mandatory eligibility.
5. Calculate matching scores using relevant profile information.
6. Rank eligible opportunities.
7. Display ranked results and explain the matches.

Initial skill-match formula:

`Skill Match = Number of matched required skills / Total number of required skills`

Relevant completed courses and previous projects/experience are also proposed matching factors.

## Proposed technologies

| Technology | Purpose |
|---|---|
| Java | Main programming language and application logic |
| SQL / relational DBMS | Persistent storage |
| PostgreSQL (proposed) | Relational database; confirm with the team/supervisor |
| IntelliJ IDEA | Java development environment |
| Git | Version control |
| GitHub | Collaboration, repository hosting, issue tracking, and project history |

The current proposal is a terminal-based application, not a web application.

## Applying course concepts

- **OOP:** Model users, role-specific profiles, opportunities, research projects, and requests using classes and appropriate object-oriented principles.
- **DSA:** Implement suitable searching, sorting, matching, ranking, and graph-related operations where they solve actual application problems.
- **DBMS:** Design relational tables and relationships, use keys and constraints, and perform SQL operations to persist and retrieve data.

The team intends to implement core data structures and algorithms itself where required by the course and supervisor. The exact restrictions on built-in Java and library functions should be agreed with the supervisor.

## Planned development approach

1. Finalize requirements, class design, and database design.
2. Build registration, login, and role-specific profiles.
3. Implement opportunity management.
4. Implement alumni connections and mentorship requests.
5. Implement research project collaboration.
6. Implement and test recommendation and ranking algorithms.
7. Integrate modules, test workflows, and prepare documentation.

## Project information

- **Project:** IUT Opportunity Hub
- **Course:** Software Project Lab (SPL)
- **Batch:** SWE 24
- **Team members:** 
 Farnaz Rahman Maliha - 240042117
 Tasnova Tahia - 240042138
 Tasnita Raida - 240042113
- **Supervisor:** 
- Md. Bakhtiar Hasan

## Current status

**Proposal / initial design stage.** The modules and workflows described here represent the approved initial concept. Detailed class design, database schema, exact algorithms, validation rules, and implementation details will be refined during development.
