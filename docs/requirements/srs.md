\# Webify — Software Requirements Specification (SRS)



\*\*Project:\*\* Webify  

\*\*Version:\*\* 1.0  

\*\*Date:\*\* November 27, 2026  

\*\*Status:\*\* Initial Draft



\---



\## 1. Introduction



\### 1.1 Purpose



This document defines the software requirements for Webify, a website marketplace and customization platform. It describes the system's functionality, users, technical expectations, and limitations.



It will serve as a reference for designing, developing, testing, and maintaining the platform.



\### 1.2 Product Overview



Webify is a platform that allows individuals and businesses to discover professional website templates, customize their selected designs, and launch websites without needing extensive programming knowledge.



The platform will initially target the Lebanese market, with plans to expand internationally.



\### 1.3 Product Vision



To make professional website creation more accessible, affordable, and straightforward for individuals, freelancers, entrepreneurs, and businesses.



\*\*Tagline:\*\* Build. Customize. Launch.



\---



\## 2. Scope



\### 2.1 Included in the MVP



\- Public homepage.

\- Website template marketplace.

\- Template categories and basic search.

\- Template details and previews.

\- Customer registration and login.

\- Customer dashboard.

\- Basic website customization.

\- Order and purchase request management.

\- Administrative dashboard.

\- Template and customer management.

\- Website preview and delivery/publishing workflow.

\- Responsive desktop and mobile experience.



\### 2.2 Excluded from the Initial MVP



\- AI-powered website generation.

\- Advanced unrestricted drag-and-drop editing.

\- Third-party template creator marketplace.

\- Complex subscription plans.

\- Advanced agency collaboration.

\- Automated international payment processing.

\- Advanced analytics and marketing automation.



These features may be considered in later releases.



\---



\## 3. User Types



\### 3.1 Guest



A visitor who has not registered.



Can:

\- Visit the homepage.

\- Browse templates.

\- Search and filter templates.

\- View template details and previews.

\- Register for an account.



\### 3.2 Customer



A registered user who wants to obtain and customize a website.



Can:

\- Log in and manage their account.

\- Browse and select templates.

\- Submit purchase or service requests.

\- View order status.

\- Customize permitted website content.

\- Preview and save changes.

\- Access their website delivery information.



\### 3.3 Administrator



A platform manager responsible for operating Webify.



Can:

\- Access the administration dashboard.

\- Manage templates and categories.

\- Manage customer accounts.

\- Review and manage orders.

\- Update order and payment statuses.

\- Manage marketplace content.

\- Review customer inquiries.



\### 3.4 Developer



Responsible for building and maintaining the platform.



Can:

\- Maintain frontend and backend applications.

\- Manage database structures.

\- Develop and maintain APIs.

\- Implement security controls.

\- Test and deploy new versions.

\- Monitor application performance.



\---



\## 4. Functional Requirements



\### FR-01: Homepage

The system shall provide a homepage explaining Webify's services and displaying featured templates.



\### FR-02: Template Marketplace

The system shall display available website templates in an organized marketplace.



\### FR-03: Template Categories

The system shall allow visitors to browse templates by categories such as business, restaurant, portfolio, and e-commerce.



\### FR-04: Template Search

The system shall allow visitors to search for templates using keywords.



\### FR-05: Template Details

The system shall display template descriptions, screenshots, features, and available previews.



\### FR-06: User Registration

The system shall allow visitors to create customer accounts.



\### FR-07: User Authentication

The system shall allow registered customers to securely log in and log out.



\### FR-08: Customer Dashboard

The system shall provide customers with a dashboard to access their orders and websites.



\### FR-09: Template Selection

The system shall allow customers to select a template and submit a request to obtain it.



\### FR-10: Order Management

The system shall allow customers to view their order details and current order status.



\### FR-11: Website Customization

The system shall allow customers to modify approved content, including text, images, colors, buttons, and contact information.



\### FR-12: Website Preview

The system shall allow customers to preview their website before final delivery or publishing.



\### FR-13: Save Changes

The system shall allow customers to save their customization changes.



\### FR-14: Administration

The system shall provide administrators with tools to manage customers, templates, categories, and orders.



\### FR-15: Payment Management

The system shall support recording and reviewing payment status through the payment method selected for the MVP.



\### FR-16: Website Delivery

The system shall provide an organized process for delivering or publishing completed customer websites.



\### FR-17: Customer Support

The system shall provide a way for customers to contact Webify regarding questions or problems.



\---



\## 5. Non-Functional Requirements



\### NFR-01: Performance

The platform should load its main pages efficiently and optimize images and other assets.



\### NFR-02: Security

The system shall protect customer accounts, passwords, website data, and administrative operations.



\### NFR-03: Usability

The interface should be simple and understandable for users with limited technical experience.



\### NFR-04: Responsiveness

The platform shall support desktop, tablet, and mobile screen sizes.



\### NFR-05: Reliability

The system should minimize downtime and provide reliable data storage and backups.



\### NFR-06: Maintainability

The application should use a modular architecture and consistent coding standards.



\### NFR-07: Scalability

The architecture should support future increases in users, templates, and customer websites.



\### NFR-08: Compatibility

The platform should support modern browsers, including Chrome, Edge, Firefox, and Safari.



\### NFR-09: Data Integrity

The system shall validate user input and maintain accurate customer, order, and payment records.



\### NFR-10: Accessibility

The interface should follow accessible design practices, including readable text, keyboard navigation, and appropriate color contrast.



\---



\## 6. Technology Stack



| Layer | Technology |

|---|---|

| Frontend | Next.js, React, TypeScript |

| Styling | Tailwind CSS |

| Backend | NestJS, TypeScript |

| Database | PostgreSQL |

| ORM | Prisma |

| Website Editor | GrapesJS prototype or controlled custom editor |

| File Storage | Cloudinary or S3-compatible storage |

| Testing | Jest/Vitest, Playwright |

| Version Control | Git and GitHub |

| Deployment | To be evaluated |



The architecture will initially follow a modular monolith approach.



\---



\## 7. Business Rules



1\. Customers must authenticate before submitting orders.

2\. Only administrators can publish, edit, or remove marketplace templates.

3\. Customers may only access and modify websites they own.

4\. A customer must receive confirmation of their order before the delivery process begins.

5\. Payment status must be recorded and verified before a paid order is marked as completed.

6\. Website customization must use approved components and validated content.

7\. Template updates must not automatically overwrite existing customer websites.

8\. Administrative actions must be protected by role-based permissions.



\---



\## 8. Security Requirements



\- Passwords must be securely hashed.

\- Authentication and authorization must be enforced.

\- Administrative routes must be restricted.

\- User input must be validated on the server.

\- File uploads must be checked for type and size.

\- API endpoints must implement appropriate access controls and rate limiting.

\- Payment webhooks, if introduced, must be verified.

\- Customer data must not be accessible to unauthorized users.



\---



\## 9. Future Enhancements



\- Advanced drag-and-drop website builder.

\- AI-assisted website generation.

\- Arabic and English language support with RTL layouts.

\- Custom domain integration.

\- Subscription-based services.

\- Agency accounts.

\- Advanced analytics.

\- International payment integrations.

\- Third-party template creator marketplace.



\---



\## 10. Acceptance Criteria



The initial MVP will be considered ready for beta testing when:



\- Visitors can browse and preview templates.

\- Customers can register and log in.

\- Customers can submit and track orders.

\- Administrators can manage templates and orders.

\- Customers can customize approved website content.

\- Customers can preview their changes.

\- The core workflows work on desktop and mobile.

\- No critical security or functional defects remain unresolved.

\- The website delivery process has been tested successfully.



\---



\## 11. Open Questions



The following decisions require further investigation:



1\. Which payment provider can legally and practically support Webify in Lebanon?

2\. Will the initial customization editor use GrapesJS or a custom component-based editor?

3\. Which hosting provider will be used for customer websites?

4\. Will website publishing initially use Webify subdomains?

5\. What pricing model should be used for templates and custom development services?



\---



\*\*Document Owner:\*\* Webify Project Team  

\*\*Document Status:\*\* Initial Draft — Subject to Review

