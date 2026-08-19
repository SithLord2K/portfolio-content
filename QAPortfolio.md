# Chris Wiley — QA Automation & Software Testing Portfolio

**Location:** Welland / Pelham, ON, Canada  
**Email:** wileysoftware@gmail.com | sithlord2k@gmail.com  
**Phone:** +1 (289) 241-8953  
**GitHub:** [github.com/SithLord2K](https://github.com/SithLord2K)  
**Portfolio:** [chriswiley.codersden.com](https://chriswiley.codersden.com)  
**LinkedIn:** [linkedin.com/in/cw-hacks](https://www.linkedin.com/in/cw-hacks)  

---

## Executive Summary

**Quality Assurance Automation Specialist & Technical SME** with over 7 years of dedicated software testing experience and a foundational background of nearly 30 years in Information Technology. 

Proven track record of designing robust automated test suites, developing custom internal test utilities in C# and WPF, validating complex multi-tiered enterprise applications (Web, Desktop, POS), and managing extensive hardware testing environments. Expert in bridging the gap between deep exploratory manual testing, developer-level application architecture, and scalable automated frameworks.

---

## Technical Competency Matrix

| Category | Technologies & Methodologies |
| :--- | :--- |
| **Automation & Frameworks** | TestComplete (C# Scripting, Python), Playwright, Selenium WebDriver, Custom Test Harnesses |
| **Languages & Scripting** | C#, Python, SQL (T-SQL), Bash, PowerShell, JavaScript/TypeScript |
| **API & Integration Testing** | Postman (REST API validation, JSON assertions, test runners), Microservices, Webhooks |
| **Databases & Data Integrity** | Microsoft SQL Server, MySQL, Entity Framework Core, complex T-SQL joins, data seeding |
| **Test Management & CI/CD** | Azure DevOps (Test Plans, Defect Tracking, Repos), Jira, Confluence, Git, GitHub Actions |
| **Testing Methodologies** | Shift-Left Testing, End-to-End (E2E), Functional, Regression, Smoke, Exploratory, UAT, Boundary Value Analysis |
| **Hardware & POS Labs** | Enterprise POS terminals, Payment Peripherals (Moneris, Chase, TD), Epson printers, barcode scanners |
| **Security & Diagnostics** | OWASP Top 10, Burp Suite, OWASP ZAP, Nmap, Network packet capture (Wireshark), Log analysis |
| **AI-Augmented QA** | Prompt engineering for edge-case discovery, synthetic test data generation, automated script scaffolding |

---

## Featured QA & Automation Projects

### 1. Enterprise POS Automated Regression Framework
* **Context:** Panasonic Canada ISD (Integrated Services Division)
* **Tools:** TestComplete, C# Scripting, Python, Windows Shell, SQL Server
* **Overview:** Designed, developed, and maintained core automated test suites for enterprise-scale proprietary Point of Sale (POS) software handling high-volume transaction processing and mission-critical workflows.
* **Key Achievements:**
  * Achieved approximately **40% automated test coverage** across critical application paths, significantly accelerating regression cycle turnarounds.
  * Authored custom object identification mapping and dynamic synchronization routines to eliminate test flakiness across varied hardware display resolutions.
  * Built custom execution helpers in C# script and Python to interface with Windows OS shell routines and validate process exit codes dynamically.
  * Integrated backend database validation checks to verify financial totals, tax configurations, and inventory deductions directly in SQL Server after transaction executions.

#### Automated Execution Helper Script:
```csharp
// Sample TestComplete C# Script: Dynamic Range Evaluation & Execution
function EvaluateTPNRange() {
    // 1. Retrieve Project Variables
    var tpnStart = Project.Variables.TPNStartTime;
    var tpnEnd = Project.Variables.TPNEndTime;
    var startTimeRange = Project.Variables.StartTimeRange;
    var endTimeRange = Project.Variables.EndTimeRange;

    // 2. Get the executable path dynamically from TestedApps
    var appPath = TestedApps.TCTimeEvaluate.FullFileName;

    // 3. Construct Command String with escaped parameters
    var command = "\"" + appPath + "\" " + startTimeRange + " " + endTimeRange + " " + tpnStart + " " + tpnEnd;

    // 4. Initialize Shell Object and Execute
    var WshShell = Sys.OleObject("WScript.Shell");
    var exitCode = WshShell.Run(command, 1, true);

    // 5. Validate Application Exit Code
    if (exitCode == 0) {
        Log.Message("Success: Application executed successfully and returned code 0");
    } else {
        Log.Error("Failure: Application returned non-zero exit code: " + exitCode);
    }
}
```

---

### 2. QA Configuration & Environment Utility (`QA.Configuration.Utility`)
* **Role:** Lead Architect & Developer
* **Technologies:** C#, .NET, WPF, SQL Server, T-SQL Scripting Engine
* **Overview:** Created an in-house desktop configuration application tailored specifically for the QA department to automate repetitive setup procedures, environment provisioning, and database state initialization across multiple test environments.
* **Key Achievements:**
  * **30% Reduction in Setup Overhead:** Automated multi-step database seeding, configuration file swaps, and connection string updates that previously required manual developer intervention.
  * **One-Click Test Data Prep:** Enabled testers to switch between test database profiles, wipe transactional tables safely, and apply schema patches without writing ad-hoc SQL.
  * **Error Handling & Logging:** Built detailed logging mechanisms to capture environmental mismatch errors and missing dependency flags before test execution begins.

---

### 3. Modern Web End-to-End Automation POC
* **Frameworks:** Playwright, Selenium WebDriver, TypeScript / C#
* **Target:** Modern Web Applications & Progressive Web Apps (PWAs)
* **Overview:** Proactive initiative exploring and evaluating next-generation automated testing frameworks for modern web interfaces, transitioning legacy desktop automation paradigms toward scalable cloud-ready pipelines.
* **Implementation Highlights:**
  * **Page Object Model (POM):** Implemented strict POM architecture separating test logic from UI selectors for maintainability.
  * **Resilient Selectors:** Leveraged semantic user-facing locators (roles, text, labels) to prevent brittle test suites.
  * **Cross-Browser & Responsive Validation:** Configured test suites across Chromium, Firefox, and WebKit engines, including mobile viewport emulation.
  * **CI/CD Readiness:** Structured test runs with headless execution, video capture on failure, and HTML artifact generation suitable for Azure DevOps pipelines.

---

### 4. REST API Validation & Backend Verification Suites
* **Tools:** Postman, Newman, SQL Server, JSON Schema Validator
* **Overview:** Comprehensive automated and manual API testing suites validating microservices, authentication handshakes, and third-party data integrations.
* **Implementation Highlights:**
  * **Postman Test Collections:** Built automated test scripts utilizing Postman environment variables, pre-request scripts, and test assertions validating HTTP status codes, response times, headers, and JSON body structure.
  * **Data Integrity Checks:** Correlated REST API payloads against backend database records using custom SQL queries to ensure exact data persistence and transactional atomicity.
  * **Edge & Negative Testing:** Systematically executed boundary tests, malformed payload injections, invalid tokens, and rate-limit verifications.

---

### 5. Full-Stack Application Testing Context (Welland Pool League PWA)
* **Context:** Production PWA Application ([wpl.codersden.com](https://wpl.codersden.com))
* **Technologies:** C#, .NET 10, Blazor Server, MudBlazor, SQL Server, Auth0, Google Gemini AI API, QuestPDF
* **Demonstrated QA / Engineering Synergy:**
  * Hands-on experience developing and testing complex full-stack web applications provides deep "under-the-hood" insight into how software breaks.
  * Tested OCR handwriting analysis pipelines integrated with Google Gemini AI, designing fuzzy-matching validation suites (Levenshtein distance) to test typo tolerance.
  * Validated real-time SignalR broadcasts, offline caching mechanisms, and Role-Based Access Control (RBAC) security boundaries.

---

## Hardware Lab Management & SME Leadership

* **Hardware Lab Environment:** Managed physical and virtual hardware test labs covering legacy to unreleased prototype Panasonic POS terminals.
* **Peripheral Integration Testing:** Validated hardware-software communication for:
  * **Payment Terminals:** Chase, Moneris, TD merchant interfaces
  * **Printing Systems:** Epson thermal receipt and kitchen label printers
  * **Input & Dispensing:** 1D/2D barcode scanners, cash drawers, automated coin dispensers
* **Technical Mentorship:** Served as the primary Subject Matter Expert (SME), leading the technical onboarding, lab training, and hardware debugging processes for three incoming Senior QA Analysts.

---

## Testing Philosophy & Methodologies

1. **Shift-Left Quality Culture:** Integrating QA into requirements clarification and sprint backlog refinement to catch ambiguities and architecture risks before a line of code is written.
2. **Defect Clarity & Traceability:** Authoring bug reports with clear reproduction steps, expected vs. actual outcomes, isolated log excerpts, environment metadata, and screen recordings in Azure DevOps and Jira.
3. **Defense-in-Depth Testing:** Combining automated regression safety nets with unconstrained exploratory testing, security checks (OWASP Top 10), and backend data verification.
4. **AI-Enabled Efficiency:** Leveraging prompt engineering and AI coding assistants for rapid edge-case brainstorming, synthetic test dataset creation, and script refactoring.

---

## Professional Experience History

### **Quality Assurance Automation Analyst**
**Panasonic Canada ISD (Formerly Quickservice Technologies)** | *Dec 2018 – Present*
* Lead automated and manual QA initiatives across enterprise POS software suites and web applications.
* Architect automated regression suites in TestComplete; author custom C# and Python testing logic.
* Actively drive the adoption of modern test automation frameworks (Playwright, Selenium) and CI/CD execution.
* Execute API test collections in Postman and write advanced SQL Server queries for backend verification.
* Manage hardware testing labs and mentor incoming senior engineering and QA personnel.

### **Senior Customer Service Analyst**
**Quickservice Technologies** | *Oct 2014 – Dec 2018*
* Conducted deep root-cause analysis on SQL database structures, application error logs, and system crash dumps.
* Translated complex client-reported technical anomalies into clear developer defect specifications.
* Mentored technical support staff in diagnostic logic and database troubleshooting.

### **Technical Team Lead**
**One Touch Direct** | *Jan 2012 – Jun 2014*
* Led frontline technical support teams, serving as final escalation point for intricate technical and network issues.
* Enforced stringent quality control standards, data security protocols, and SLA adherence.

---

## Education & Continuous Professional Development

* **High School Diploma / Computer Repair Studies** — Father Fogarty Secondary School
* **Practical Network Penetration Tester (PNPT)** — TCM Security *(In Progress)*
* **Certified in Cybersecurity (CC) Candidate** — ISC2
* **TryHackMe Global Ranking** — Top 7% Globally
* **Competitive CTF Achievements:** 20th place team finish in the *TCM Security Invitational CTF*; high placements in *MetaCTF Flash CTFs*
* **Enterprise Home Lab:** Configured multi-subnet home lab with Windows Server 2019 (Active Directory, DNS, Group Policy), VMware Workstation Pro, and pfSense firewall.
