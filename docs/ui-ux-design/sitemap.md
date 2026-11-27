# WEBIFY — WEBSITE SITEMAP

**Project:** Webify  
**Document:** Website Sitemap  
**Version:** 1.0  
**Date:** November 27, 2026  
**Status:** Initial Draft — Pending UI/UX Review  
**Project Owner:** Rodolph Habib

---

## 1. Introduction

### 1.1 Purpose

This document defines the information architecture and website structure of Webify.

It identifies the main pages, subpages, navigation hierarchy, and access requirements for visitors, registered customers, and administrators.

The sitemap will guide the UI/UX design process and serve as a reference during frontend development.

### 1.2 Product Overview

Webify is a website-template marketplace that enables customers to browse professionally designed templates, preview available designs, purchase or request templates, customize website content through a controlled editor, and receive completed websites.

The platform also offers additional custom website development services.

The initial target market is Lebanon, with international expansion planned for the future.

### 1.3 Scope

This sitemap covers:

- Public-facing website pages.
- Customer authentication and account pages.
- Customer dashboard and website management.
- Template browsing and ordering.
- Website customization and preview.
- Administrative dashboard and management pages.
- Supporting legal and informational pages.

Features outside the initial MVP are identified separately.

---

## 2. Sitemap Hierarchy

The Webify platform is divided into three main sections:

1. Public Website
2. Customer Dashboard
3. Administrator Dashboard

### 2.1 Public Website

These pages are accessible without authentication unless otherwise specified.

```text
Webify
│
├── Home (/)
│
├── Marketplace (/marketplace)
│   │
│   ├── All Templates
│   │
│   ├── Categories (/marketplace/categories)
│   │   ├── Business
│   │   ├── Portfolio
│   │   ├── Restaurant
│   │   ├── E-commerce
│   │   ├── Organization
│   │   └── Other Categories
│   │
│   ├── Search Results
│   │
│   └── Template Details (/templates/:slug)
│       ├── Template Preview
│       ├── Description
│       ├── Features
│       ├── Included Pages
│       ├── Pricing
│       └── Select Template
│
├── Custom Development (/custom-development)
│   ├── Services
│   ├── Development Process
│   └── Request a Project
│
├── About Us (/about)
│
├── Contact Us (/contact)
│
├── FAQ (/faq)
│
├── Authentication
│   ├── Login (/login)
│   ├── Register (/register)
│   ├── Forgot Password (/forgot-password)
│   └── Reset Password (/reset-password)
│
├── Legal
│   ├── Terms and Conditions (/terms)
│   ├── Privacy Policy (/privacy)
│   └── Refund Policy (/refund-policy)
│
└── Error Pages
    ├── 404 Not Found
    └── 500 Server Error
```

### 2.2 Customer Dashboard

These pages require an authenticated customer account.

```text
Customer Dashboard (/dashboard)
│
├── Overview (/dashboard)
│
├── My Websites (/dashboard/websites)
│   │
│   └── Website Details (/dashboard/websites/:id)
│       ├── Website Information
│       ├── Edit Website
│       ├── Preview Website
│       ├── Save Changes
│       └── Publishing / Delivery Status
│
├── My Orders (/dashboard/orders)
│   │
│   └── Order Details (/dashboard/orders/:id)
│       ├── Order Information
│       ├── Selected Template
│       ├── Payment Status
│       └── Order Progress
│
├── Customization Editor (/dashboard/websites/:id/editor)
│   ├── Content Editing
│   ├── Image Management
│   ├── Approved Color Settings
│   ├── Button and Link Settings
│   ├── Live Preview
│   └── Save Changes
│
├── Notifications (/dashboard/notifications)
│
├── Account Settings (/dashboard/settings)
│   ├── Personal Information
│   ├── Email and Password
│   └── Account Management
│
└── Support (/dashboard/support)
    ├── Help Center
    └── Contact Support
```

### 2.3 Administrator Dashboard

These pages require administrator authentication and appropriate permissions.

```text
Admin Dashboard (/admin)
│
├── Overview (/admin)
│   ├── Platform Statistics
│   ├── Recent Orders
│   ├── Recent Customers
│   └── Revenue Summary
│
├── Template Management (/admin/templates)
│   ├── All Templates
│   ├── Add Template
│   ├── Edit Template
│   ├── Template Categories
│   └── Publish / Unpublish Template
│
├── Customer Management (/admin/customers)
│   ├── All Customers
│   └── Customer Details
│
├── Order Management (/admin/orders)
│   ├── All Orders
│   ├── Order Details
│   ├── Update Order Status
│   └── Delivery Management
│
├── Payment Management (/admin/payments)
│   ├── All Payments
│   ├── Payment Details
│   └── Payment Verification
│
├── Website Management (/admin/websites)
│   ├── Customer Websites
│   └── Website Delivery Status
│
├── Custom Development Requests (/admin/requests)
│   ├── All Requests
│   └── Request Details
│
├── Support Management (/admin/support)
│   └── Customer Inquiries
│
└── Admin Settings (/admin/settings)
    ├── Administrator Profile
    └── Platform Settings
```

---

## 3. Navigation Structure

### 3.1 Public Navigation

The main navigation bar should provide access to:

| Navigation Item | Destination |
|---|---|
| Logo | Home |
| Home | `/` |
| Marketplace | `/marketplace` |
| Custom Development | `/custom-development` |
| About | `/about` |
| Contact | `/contact` |
| Login | `/login` |
| Get Started / Sign Up | `/register` |

The marketplace should be the primary navigation destination because browsing templates is the main customer acquisition journey.

### 3.2 Customer Navigation

The customer dashboard should use a sidebar or dashboard navigation menu.

| Navigation Item | Destination |
|---|---|
| Overview | `/dashboard` |
| My Websites | `/dashboard/websites` |
| My Orders | `/dashboard/orders` |
| Notifications | `/dashboard/notifications` |
| Account Settings | `/dashboard/settings` |
| Support | `/dashboard/support` |
| Log Out | Authentication action |

### 3.3 Administrator Navigation

The administrator dashboard should use a dedicated sidebar.

| Navigation Item | Destination |
|---|---|
| Overview | `/admin` |
| Templates | `/admin/templates` |
| Customers | `/admin/customers` |
| Orders | `/admin/orders` |
| Payments | `/admin/payments` |
| Websites | `/admin/websites` |
| Custom Requests | `/admin/requests` |
| Support | `/admin/support` |
| Settings | `/admin/settings` |
| Log Out | Authentication action |

---

## 4. Main Customer Journey

The sitemap should support the following primary customer journey:

```text
Homepage
   |
   v
Marketplace
   |
   v
Browse / Search Templates
   |
   v
Template Details
   |
   v
Preview Template
   |
   v
Select Template
   |
   v
Register / Login
   |
   v
Submit Order
   |
   v
Payment / Payment Verification
   |
   v
Order Confirmation
   |
   v
Customer Dashboard
   |
   v
Customize Website
   |
   v
Preview and Save
   |
   v
Website Delivery / Publishing
```

The platform must clearly communicate each stage and the current order status.

---

## 5. Page Access and Permissions

| Page Section | Visitor | Customer | Administrator |
|---|---|---|---|
| Homepage | Yes | Yes | Yes |
| Marketplace | Yes | Yes | Yes |
| Template Details | Yes | Yes | Yes |
| Login / Register | Yes | Limited | Limited |
| Customer Dashboard | No | Yes | As authorized |
| Website Editor | No | Yes, own websites | As authorized |
| Customer Orders | No | Own orders | All orders |
| Payment Management | No | Own payment status | Authorized |
| Template Management | No | No | Authorized |
| Customer Management | No | No | Authorized |
| Admin Dashboard | No | No | Authorized |

All protected routes must enforce authorization on the backend. Hiding a page or menu item in the frontend is not sufficient security.

Customers must only access their own websites, orders, and payment information.

Administrator access must be restricted by role and permission.

---

## 6. MVP and Future Scope

Not every page in the complete sitemap must be implemented in the first release.

### 6.1 MVP Pages — P0

The following pages are required for the initial Webify release:

**Public Website**
- Homepage
- Marketplace
- Template Categories
- Search Results
- Template Details and Preview
- About Us
- Contact Us
- Login
- Register
- Forgot / Reset Password
- Terms and Conditions
- Privacy Policy
- Refund Policy
- 404 Error Page

**Customer Dashboard**
- Dashboard Overview
- My Websites
- Website Details
- My Orders
- Order Details
- Website Customization Editor
- Website Preview
- Account Settings

**Administrator Dashboard**
- Admin Overview
- Template Management
- Customer Management
- Order Management
- Payment Management
- Website Delivery Management

### 6.2 Future Pages — P1

These pages can be introduced after the core MVP journey is operational:

- FAQ and Help Center
- Customer Notifications
- Advanced Support Management
- Advanced Website Management
- Additional customer website pages
- Enhanced analytics
- Improved account preferences
- Arabic and English interface enhancements, including RTL support

### 6.3 Future Expansion — P2

Potential future additions include:

- Advanced drag-and-drop editor
- E-commerce management dashboard
- Agency accounts and team management
- Affiliate program
- AI-assisted website customization
- Advanced analytics and reporting
- International marketplace features

These features are not part of the initial MVP commitment.

---

## 7. URL and Routing Conventions

Webify should follow consistent and understandable URL conventions.

Examples:

| Page | Proposed URL |
|---|---|
| Homepage | `/` |
| Marketplace | `/marketplace` |
| Category | `/marketplace/categories/business` |
| Template Details | `/templates/business-template` |
| Login | `/login` |
| Registration | `/register` |
| Customer Dashboard | `/dashboard` |
| Customer Website | `/dashboard/websites/123` |
| Website Editor | `/dashboard/websites/123/editor` |
| Customer Order | `/dashboard/orders/123` |
| Admin Dashboard | `/admin` |
| Admin Templates | `/admin/templates` |
| Admin Orders | `/admin/orders` |

Routing requirements:

1. Use lowercase URLs.
2. Use descriptive page names.
3. Use URL slugs for publicly accessible template pages.
4. Use unique identifiers for customer-owned resources.
5. Protect private routes with authentication and authorization.
6. Avoid exposing sensitive customer information in URLs.
7. Provide clear navigation and breadcrumb trails where appropriate.

The example numeric identifiers are illustrative, not actual database IDs.

---

## 8. Search and Navigation Requirements

The marketplace should provide:

- Search by template name.
- Search by relevant keywords.
- Browse by category.
- Clear links to template details.
- A way to return to search results.
- Clear navigation between marketplace and template pages.

Customer and administrator dashboards should provide consistent navigation across their respective sections.

Navigation should remain understandable on desktop, tablet, and mobile devices.

---

## 9. UI/UX Design Considerations

The sitemap should guide the following design principles:

- Keep the public navigation simple and focused on template discovery.
- Make the marketplace easy to browse.
- Ensure template previews and details are easy to access.
- Make registration and ordering straightforward.
- Use a consistent sidebar for customer dashboard navigation.
- Use a separate administrative navigation structure.
- Clearly distinguish customer and administrator interfaces.
- Provide loading, empty, error, and success states for important pages.
- Design responsive layouts for different screen sizes.
- Plan for Arabic, English, and RTL support.

---

## 10. Assumptions and Decisions Requiring Review

The following points require confirmation during subsequent design and development:

1. Whether custom development requests should have a separate public page and workflow.
2. Whether customers will receive a website preview before final delivery.
3. Whether website publishing will be automated or initially handled by an administrator.
4. Whether notifications will be available in the MVP.
5. Whether the marketplace will support multiple pages per customer website at launch.
6. Whether customers will have a dedicated support ticket system or use a simpler contact workflow.

These decisions should be documented and reflected in the relevant requirements before implementation.

---

## 11. Acceptance Criteria

This sitemap is considered ready for UI/UX design review when:

- [ ] All major public website pages are identified.
- [ ] Customer dashboard pages are identified.
- [ ] Administrator dashboard pages are identified.
- [ ] Navigation hierarchy is documented.
- [ ] Primary customer journey is mapped.
- [ ] Page access and permissions are defined.
- [ ] MVP pages are separated from future features.
- [ ] URL and routing conventions are proposed.
- [ ] Navigation requirements are documented.
- [ ] The sitemap is consistent with Webify's MVP requirements.

---

## 12. Conclusion

This sitemap establishes the proposed information architecture for Webify.

It provides a structured foundation for designing the public marketplace, customer dashboard, website customization experience, and administrator dashboard.

The sitemap will be used as a reference for the next UI/UX tasks, particularly customer and administrator user flows.

**Document Status:** Initial Draft — Pending UI/UX Review.

