<img width="1920" height="7877" alt="image" src="https://github.com/user-attachments/assets/156bf8b2-c0ad-40c1-b6d8-f52e87b11bcf" /><img width="1920" height="2807" alt="image" src="https://github.com/user-attachments/assets/15a9f4a6-f654-4b3a-aab4-ceabcd7097cd" /># ClinisolTech
### High-Performance Vanilla JavaScript SPA for IT Staffing & Technology Consulting
<img width="1781" height="899" alt="image" src="https://github.com/user-attachments/assets/de6b5085-4e6f-4ee0-938f-7482d617d7c8" />


> A production corporate web application built without a frontend framework,
> featuring custom History API routing, GSAP interactions, serverless form
> processing, resume uploads, technical SEO, and Apache production configuration.

🌐 Live: https://clinisoltech.com/

---

## ⚡ Engineering Highlights

- Custom Single Page Application built with Vanilla JavaScript
- HTML5 History API based client-side routing
- Clean routes such as `/services`, `/careers`, and `/contact`
- GSAP + ScrollTrigger interaction system
- Serverless Google Apps Script form processing
- Candidate resume upload using the FileReader API
- Google Sheets and Google Drive integration
- Apache `.htaccess` SPA fallback configuration
- HTTPS and canonical URL enforcement
- Security-related HTTP headers
- XML Sitemap, robots.txt and JSON-LD structured data
- Responsive CSS Grid/Flexbox architecture

---

## 🧩 Why I Built It This Way

ClinisolTech required more than a static corporate website.

The objective was to create a fast and responsive web experience while keeping
the frontend lightweight and avoiding unnecessary framework dependencies.

I implemented the application using:

HTML5
CSS3
Vanilla JavaScript ES6+
GSAP
Google Apps Script

Instead of creating separate HTML pages for every primary section, the application
uses a custom SPA navigation system.

---

## 🧭 Building SPA Routing Without React

One of the main technical parts of this project was implementing clean client-side
routing using the HTML5 History API.

Routes include:

/  
/about-us  
/services  
/careers  
/contact

### Navigation Flow

User clicks navigation
        ↓
JavaScript intercepts navigation
        ↓
History API updates browser URL
        ↓
Matching page container becomes active
        ↓
Page-specific UI initializes
        ↓
Animations execute

This provides SPA-style navigation while keeping readable URLs.

### Production Challenge

Client-side routing introduces an important deployment problem.

Opening:

clinisoltech.com/services

directly in the browser requires the server to understand that the request belongs
to the SPA.

I configured Apache rewrite/fallback behavior through `.htaccess` so clean routes
continue to load the application correctly.

---

## 🎬 Interaction & Animation Engineering

GSAP and ScrollTrigger were used to build the visual interaction layer.

The website includes:

→ Scroll-triggered section reveals  
→ Hero animations  
→ Animated statistics  
→ Interactive cards  
→ Smooth content transitions  
→ Responsive visual effects  

Animations were integrated with the application's navigation lifecycle rather than
being treated only as decorative effects.

---

## 🔎 Interactive Services Explorer

The Services interface allows visitors to filter technical capabilities without
loading another page.

Categories include:

[ All ] [ Cloud & DevOps ] [ Software Engineering ] [ QA & Support ]

JavaScript controls which service components are displayed based on the selected
category.

This provided additional hands-on experience with:

DOM manipulation  
event handling  
UI state management  
dynamic filtering

---

## 📄 Candidate Resume Pipeline

The Careers section contains a candidate profile and resume submission workflow.

### Browser

Candidate
   ↓
Career Form
   ↓
Resume Selection
   ↓
FileReader API
   ↓
Validation
   ↓
Base64 Encoding

### Serverless Layer

Encoded Request
   ↓
Google Apps Script
   ↓
├── Google Sheets → Candidate/Form Data
│
└── Google Drive → Resume/File Storage

The browser's FileReader API handles the selected file before the request is sent
to the serverless backend.

> Base64 is used for payload encoding, not encryption.

---

## ☁️ Serverless Form Architecture

Both candidate and business inquiry workflows communicate with Google Apps Script
Web App endpoints.

                    CLINISOLTECH
                         │
                Vanilla JavaScript
                         │
               ┌─────────┴─────────┐
               │                   │
            Careers             Contact
               │                   │
          Resume/Form           Lead Form
               │                   │
               └─────────┬─────────┘
                         ↓
                 Google Apps Script
                         ↓
                ┌────────┴────────┐
                │                 │
          Google Sheets      Google Drive

This architecture provided a lightweight backend for business forms without
requiring a continuously running application server.

---

## 🛡 Production Web Configuration

Another important part of this project was moving beyond frontend development and
handling production web configuration.

### Apache / `.htaccess`

Configured behavior for:

✓ HTTPS enforcement  
✓ Canonical non-WWW domain  
✓ SPA route fallback  
✓ Browser security headers  

### HTTP Headers

Implemented configuration involving:

HSTS  
X-Content-Type-Options  
X-Frame-Options  
Referrer-Policy

This gave me practical exposure to how frontend applications interact with web
server configuration in production.

---

## 🔍 Technical SEO

SEO was considered at the architecture level rather than only through page text.

Implemented:

### Clean URLs

clinisoltech.com/about-us  
clinisoltech.com/services  
clinisoltech.com/careers  
clinisoltech.com/contact

### Search Engine Files

sitemap.xml  
robots.txt

### Structured Data

JSON-LD / Schema.org markup for:

Organization  
Website

### Additional Configuration

Semantic HTML  
HTTPS  
Canonical domain handling  
Responsive layouts

---

## 🧱 Technology Breakdown

Frontend
├── HTML5
├── CSS3
│   ├── CSS Variables
│   ├── Grid
│   └── Flexbox
└── JavaScript ES6+
    ├── DOM API
    ├── History API
    └── FileReader API

Motion
├── GSAP
└── ScrollTrigger

Serverless
├── Google Apps Script
├── Google Sheets
└── Google Drive

Production
├── Apache / .htaccess
├── HTTPS
├── Rewrite Rules
└── HTTP Security Headers

SEO
├── sitemap.xml
├── robots.txt
└── JSON-LD

---

## 🖼 Product Walkthrough

### Landing Experience

<img width="1772" height="883" alt="image" src="https://github.com/user-attachments/assets/83978c12-eb00-4ba3-9fc4-f564fc3c0631" />



The landing experience introduces the company's staffing and technology
capabilities through an animated responsive interface.

### Technology Services

<img width="1224" height="603" alt="image" src="https://github.com/user-attachments/assets/99ead456-9438-40ec-b514-26b39399b771" />
<img width="1246" height="607" alt="image" src="https://github.com/user-attachments/assets/7e910e54-ac52-4031-ac56-0e3ebca9fd0b" />


Interactive service discovery for Cloud & DevOps, Software Engineering,
Data, QA and enterprise technology capabilities.

### Careers Experience

<img width="1360" height="616" alt="image" src="https://github.com/user-attachments/assets/73c5edf8-5aff-4046-be32-53e27ec200e3" />
<img width="1031" height="571" alt="image" src="https://github.com/user-attachments/assets/7e42875f-58e7-4763-bd18-6fe6b7b1c798" />


Candidate-focused careers interface with company information and application
functionality.

### Resume Submission

<img width="1018" height="580" alt="image" src="https://github.com/user-attachments/assets/781be835-8ef7-4053-ae2a-ac2e4ea266ab" />


Candidate profile and resume submission workflow connected to the serverless
processing layer.

### Contact & Lead Generation

<img width="1920" height="2807" alt="image" src="https://github.com/user-attachments/assets/e4ec47c7-8be2-4cc6-b25c-fccbd18f1810" />



Business inquiry workflow connected to Google Apps Script.

### Responsive Experience
Mobile Version
<img width="320" height="785" alt="image" src="https://github.com/user-attachments/assets/f4a554b6-c5f0-407e-9a08-77f18139c1a8" />

Tablet Version
<img width="574" height="817" alt="image" src="https://github.com/user-attachments/assets/2cb67c5a-a8e5-4545-9181-31c0cc4ddff3" />



Responsive layouts and navigation optimized for smaller devices.

---

## 🧠 Problems I Solved

### 01 — SPA navigation without React

Implemented custom routing and browser history management using Vanilla JavaScript.

### 02 — Direct URL access

Configured server rewrite rules so routes such as `/services` continue to work
when accessed directly.

### 03 — Resume processing without a traditional backend

Combined FileReader, Base64 payload processing and Google Apps Script to build
the candidate submission workflow.

### 04 — Serverless business lead capture

Connected frontend forms directly to Apps Script workflows and Google Sheets.

### 05 — Animation lifecycle

Integrated GSAP animations with SPA page transitions and dynamic content.

### 06 — Production SEO

Combined clean URLs, sitemap configuration, robots directives and structured
data with the SPA architecture.

---

## 📁 Showcase Repository

This repository is a technical case study rather than the production source
repository.

clinisoltech-serverless-spa-recruitment-platform/
│
├── README.md
└── screenshots/
    ├── home-page.png
    ├── services-page.png
    ├── careers-page.png
    ├── resume-submission.png
    ├── contact-page.png
    └── mobile-view.png

Production source code and internal configuration are intentionally excluded.

---

## 🚀 What I Would Build Next

My next iteration of this architecture would move toward:

React
   ↓
Spring Boot REST API
   ↓
Spring Security + JWT
   ↓
Hibernate / JPA
   ↓
PostgreSQL
   ↓
Docker
   ↓
CI/CD
   ↓
AWS

This would evolve the serverless corporate application into a conventional
Java full-stack architecture.

---

## 👨‍💻 Developer

**Pavan Kalyan Yarlagadda**

Web Development • JavaScript • Automation • Java Full Stack

---

## 🔒 Project Confidentiality

This repository contains documentation and sanitized screenshots only.

Production source code, API endpoints, Apps Script configuration, candidate
information, resumes, Google Sheets identifiers, Google Drive configuration,
credentials and internal company information are not publicly included.
