---
name: Ahmed Al-Jarmoozi
neptun: Y8AJ2T
id: 2026-LG-05
github: https://github.com/ahmadhas08-sys/Project-INT-Al-Jarmoozi
trello: "https://trello.com/b/Vt8Yqrj7/my-trello-board"
---
# GitHub Projects Portfolio Observatory

Teams often manage work across several GitHub Projects with different status labels, priority scales, assignees, and deadlines. Although each GitHub Project provides its own view, stakeholders lack a consistent way to understand the overall portfolio, identify neglected work, and see what has changed over time. Manually opening and comparing several boards is time-consuming and can hide risks.

The **GitHub Projects Portfolio Observatory** is a web-based, read-oriented monitoring and decision-support application. It connects to authorized GitHub Projects, allows users to map project-specific fields into a common model, collects historical information, and presents a unified view through personal, team/project, and read-only company dashboards. It complements GitHub Projects rather than replacing it.

## Objectives
- **Primary objective:** Help users understand and monitor work across multiple GitHub Projects from one place.
- **Target users / stakeholders:** Individual contributors, team or office leads, portfolio managers, and read-only dashboard viewers.
- **Measurable success criteria:**
  - An authorized user can connect and display at least two GitHub Projects with different field labels.
  - Configured field mappings produce consistent status, priority, assignee, and optional due-date information.
  - Users can switch among personal, project/team, and read-only portfolio views.
  - The system identifies qualifying stale, overdue, soon-due, blocked, unassigned, and high-priority items where sufficient data exists.
  - A change feed shows detected changes in high-priority items using retained historical observations.
  - Users see clear feedback when access is denied, data is unavailable, or collection fails.
- **Constraints:** Use the official GitHub Projects v2 API; support authorized read access; use TypeScript; protect credentials; accommodate different project configurations; preserve sufficient history for change-based features; and provide tests for normalization, rules, and an API integration boundary.

## Scope
### In scope
- Authorized connection to multiple user- or organization-owned GitHub Projects.
- Selection of monitored Projects and mapping of custom status, priority, assignee, and optional deadline fields into a common model.
- Unified work-item display with source-project context.
- Personal dashboard for work relevant to the signed-in user.
- Project/team dashboard for comparing monitored Projects.
- Read-only company/wall dashboard for portfolio-level monitoring.
- Configurable stale-item detection and supported overdue, soon-due, blocked, unassigned, and high-priority indicators.
- Persistent historical observations and a recent-changes feed for high-priority work.
- Understandable empty, loading, authentication, permission, rate-limit, and API-error states.

### Out of scope
- Replacing GitHub Projects or becoming a full task-editing application.
- Editing GitHub work items, statuses, or assignments from the observatory in the initial version.
- Supporting unrelated project-management providers in the initial version.
- Promising detection of fields or states that a source Project does not expose or that have not been mapped.
- AI-generated summaries, notifications, advanced forecasting, and capacity planning as mandatory initial features. AI assistance is a candidate extension to investigate with the supervisor.

## Notes
The first functional demonstration should show two differently configured GitHub Projects becoming one understandable monitoring view. The specification will define roles, user journeys, functional requirements, business rules, and testable acceptance criteria. The implementation architecture, technology comparisons, historical-storage approach, and any cost-conscious AI integration will be developed for the later technical proposal rather than treated as decided here.

**Decisions requiring confirmation:** exact dashboard access model; definition of an open item; configurable staleness threshold; mapping of blocked/high-priority values; default soon-due window; and scope of the initial implementation milestone.
