# Webify — Website Editor Technology Evaluation

**Version:** 1.0  
**Date:** November 27, 2026  
**Status:** Architecture Decision — Proposed

## 1. Objective

Evaluate GrapesJS against a custom component-based editor to select a suitable approach for Webify's initial website customization functionality.

## 2. Option A — GrapesJS

GrapesJS is an open-source web builder framework for creating and editing website templates.

### Advantages
- Provides a visual editing canvas.
- Includes component and block management.
- Supports custom component types and plugins.
- Includes style editing capabilities.
- Provides project data storage and loading.
- Reduces the amount of editor functionality that must be built from scratch.

### Disadvantages
- Requires learning and configuring its architecture.
- Its default editing experience may need significant customization to match Webify's design.
- Requires careful control over allowed HTML, CSS, components and exported content.
- Integration with a React/Next.js application needs careful lifecycle management.
- A general-purpose editor may expose more functionality than the MVP requires.

## 3. Option B — Custom Component-Based Editor

A custom editor would use predefined React components and controlled editing panels.

### Advantages
- Complete control over the user interface.
- Easier to restrict customers to approved components.
- Better alignment with Webify's templates and design system.
- Easier to define structured website data.
- Can start with simple editing controls rather than advanced drag-and-drop.

### Disadvantages
- More development work for editor functionality.
- Requires building selection, editing, preview and save behavior.
- Advanced drag-and-drop features require additional implementation.
- More responsibility for maintaining editor functionality.

## 4. Comparison

| Evaluation Area | GrapesJS | Custom Editor |
|---|---|---|
| Initial development speed | Faster for a broad visual editor | Faster only for a very limited editor |
| Drag-and-drop | Available | Must be implemented |
| UI customization | Configurable | Full control |
| Component restrictions | Requires configuration | Easier to enforce |
| Template integration | Requires adaptation | Designed around Webify's templates |
| Maintenance | Framework and plugins | Fully owned implementation |
| Security | Requires strict configuration and validation | Requires strict validation and safe rendering |
| MVP suitability | Good for prototyping | Strong for controlled customization |

## 5. Security Considerations

Regardless of the selected editor:

- Never trust customer-provided HTML, CSS or JavaScript.
- Never execute arbitrary customer-provided server-side code.
- Validate saved website data on the backend.
- Restrict available components and editable properties.
- Validate links and uploaded assets.
- Enforce customer ownership checks.
- Store structured, versioned website data.
- Sanitize content before rendering where appropriate.

## 6. Recommendation

**Recommended for the first MVP: Custom component-based controlled editor.**

Webify's first release does not require a complete unrestricted website builder. Customers initially need to edit approved content such as:

- Text.
- Images.
- Colors.
- Buttons and links.
- Contact information.

A controlled editor will reduce initial complexity and allow Webify to keep customer websites consistent with the selected templates.

GrapesJS should remain a candidate for a later prototype if customer research demonstrates demand for advanced drag-and-drop functionality.

## 7. Proposed Implementation Direction

1. Create a reusable library of approved website components.
2. Define a structured JSON schema for website content.
3. Build editing panels for approved component properties.
4. Display changes in a live preview.
5. Save versioned website data through the backend.
6. Validate ownership and content before saving.
7. Keep the editor architecture extensible for future drag-and-drop functionality.

## 8. Final Decision

For the initial MVP, use a custom component-based controlled editor.

Do not implement advanced drag-and-drop functionality until the core marketplace and customization workflow has been validated.

**Decision status:** Proposed and documented; validate through a small technical prototype before committing to full implementation.

## 9. References

- GrapesJS official documentation: https://grapesjs.com/docs/
- Component Manager: https://grapesjs.com/docs/modules/Components.html
- Storage Manager: https://grapesjs.com/docs/modules/Storage.html
- GrapesJS repository and license: https://github.com/GrapesJS/grapesjs

