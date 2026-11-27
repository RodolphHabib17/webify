# WEBIFY — MVP SCOPE REVIEW AND CHANGE LOG

**Project:** Webify  
**Document:** MVP Scope Review and Change Log  
**Version:** 1.0  
**Review Date:** November 27, 2026  
**Status:** Proposed — Pending Final Review  
**Project Owner:** Rodolph Habib

---

## 1. Introduction

This document records the review and refinement of the existing Webify MVP Features and Scope document.

The purpose of this review is to confirm the features required for the first release, identify functionality that should be postponed, clarify technical decisions, and prevent unnecessary complexity during initial development.

This document supplements the original MVP specification. It does not replace it.

**Primary reference:** `docs/requirements/mvp-features.md`

## 2. MVP Scope Review

The existing MVP scope is considered appropriate for the initial Webify release.

The first release will focus on providing a complete customer journey:

1. Discover website templates.
2. Browse and preview available designs.
3. Register and access a customer account.
4. Select a template.
5. Submit an order or purchase request.
6. Complete the approved payment process.
7. Customize permitted website content.
8. Preview the customized website.
9. Receive a completed and usable website.

The initial release should prioritize reliability and a working end-to-end customer experience rather than advanced editor functionality.

## 3. Confirmed MVP Features — P0

The following features remain essential for the first release.

| ID | Feature | Decision |
|---|---|---|
| MVP-01 | Public homepage | Keep in MVP |
| MVP-02 | Template marketplace | Keep in MVP |
| MVP-03 | Template categories | Keep in MVP |
| MVP-04 | Basic template search | Keep in MVP |
| MVP-05 | Template details and previews | Keep in MVP |
| MVP-06 | Customer registration and authentication | Keep in MVP |
| MVP-07 | Customer dashboard | Keep in MVP |
| MVP-08 | Basic website customization | Keep in MVP |
| MVP-09 | Purchase and order request workflow | Keep in MVP |
| MVP-10 | Administrator dashboard | Keep in MVP |
| MVP-11 | Responsive design | Keep in MVP |
| MVP-12 | Basic security and data protection | Keep in MVP |
| MVP-13 | Payment recording and verification | Keep in MVP |
| MVP-14 | Website delivery or publishing workflow | Keep in MVP |

These features must work together to provide a usable first release.

## 4. Website Customization Decision

### 4.1 Initial Approach

Webify will initially use a controlled component-based customization interface.

Customers will be able to modify predefined website elements without needing programming knowledge.

### 4.2 Supported Customization

The initial editor should support:

- Editing text.
- Replacing images.
- Changing approved colors.
- Editing buttons and links.
- Updating contact information.
- Previewing changes.
- Saving customization changes.

### 4.3 Explicit Limitations

The first release will not require:

- An unrestricted drag-and-drop editor.
- Custom JavaScript execution.
- Custom server-side code execution.
- Advanced animation controls.
- Complex layout manipulation.
- Advanced responsive editing.

### 4.4 Security and Data Isolation

The customization system must:

1. Validate website content on the backend.
2. Allow only approved components and properties.
3. Restrict customers to websites they own.
4. Store customer customization data separately from the original template.
5. Prevent future template updates from unexpectedly overwriting customer websites.
6. Maintain appropriate website versions.

### 4.5 Implementation Direction

A custom component-based editor is the proposed direction for the MVP.

GrapesJS remains an alternative for future prototyping if customer requirements justify a more advanced visual editor.

The proposed approach must be validated through a small technical prototype before full implementation.

## 5. Payment Strategy Review

### 5.1 Business Requirement

Webify must provide a reliable process for customers to pay for selected templates and website services.

Payment-provider eligibility must be verified before choosing an online payment integration.

### 5.2 Provider Investigation

The initial investigation identifies:

- MyMonty / Monty Finance as a local payment-gateway candidate.
- PayTabs as another provider requiring confirmation of Lebanese merchant onboarding and commercial terms.
- Stripe as unsuitable for a standard account opened using only Lebanese business registration under its currently published supported-country list.

These findings are preliminary and do not constitute merchant approval.

### 5.3 MVP Payment Requirements

The system must:

- Associate payments with the correct orders.
- Record payment method, amount and status.
- Allow authorized administrators to review payments.
- Verify payment notifications before updating payment status.
- Prevent duplicate transaction processing.
- Keep payment records available for administrative review.

### 5.4 Fallback Approach

If an eligible online payment integration is unavailable, Webify may use an administrator-verified manual payment process, subject to legal and operational review.

The system must not mark an order as paid until payment has been verified.

### 5.5 Final Decision Status

**Decision:** Payment recording and verification remain P0.

**Pending:** Final payment provider selection, merchant eligibility confirmation, commercial terms and integration testing.

## 6. Features Postponed Until After MVP

### 6.1 P1 — Should Have

The following features may be implemented after the core MVP or included if resources allow without delaying launch.

| Feature | Reason for postponement |
|---|---|
| Advanced template filters | Basic category filtering and search are sufficient initially |
| Favorites | Not essential to complete the purchase journey |
| Customer email notifications | Can be improved after core order workflows |
| Improved interactive previews | Basic template previews are sufficient initially |
| Multiple website pages | Begin with a manageable customization scope |
| Advanced image management | Basic image replacement is sufficient |
| SEO settings | Can be introduced after the initial publishing workflow |
| Arabic and English interface | Plan architecture for localization, then prioritize based on customer validation |
| Customer support form | Can initially use a simple contact method |
| Basic analytics | Can follow after initial marketplace usage |

### 6.2 P2 — Future Enhancements

The following features are excluded from the first release:

**Advanced Website Builder**
- Full drag-and-drop editor.
- Advanced component library.
- Custom layout grids.
- Reusable sections.
- Advanced responsive editing.
- Undo and redo history.
- Advanced animation controls.

**Advanced E-commerce**
- Complete online store builder.
- Product and inventory management.
- Shopping carts for customer websites.
- Customer checkout management.
- Shipping integrations.
- Advanced tax calculations.

**Agency Features**
- Agency accounts.
- Multiple team members.
- Client management.
- Team collaboration.
- White-label services.
- Agency subscriptions.

**Advanced Publishing and Infrastructure**
- Automatic custom-domain provisioning.
- Advanced hosting management.
- Website version rollback interface.
- Multiple deployment environments.
- Advanced uptime monitoring.

**Business and Growth**
- AI website generation.
- Third-party template creator marketplace.
- Revenue sharing.
- Affiliate programs.
- Customer reviews and ratings.
- Advanced analytics.
- International payment expansion.
- Complex subscription billing.

These features can be reconsidered after the MVP has been tested with real customers.

## 7. Technology Scope Review

The proposed initial technology stack remains:

| Layer | Technology |
|---|---|
| Frontend | Next.js, React, TypeScript |
| Styling | Tailwind CSS |
| Backend | NestJS, TypeScript |
| Database | PostgreSQL |
| ORM | Prisma |
| Authentication | Secure session-based authentication |
| Website Editor | Custom component-based controlled editor |
| File Storage | S3-compatible storage or Cloudinary |
| Testing | Vitest/Jest and Playwright |
| Version Control | Git and GitHub |

### Architecture Decision

Webify will begin with a modular monolith architecture.

Microservices will not be introduced during the initial MVP unless a demonstrated technical requirement justifies them.

The editor and payment integrations should be designed so that future providers or implementation approaches can be introduced without redesigning the entire platform.

## 8. MVP Dependencies and Risks

| Dependency or Risk | Required Action |
|---|---|
| Payment-provider availability in Lebanon | Confirm merchant eligibility and commercial terms |
| Website editor complexity | Validate the controlled editor through a small prototype |
| Hosting costs | Compare hosting providers and estimate operating costs |
| Website security | Implement backend validation and ownership controls |
| Data loss | Configure automated backups and test restoration |
| Website publishing | Validate the delivery and publishing workflow |
| Customer adoption | Conduct customer interviews and collect feedback |

## 9. Updated MVP Release Criteria

The MVP will be considered ready for beta or production release when:

1. The homepage and marketplace are functional.
2. Visitors can browse and preview published templates.
3. Customers can register and log in securely.
4. Customers can submit orders or purchase requests.
5. Administrators can manage templates, categories, customers and orders.
6. Payment status can be recorded and verified.
7. Customers can customize approved website content.
8. Customers can preview and save customization changes.
9. Customer website ownership and data isolation are enforced.
10. A reliable website delivery or publishing workflow exists.
11. Core customer workflows pass functional testing.
12. Desktop and mobile experiences are usable.
13. No critical unresolved security vulnerabilities remain.
14. Production database backups are configured and restoration is tested.
15. Payment and order-status workflows are tested successfully.
16. Publishing and website ownership isolation are verified.
17. Required business and legal policies are prepared.

## 10. Scope Change Management

Any feature proposed for addition to the MVP must be evaluated before implementation.

The review should consider:

- Business value.
- Customer demand.
- Development effort.
- Technical complexity.
- Security impact.
- Testing requirements.
- Schedule impact.
- Hosting and operating costs.

Features that are not essential to the first customer journey should normally remain outside the initial MVP.

## 11. Review Outcome

The review confirms that the original Webify MVP scope remains suitable as the foundation for initial development.

The main clarifications are:

1. Use controlled component-based customization initially.
2. Keep unrestricted drag-and-drop functionality outside the MVP.
3. Verify payment-provider eligibility before integrating online payments.
4. Keep an approved manual payment workflow as a potential fallback.
5. Protect customer websites through ownership checks and version isolation.
6. Validate the editor and publishing workflow before full implementation.
7. Test database backup restoration before production release.

The original `mvp-features.md` remains the primary MVP specification. This review records the decisions and refinements made on November 27, 2026.

---

**Document Owner:** Webify Project Owner  
**Version:** 1.0  
**Status:** Proposed — Pending Final Review

*Webify — Build. Customize. Launch.*