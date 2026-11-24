\# WEBIFY — PROJECT CHARTER



\*\*Tagline:\*\* Build. Customize. Launch.



| Document Control | Details |

|---|---|

| Product | Webify — Website Template Marketplace and Visual Website Builder |

| Document Type | Project Charter |

| Version | 1.0 |

| Status | Initial Baseline Draft |

| Prepared | 24 November 2026 |

| Initial Market | Lebanon, followed by international expansion |

| Product Owner | Founder |

| Business Model | Template sales, custom development, future subscriptions and marketplace commissions |



\---



\## 1. Executive Summary



Webify is a digital platform that enables individuals and businesses to discover professionally designed website templates, preview them, purchase a suitable design, customize their websites through a visual editor, and publish them online.



Customers who require more advanced functionality or unique designs can also request professional custom development services.



Webify aims to simplify website creation and make professional web solutions more accessible, particularly for small businesses, freelancers, and entrepreneurs in Lebanon.



\## 2. Vision and Mission



\### Vision



Make professional website creation more accessible to businesses and individuals, starting in Lebanon and expanding internationally after validating the product and business model.



\### Mission



Provide an accessible platform combining professionally designed website templates, visual customization tools, and reliable development services.



\### Product Positioning



Webify combines three main capabilities:



1\. A curated website-template marketplace.

2\. A visual website builder.

3\. Optional professional development and maintenance services.



\## 3. Business Objectives



\- Validate demand for affordable, professionally designed websites among Lebanese businesses.

\- Generate revenue through website-template sales and custom development.

\- Build a repeatable process for creating, licensing, selling, and supporting templates.

\- Establish a foundation for subscriptions and third-party developer participation.

\- Expand internationally after validating the initial market.



\## 4. Product Objectives



\- Allow visitors to browse and preview templates without registering.

\- Allow customers to purchase templates and create independent websites.

\- Provide a visual editor for modifying website content and design.

\- Allow customers to save drafts and publish websites.

\- Support Webify-managed subdomains in the initial release.

\- Allow customers to request and track custom-development projects.



\## 5. Target Users



| User Group | Needs | Webify Solution |

|---|---|---|

| Small business owners | Affordable professional websites | Templates and visual editor |

| Entrepreneurs | Launch an online presence quickly | Ready-made templates |

| Freelancers | Professional portfolio websites | Portfolio templates |

| Agencies | Faster website delivery | Reusable templates |

| Developers | Opportunities to provide services | Future marketplace participation |

| Administrators | Manage platform operations | Admin dashboard |



\## 6. Product Scope



\### 6.1 MVP — Initial Release



The first release will focus on the following capabilities.



\*\*A. Public Marketplace\*\*



\- Homepage and template catalog.

\- Template categories and search.

\- Template details and pricing.

\- Screenshots and live previews.

\- Responsive template previews.



\*\*B. User Accounts\*\*



\- Registration and login.

\- Customer profiles.

\- Secure account management.



\*\*C. Template Management\*\*



\- Administrative template creation and editing.

\- Template publication and archiving.

\- Template version management.



\*\*D. Visual Website Builder\*\*



\- Basic drag-and-drop editing.

\- Supported components such as headings, paragraphs, images, buttons, and sections.

\- Editing text, colors, typography, and spacing.

\- Desktop, tablet, and mobile previews.

\- Saving and reloading website drafts.



\*\*E. Commerce\*\*



\- Orders and purchase records.

\- Payment workflow using a verified, locally viable payment method.

\- Purchase entitlements and template licensing.



\*\*F. Website Publishing\*\*



\- Publish websites using Webify-managed subdomains.

\- Basic publishing status and website management.



\*\*G. Custom Development\*\*



\- Request form for customers needing personalized development.

\- Administrative request tracking and quotation workflow.



\### 6.2 Out of Scope for the First Release



The following features are deferred:



\- A fully general-purpose competitor to mature website-building platforms.

\- Automated multi-vendor developer payouts.

\- Arbitrary server-side code execution.

\- Unrestricted JavaScript injection.

\- Full enterprise e-commerce functionality.

\- AI-generated complete websites.

\- Real-time collaborative editing.

\- Advanced animation timelines.

\- A large third-party plugin ecosystem.



These features may be evaluated in future releases.



\## 7. Functional Requirements



| ID | Requirement |

|---|---|

| FR-01 | Visitors can browse available templates. |

| FR-02 | Visitors can search and filter templates. |

| FR-03 | Visitors can view template details and previews. |

| FR-04 | Customers can register and authenticate. |

| FR-05 | Customers can purchase templates through supported payment methods. |

| FR-06 | Administrators can manage templates and categories. |

| FR-07 | Customers can create websites from purchased templates. |

| FR-08 | Customers can edit supported website components. |

| FR-09 | Customers can save and reload website drafts. |

| FR-10 | Customers can preview responsive layouts. |

| FR-11 | Customers can publish websites to Webify subdomains. |

| FR-12 | Customers can submit custom-development requests. |

| FR-13 | Administrators can manage orders and customer requests. |



\## 8. Non-Functional Requirements



\### Security



\- Secure password hashing.

\- Role-based access control.

\- Ownership verification for customer resources.

\- Input validation and output sanitization.

\- Rate limiting and secure session management.

\- Secure file-upload validation.



\### Performance



\- Optimize images and static assets.

\- Minimize unnecessary API requests.

\- Implement pagination for template catalogs.

\- Monitor page load and rendering performance.



\### Scalability



\- Begin with a modular monolith.

\- Keep application modules clearly separated.

\- Design integrations so payment and hosting providers can be changed.



\### Maintainability



\- Use TypeScript and consistent coding standards.

\- Maintain technical documentation.

\- Use version control and meaningful commits.

\- Implement automated testing.



\### Accessibility and Localization



\- Responsive interfaces.

\- Accessible navigation and forms.

\- Arabic and English language support.

\- Right-to-left layout support for Arabic.



\### Reliability



\- Database backups.

\- Error logging and monitoring.

\- Tested recovery procedures.

\- Versioned website content.



\## 9. Proposed Technology Stack



| Layer | Proposed Technology |

|---|---|

| Frontend | Next.js, React, TypeScript |

| Styling | Tailwind CSS |

| Backend | NestJS, TypeScript |

| Database | PostgreSQL |

| ORM | Prisma |

| Visual Editor | GrapesJS prototype or custom editor |

| Drag and Drop | dnd-kit, if using a custom editor |

| File Storage | S3-compatible storage or Cloudinary |

| Testing | Vitest/Jest and Playwright |

| Version Control | Git and GitHub |

| CI/CD | GitHub Actions |



Technology choices are provisional and must be documented when finalized.



\## 10. High-Level Architecture



Webify will initially follow a modular monolith architecture.



The main application modules are:



\- Authentication and user management.

\- Marketplace and catalog.

\- Template management.

\- Website builder.

\- Website rendering and publishing.

\- Orders and payments.

\- Custom development requests.

\- Administration.



The frontend communicates with the backend through documented APIs. PostgreSQL stores application data, while object storage handles uploaded media and template assets.



Microservices are not required for the initial release and should only be considered when justified by actual scale or operational needs.



\## 11. Core Data Entities



The initial conceptual data model includes:



\- User

\- Role and UserRole

\- Profile

\- Category

\- Template

\- TemplateVersion

\- TemplateAsset

\- Website

\- WebsitePage

\- WebsiteVersion

\- Asset

\- Order

\- OrderItem

\- Payment

\- License

\- Subscription

\- Domain

\- CustomRequest

\- Quotation

\- Review

\- AuditLog



\### Data Integrity Principles



\- Use UUID primary keys.

\- Enforce foreign-key relationships.

\- Use DECIMAL/NUMERIC for monetary values.

\- Store currency for every price and transaction.

\- Use database transactions for order and payment state changes.

\- Keep immutable snapshots of purchased products and license terms.

\- Enforce ownership and authorization at the backend level.



\## 12. UX/UI Direction



\*\*Brand:\*\* Webify



\*\*Tagline:\*\* Build. Customize. Launch.



Initial visual direction:



\- Modern, clean, and professional SaaS interface.

\- Primary color: `#6C4CF1`

\- Dark color: `#111827`

\- Background: `#F8FAFC`

\- Soft accent: `#E8E4FF`

\- Typography: Inter or Manrope, with a suitable Arabic font pairing.



\### Main Public Pages



\- Home

\- Templates

\- Template Categories

\- Template Details

\- Pricing

\- Custom Development

\- About

\- Contact

\- Login

\- Register



\### Customer Dashboard



\- Overview

\- My Websites

\- Website Editor

\- Purchases

\- Orders

\- Domains

\- Account Settings



\### Administration



\- Dashboard

\- Users

\- Templates

\- Categories

\- Orders

\- Custom Requests

\- Platform Settings



\## 13. Security, Payments and Operations



Security and customer data protection must be considered throughout development.



Important controls include:



\- Password hashing and secure authentication.

\- Role-based authorization.

\- Protection against XSS, CSRF, and IDOR vulnerabilities.

\- Validation of uploaded files and media.

\- Webhook signature verification and idempotency.

\- Secure handling of environment variables and API credentials.

\- Regular database backups.

\- Audit logging for sensitive administrative actions.



\### Payment Strategy



Payment provider eligibility for Lebanese merchants must be verified before selecting a provider.



Webify should use a payment-provider adapter so that payment integrations can be replaced without redesigning the order system.



A controlled bank-transfer and manual-confirmation workflow may be considered if appropriate.



Webify must never store raw payment-card numbers or CVV values.



\## 14. Key Risks and Mitigation



| Risk | Impact | Mitigation |

|---|---|---|

| Advanced visual builder complexity | High | Build a limited component-based editor first |

| Payment provider restrictions | High | Verify eligibility and prepare alternative methods |

| Hosting and infrastructure costs | Medium | Start with controlled hosting architecture |

| Security vulnerabilities | High | Apply secure development practices and testing |

| Scope expansion | High | Prioritize MVP requirements |

| Customer hosting expectations | High | Clearly communicate package inclusions and recurring costs |

| Template licensing issues | High | Verify commercial usage and redistribution rights |

| Solo-developer capacity | High | Work in small milestones and avoid premature complexity |



\## 15. Engineering and Project Management Workflow



All project work should be tracked through GitHub Issues and a project board.



Recommended hierarchy:



\*\*Initiative → Epic → Story/Task → Subtask\*\*



Every task should have:



\- A clear description.

\- Priority.

\- Acceptance criteria.

\- Status.

\- Related documentation.

\- Testing expectations.



\### Workflow Statuses



| Status | Meaning |

|---|---|

| Backlog | Not yet selected |

| Ready | Requirements are clear |

| In Progress | Work has started |

| In Review | Review is in progress |

| In QA | Testing is in progress |

| Blocked | Work cannot continue |

| Done | Acceptance criteria are met |



\### Git Conventions



\- `main` should remain stable.

\- Use feature branches for new functionality.

\- Use bug-fix branches for corrections.

\- Use documentation branches for documentation changes.

\- Write meaningful commit messages.

\- Use pull requests and review changes before merging.



Example commit:



`docs: add project charter`



\## 16. Definition of Done



A task is complete when:



\- Its acceptance criteria are satisfied.

\- Relevant tests pass.

\- Code is reviewed.

\- No known critical defect remains.

\- Documentation is updated where necessary.

\- Security and authorization implications are reviewed.

\- Changes are committed and linked to the relevant GitHub issue.



\## 17. Project Success Measures



Initial measures to validate include:



\- Number of available published templates.

\- Number of visitors browsing the marketplace.

\- Number of registered customers.

\- Template preview-to-purchase conversion.

\- Number of completed purchases.

\- Number of websites created and published.

\- Number of custom-development requests.

\- Customer satisfaction and support response time.

\- Availability and reliability of published websites.



Targets should be established after initial customer research and beta testing.



\## 18. Immediate Priorities



1\. Complete the repository documentation structure.

2\. Finalize the MVP requirements.

3\. Identify target customer groups and validate their needs.

4\. Define the first user journeys.

5\. Create the initial Figma design system.

6\. Document the system architecture.

7\. Design the initial database model.

8\. Establish the development environment.

9\. Create the first development milestone.

10\. Begin implementation only after the requirements and initial designs are sufficiently clear.



\## 19. Charter Approval and Change Control



This document is the initial project baseline for Webify.



Material changes to the product vision, MVP scope, architecture, business model, or release targets should be recorded and reviewed.



| Field | Value |

|---|---|

| Project Owner | Founder |

| Document Version | 1.0 |

| Status | Draft for Review |

| Last Updated | 24 November 2026 |

| Next Review | After initial discovery and requirements validation |



\---



\*\*Webify — Build. Customize. Launch.\*\*

