\# WEBIFY — PROJECT ROADMAP



\*\*Project:\*\* Webify  

\*\*Tagline:\*\* Build. Customize. Launch.  

\*\*Document:\*\* Project Roadmap  

\*\*Version:\*\* 1.0  

\*\*Last Updated:\*\* November 24, 2026  

\*\*Status:\*\* Planned  

\*\*Project Owner:\*\* Rodolph Habib



\---



\## 1. Introduction



This roadmap defines the planned development phases, milestones, deliverables, and target timeline for Webify.



Webify is a website-template marketplace and visual website-building platform. It will allow users to discover professional website templates, purchase them, customize their websites through a visual editor, and publish their websites online.



The platform will initially target the Lebanese market, with the long-term objective of expanding internationally.



The roadmap will be reviewed regularly and updated when project priorities, technical requirements, or business decisions change.



\## 2. Project Timeline Overview



| Phase | Name | Target Period |

|---|---|---|

| 0 | Project Planning and Setup | November 2026 |

| 1 | Requirements and UX/UI Design | November–December 2026 |

| 2 | Marketplace Frontend Development | December 2026 |

| 3 | Backend and Authentication | January 2027 |

| 4 | Template Management System | January–February 2027 |

| 5 | Visual Website Builder MVP | February–March 2027 |

| 6 | E-commerce and Payment Integration | April 2027 |

| 7 | Website Publishing and Hosting | May 2027 |

| 8 | Custom Development Services | June 2027 |

| 9 | Testing, Security, and Beta Release | July 2027 |

| 10 | Public MVP Launch | August 2027 |

| 11 | Improvements and Growth | September–October 2027 |

| 12 | International Expansion Preparation | November–December 2027 |



\*Note: These are preliminary target periods, not guaranteed deadlines. The schedule depends on available development time, technical complexity, and business requirements.\*



\---



\## 3. Detailed Development Phases



\### Phase 0 — Project Planning and Setup



\*\*Target:\*\* November 2026



\*\*Objectives:\*\*

\- Establish the project vision and scope.

\- Define the MVP requirements.

\- Organize the GitHub repository.

\- Establish documentation and development standards.

\- Prepare the initial development environment.



\*\*Deliverables:\*\*

\- Project Charter.

\- Project Roadmap.

\- Requirements documentation.

\- Risk Register.

\- GitHub repository structure.

\- Development workflow.



\*\*Completion Criteria:\*\*

\- Project documentation is organized.

\- Initial requirements are documented.

\- Repository and development environment are ready.



\### Phase 1 — Requirements and UX/UI Design



\*\*Target:\*\* November–December 2026



\*\*Objectives:\*\*

\- Define the main user journeys.

\- Identify customer, administrator, and developer needs.

\- Design the platform's visual identity.

\- Create responsive layouts and reusable components.



\*\*Main Activities:\*\*

\- Create user personas.

\- Define the website sitemap.

\- Design wireframes in Figma.

\- Create the design system.

\- Design the homepage and marketplace.

\- Design template details and preview pages.

\- Design customer and administrator dashboards.

\- Plan the visual editor interface.



\*\*Deliverables:\*\*

\- Software Requirements Specification (SRS).

\- User Stories and Acceptance Criteria.

\- Figma UI/UX designs.

\- Design System.

\- User Flow Diagrams.

\- Sitemap.



\*\*Completion Criteria:\*\*

\- Main user journeys are documented.

\- Core screens have approved designs.

\- Responsive design principles are established.



\### Phase 2 — Marketplace Frontend Development



\*\*Target:\*\* December 2026



\*\*Objectives:\*\*

Develop the initial customer-facing marketplace.



\*\*Main Activities:\*\*

\- Set up the Next.js and React frontend.

\- Configure TypeScript and Tailwind CSS.

\- Implement the homepage.

\- Build the navigation and footer.

\- Create the template catalog.

\- Implement category filters and search.

\- Create template detail pages.

\- Add responsive layouts.



\*\*Deliverables:\*\*

\- Functional homepage.

\- Template marketplace.

\- Template cards and categories.

\- Template detail pages.

\- Responsive frontend.



\*\*Completion Criteria:\*\*

\- Users can browse available templates.

\- Users can filter and view template details.

\- Main pages work on desktop and mobile.



\### Phase 3 — Backend and Authentication



\*\*Target:\*\* January 2027



\*\*Objectives:\*\*

Build the backend foundation and user-management functionality.



\*\*Main Activities:\*\*

\- Set up the NestJS backend.

\- Configure PostgreSQL and Prisma.

\- Design the database schema.

\- Implement authentication.

\- Implement registration and login.

\- Add password hashing and secure sessions.

\- Implement role-based access control.

\- Create initial API endpoints.



\*\*Deliverables:\*\*

\- Backend application.

\- Database schema.

\- Authentication API.

\- User management.

\- Role and permission system.

\- API documentation.



\*\*Completion Criteria:\*\*

\- Users can register and log in.

\- Authentication is securely implemented.

\- Protected endpoints enforce permissions.

\- Database relationships and constraints are tested.



\### Phase 4 — Template Management System



\*\*Target:\*\* January–February 2027



\*\*Objectives:\*\*

Create the system for managing and displaying website templates.



\*\*Main Activities:\*\*

\- Design the template data model.

\- Implement template categories.

\- Create template management APIs.

\- Build administrator template management screens.

\- Implement template preview functionality.

\- Store template assets and images.

\- Support template versions.



\*\*Deliverables:\*\*

\- Template management backend.

\- Administrator template dashboard.

\- Template catalog connected to the backend.

\- Template preview system.

\- Template versioning foundation.



\*\*Completion Criteria:\*\*

\- Administrators can create, update, publish, and archive templates.

\- Customers can browse published templates.

\- Template data and assets are stored correctly.



\### Phase 5 — Visual Website Builder MVP



\*\*Target:\*\* February–March 2027



\*\*Objectives:\*\*

Allow customers to customize website templates through a visual editor.



\*\*Main Activities:\*\*

\- Evaluate GrapesJS versus a custom editor.

\- Build the editor workspace.

\- Implement drag-and-drop components.

\- Add text, image, button, and section components.

\- Implement basic styling controls.

\- Add desktop and mobile previews.

\- Implement save and load functionality.

\- Support draft versions and publishing preparation.



\*\*Deliverables:\*\*

\- Visual editor MVP.

\- Component library.

\- Drag-and-drop functionality.

\- Responsive preview.

\- Website saving and loading.



\*\*Completion Criteria:\*\*

\- Customers can customize basic page content and styles.

\- Changes can be saved and restored.

\- The editor validates its structured website data.

\- User-created content cannot execute arbitrary server-side code.



\### Phase 6 — E-commerce and Payment Integration



\*\*Target:\*\* April 2027



\*\*Objectives:\*\*

Enable customers to purchase templates and manage orders.



\*\*Main Activities:\*\*

\- Implement shopping cart functionality.

\- Create order management.

\- Implement checkout workflows.

\- Research payment provider eligibility for Lebanese businesses.

\- Build a payment-provider adapter.

\- Implement payment status tracking.

\- Verify payment webhooks.

\- Consider a controlled manual bank-transfer option if required.



\*\*Deliverables:\*\*

\- Shopping cart.

\- Checkout workflow.

\- Order management system.

\- Payment integration.

\- Payment confirmation and order history.



\*\*Completion Criteria:\*\*

\- Customers can place orders.

\- Payment status is verified before granting purchases.

\- Duplicate payment notifications do not create duplicate orders.

\- Order records are stored securely.



\### Phase 7 — Website Publishing and Hosting



\*\*Target:\*\* May 2027



\*\*Objectives:\*\*

Allow customers to publish their customized websites.



\*\*Main Activities:\*\*

\- Develop the publishing workflow.

\- Implement website deployment.

\- Configure customer subdomains.

\- Manage published website versions.

\- Implement domain configuration.

\- Configure SSL and HTTPS.

\- Add basic website status monitoring.



\*\*Deliverables:\*\*

\- Website publishing system.

\- Customer subdomains.

\- Domain management foundation.

\- Published website management.



\*\*Completion Criteria:\*\*

\- Customers can publish their websites.

\- Published websites are accessible through their assigned URLs.

\- Publishing failures are logged and handled safely.



\### Phase 8 — Custom Development Services



\*\*Target:\*\* June 2027



\*\*Objectives:\*\*

Introduce custom website development as an additional business service.



\*\*Main Activities:\*\*

\- Create a custom development services page.

\- Implement project inquiry forms.

\- Collect customer requirements.

\- Create project request management.

\- Build an administrator inquiry dashboard.

\- Define project status tracking.

\- Establish quotation and approval workflows.



\*\*Deliverables:\*\*

\- Custom development service page.

\- Project inquiry form.

\- Inquiry management dashboard.

\- Project status workflow.



\*\*Completion Criteria:\*\*

\- Customers can submit project requests.

\- Administrators can review and manage inquiries.

\- Requests can be tracked through defined statuses.



\### Phase 9 — Testing, Security, and Beta Release



\*\*Target:\*\* July 2027



\*\*Objectives:\*\*

Validate the platform before public launch.



\*\*Main Activities:\*\*

\- Perform functional testing.

\- Write frontend and backend automated tests.

\- Conduct API testing.

\- Perform end-to-end testing with Playwright.

\- Test responsive layouts.

\- Review authentication and authorization.

\- Validate file uploads.

\- Test payment workflows.

\- Check performance and accessibility.

\- Run a limited beta with selected users.



\*\*Deliverables:\*\*

\- Test Strategy.

\- Test Cases and Results.

\- Bug Reports.

\- Security Review.

\- Beta Feedback Report.

\- Release Candidate.



\*\*Completion Criteria:\*\*

\- Critical and high-priority defects are resolved.

\- Main user journeys pass testing.

\- Security checks are completed.

\- Beta feedback is reviewed.



\### Phase 10 — Public MVP Launch



\*\*Target:\*\* August 2027



\*\*Objectives:\*\*

Release the first public version of Webify.



\*\*Main Activities:\*\*

\- Prepare production infrastructure.

\- Configure production environment variables.

\- Configure database backups.

\- Set up logging and monitoring.

\- Prepare legal and business documentation.

\- Publish the production website.

\- Announce the launch.

\- Monitor user activity and errors.



\*\*Deliverables:\*\*

\- Production Webify platform.

\- Public marketplace.

\- Initial template collection.

\- Customer registration and authentication.

\- MVP builder functionality.

\- Purchasing workflow, subject to payment-provider readiness.

\- Launch documentation.



\*\*Completion Criteria:\*\*

\- Production deployment is stable.

\- Critical workflows are operational.

\- Backup and recovery procedures are documented.

\- Support and issue-reporting channels are available.



\### Phase 11 — Improvements and Growth



\*\*Target:\*\* September–October 2027



\*\*Objectives:\*\*

Improve the platform based on real customer feedback.



\*\*Main Activities:\*\*

\- Analyze customer feedback.

\- Improve the visual builder.

\- Expand template categories.

\- Improve marketplace search.

\- Optimize performance.

\- Improve the customer dashboard.

\- Introduce additional analytics.

\- Improve onboarding and documentation.



\*\*Deliverables:\*\*

\- Updated platform releases.

\- Improved editor experience.

\- Additional templates.

\- Performance improvements.

\- Customer feedback reports.



\*\*Completion Criteria:\*\*

\- Priority feedback items are addressed.

\- Platform stability and usability improve.

\- New features pass the established testing process.



\### Phase 12 — International Expansion Preparation



\*\*Target:\*\* November–December 2027



\*\*Objectives:\*\*

Prepare Webify to serve customers outside Lebanon.



\*\*Main Activities:\*\*

\- Review international payment options.

\- Improve localization.

\- Support Arabic and English, including RTL layouts.

\- Evaluate additional currencies.

\- Review hosting and infrastructure scalability.

\- Review legal requirements for target markets.

\- Research international marketing opportunities.



\*\*Deliverables:\*\*

\- International expansion plan.

\- Localization improvements.

\- Payment expansion assessment.

\- Infrastructure improvement plan.

\- Updated business strategy.



\*\*Completion Criteria:\*\*

\- International requirements are documented.

\- Technical and business limitations are identified.

\- Expansion priorities are approved.



\---



\## 4. Key Project Milestones



| Milestone | Target Date | Expected Result |

|---|---|---|

| M1 — Planning Complete | November 2026 | Project foundation established |

| M2 — Design Complete | December 2026 | Main UI/UX designs approved |

| M3 — Marketplace Ready | December 2026 | Users can browse templates |

| M4 — Backend Ready | January 2027 | Authentication and APIs operational |

| M5 — Template Management Ready | February 2027 | Templates managed through the platform |

| M6 — Builder MVP Ready | March 2027 | Basic visual customization works |

| M7 — Commerce Ready | April 2027 | Orders and payment workflow operational |

| M8 — Publishing Ready | May 2027 | Customers can publish websites |

| M9 — Services Workflow Ready | June 2027 | Custom project inquiries supported |

| M10 — Beta Complete | July 2027 | Testing and beta feedback completed |

| M11 — Public MVP Launch | August 2027 | Webify publicly available |

| M12 — Expansion Plan Ready | December 2027 | International expansion assessed |



\---



\## 5. Development Priorities



Development will follow this priority order:



\*\*Priority 1 — Essential Foundation\*\*

\- Project structure and documentation.

\- UI/UX design.

\- Marketplace frontend.

\- Database and backend foundation.

\- Authentication and user management.



\*\*Priority 2 — Core Product\*\*

\- Template management.

\- Template previews.

\- Visual website builder.

\- Website saving and customization.



\*\*Priority 3 — Business Functionality\*\*

\- Shopping cart.

\- Orders and payments.

\- Website publishing.

\- Customer dashboard.



\*\*Priority 4 — Additional Services\*\*

\- Custom development inquiries.

\- Project management workflow.

\- Customer support improvements.



\*\*Priority 5 — Growth\*\*

\- Analytics.

\- Additional templates.

\- International payment research.

\- Localization and expansion.



\---



\## 6. Project Management and Tracking



Each development task should be tracked through GitHub Issues or GitHub Projects.



\### Task Statuses



\- Backlog

\- To Do

\- In Progress

\- In Review

\- Testing

\- Done

\- Blocked



\### Task Information



Every significant task should include:

\- Task ID.

\- Title.

\- Description.

\- Priority.

\- Assigned owner.

\- Related milestone.

\- Acceptance criteria.

\- Estimated effort.

\- Status.



\### Git Branching Strategy



Use the following branch conventions:



\- `main` — stable production-ready code.

\- `develop` — integration branch, if needed.

\- `feature/feature-name` — new features.

\- `fix/issue-name` — bug fixes.

\- `docs/document-name` — documentation changes.



\### Commit Message Convention



Examples:



\- `feat: add marketplace homepage`

\- `feat: implement user authentication`

\- `fix: resolve template preview issue`

\- `docs: update project roadmap`

\- `test: add authentication tests`

\- `refactor: improve template management`



\---



\## 7. Risk and Schedule Management



The roadmap is a planning baseline and may change as development progresses.



Potential schedule risks include:



\- Limited development resources.

\- Unexpected technical complexity in the visual builder.

\- Payment provider restrictions in Lebanon.

\- Hosting and publishing costs.

\- Security and performance requirements.

\- Delays in design or requirements approval.



\### Mitigation Strategy



\- Build the MVP in small, testable increments.

\- Prioritize essential functionality.

\- Validate payment options early.

\- Avoid unnecessary architectural complexity.

\- Document important technical decisions.

\- Review project progress regularly.

\- Update milestones when assumptions change.



\---



\## 8. Definition of Roadmap Completion



The roadmap will be considered successfully delivered when:



1\. The MVP is publicly available.

2\. Customers can browse and preview templates.

3\. Customers can register and manage their accounts.

4\. Customers can purchase templates through an operational payment or approved alternative workflow.

5\. Customers can customize websites using the visual editor.

6\. Customers can publish their websites.

7\. Administrators can manage templates and orders.

8\. The platform has completed its essential testing and security checks.

9\. Technical and operational documentation is maintained.

10\. A plan for future improvements and expansion is established.



\---



\## 9. Roadmap Review and Change Control



This document should be reviewed at the end of each major development phase.



Changes may be required because of:

\- New customer requirements.

\- Technical limitations.

\- Business priorities.

\- Budget or resource constraints.

\- Security or legal requirements.



All significant changes should be documented with their reason, impact, and approval status.



\*\*Document Owner:\*\* Webify Project Owner  

\*\*Document Status:\*\* Planned  

\*\*Version:\*\* 1.0



\---



\*Webify — Build. Customize. Launch.\*

