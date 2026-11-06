# SEEK International CMS — Prototype

A self-contained, browser-based content management system prototype for managing a SEEK International-style informational website.

## Run it

1. Extract the ZIP file (if using the ZIP package).
2. Open `index.html` in a modern browser (Chrome, Edge, Firefox, or Safari).
3. No package installation or internet connection is required.

## Implemented prototype functions

- CMS dashboard with content counts and shortcuts
- Create, edit, delete, search, and filter for pages, homepage sections, programs/services, About Us sections, team members, testimonials, news/events, menu items, and users
- Draft / Published / Archived content status
- Contact inquiry viewing and status updates
- Media asset metadata management
- Website preview generated from sample content
- SEO defaults and per-page SEO fields
- Website organization and social-link settings
- Browser localStorage persistence
- JSON export and import backup

## Important scope / production gaps

This is a **frontend workflow prototype**, not a production CMS. Data is stored in the browser that opens the file. There is no server/database, real authentication, permission enforcement, multi-user collaboration, public website API, real file upload storage, email notification, or production deployment. The media manager currently stores asset metadata only. These capabilities require a backend and hosting/storage integration.

The linked Figma prototype could not be retrieved from this environment. The admin UI and sample content are therefore a proposed starting point and should be visually reconciled against the actual Figma screens before client sign-off. Replace sample organization copy, programs, people, and testimonials with client-approved content.

## Suggested production architecture

- Frontend/admin: Next.js or React
- Backend/API: Next.js server routes, NestJS, or another approved API framework
- Database: PostgreSQL
- Authentication: secure session-based authentication with MFA for administrators
- Media storage: S3-compatible object storage or approved cloud media service
- Roles: Super Admin, Admin, Editor, Reviewer
- Publishing: Draft → Review → Published, with audit history and scheduled publishing

## Suggested core data entities

Users, Roles, Permissions, Pages, PageSections, Programs, AboutSections, TeamMembers, Testimonials, NewsEvents, MediaAssets, Menus, ContactInquiries, SEOSettings, SiteSettings, and AuditLogs.
