# Webify

**Build. Customize. Launch.**

Webify is a website template marketplace and visual website-building platform designed to help individuals, entrepreneurs, and businesses create professional websites without starting from scratch.

Users will be able to explore ready-made website templates, preview designs, purchase templates, customize their websites using a visual drag-and-drop editor, and publish their websites online.

Webify will initially focus on the Lebanese market, with plans to expand internationally.

---

## Project Status

**Status:** Project Initiation & Planning  
**Version:** 0.1.0  
**Project Start:** November 2026

Webify is currently in its planning and design phase. Requirements, architecture, user experience, and technical foundations are being defined before implementation begins.

## Vision

Our vision is to make professional website creation more accessible by combining a template marketplace, an intuitive visual website builder, and professional custom development services in one platform.

## Main Features

### 1. Website Marketplace
- Browse professionally designed website templates.
- Search and filter templates by category.
- Preview templates before purchasing.
- View template details, features, and pricing.
- Access purchased templates.

### 2. Visual Website Builder
- Customize website layouts visually.
- Drag and drop website components.
- Edit text, images, colors, and typography.
- Preview websites across different screen sizes.
- Save and manage website changes.

### 3. Website Publishing
- Publish customized websites.
- Support hosted website subdomains.
- Configure custom domains.
- Manage published websites.

### 4. Customer Dashboard
- Manage account information.
- View purchased templates.
- Manage created websites.
- Track orders and project progress.
- Access website settings.

### 5. Custom Development Services
- Request professionally developed websites.
- Submit project requirements.
- Communicate project needs.
- Track custom development requests.

### 6. Administration
- Manage users and customer accounts.
- Manage website templates.
- Manage orders and payments.
- Review custom development requests.
- Monitor platform activity.

## Technology Stack

The following technologies are the proposed technical baseline. Final decisions will be documented through architecture decision records (ADRs).

| Layer | Technology |
|---|---|
| Frontend | Next.js, React, TypeScript |
| Styling | Tailwind CSS |
| Backend | NestJS, TypeScript |
| Database | PostgreSQL |
| ORM | Prisma |
| Visual Builder | GrapesJS prototype / custom editor |
| Version Control | Git & GitHub |
| UI/UX Design | Figma |
| Testing | Vitest / Jest / Playwright |
| CI/CD | GitHub Actions |
| File Storage | S3-compatible storage / Cloudinary |

## Planned Repository Structure

```text
webify/
│
├── apps/
│   ├── web/                  # Customer-facing application
│   └── api/                  # Backend API
│
├── packages/
│   └── shared/               # Shared types and utilities
│
├── docs/
│   ├── requirements/
│   │   ├── project-charter.md
│   │   ├── srs.md
│   │   └── user-stories.md
│   │
│   ├── architecture/
│   │   ├── system-architecture.md
│   │   ├── database-design.md
│   │   └── adr/
│   │
│   ├── design/
│   │   ├── design-system.md
│   │   └── user-flows.md
│   │
│   ├── testing/
│   ├── deployment/
│   └── project-management/
│
├── .github/
│   ├── ISSUE_TEMPLATE/
│   └── workflows/
│
├── .gitignore
├── README.md
└── LICENSE
```

*This is the planned structure. Directories will be created as the corresponding development phases begin.*

## Development Roadmap

| Phase | Description |
|---|---|
| 01 | Project initiation and requirements engineering |
| 02 | UX/UI research and Figma design |
| 03 | Marketplace frontend development |
| 04 | Backend architecture and authentication |
| 05 | Template management and catalog |
| 06 | Visual website builder MVP |
| 07 | Orders and payment integration |
| 08 | Website publishing and domains |
| 09 | Custom development workflow |
| 10 | Testing, security, and beta release |
| 11 | Public MVP launch |
| 12 | Improvements and international expansion |

## Development Principles

Webify will follow professional software engineering practices:

- Requirements will be documented before implementation.
- Features will be divided into manageable tasks and milestones.
- Git branches will be used for individual features and fixes.
- Code changes will be reviewed before merging.
- Automated testing will be introduced throughout development.
- Security, performance, accessibility, and maintainability will be considered from the beginning.
- Technical decisions will be documented.
- Every release will have a documented version and change history.

## Git Workflow

The project will follow a structured Git workflow.

**Main branches:**

- `main` — stable and production-ready code.
- `develop` — integration branch for ongoing development.
- `feature/*` — new functionality.
- `fix/*` — bug fixes.
- `docs/*` — documentation changes.

Example:

```bash
git checkout -b feature/user-authentication
```

## Getting Started

The application is currently in the planning phase. Installation instructions and development commands will be added when the initial application structure is implemented.

## Documentation

Project documentation will be maintained in the `docs/` directory.

It will include:

- Software Requirements Specification (SRS).
- Functional and non-functional requirements.
- User stories and acceptance criteria.
- System architecture and database design.
- UI/UX designs and user flows.
- Testing documentation.
- Deployment and maintenance procedures.

## Target Market

**Initial market:** Lebanon  
**Future market:** International

The platform will consider multilingual support, including English and Arabic, with right-to-left (RTL) interface support.

## License

All rights reserved.

Webify is a proprietary project. No permission is granted to copy, distribute, modify, or commercially use this project without written authorization from its owner.

---

**Webify — Build. Customize. Launch.**