# Spearfish Platform Changelog

Release notes for the Spearfish platform. Entries are summarized at the product level;
internal details are omitted.

## 2026-09-17
- Strengthened access controls on platform services.

## 2026-09-16
- Strengthened access controls on role assignment across tenants.
- The partner ingestion API now accepts API key authentication as well as bearer tokens.
- Web app: Fixed assigning and removing user roles so changes apply in the correct tenant.

## 2026-09-15
- Web app: Added drill-through and links to records from native dashboard tables, KPIs and gauges.
- Web app: Added column settings and column ordering for native dashboard tables, and value suffixes for KPIs and gauges.
- Web app: Fixed gauges with wide bands or on short cards, and drill-through banners that listed filters the page had not applied.

## 2026-09-12
- Native dashboards now support optional filter clauses, apply filter default values, and resolve filter columns correctly.
- Fixed signal values backed by reference data showing as unmapped.

## 2026-09-11
- Fixed QA evidence highlights so they point to the right part of the transcript.
- Fixed how filters are applied inside native dashboard queries.
- Added an audit trail for data retention and deletion actions.
- Web app: Added an audit history view to the Data Retention & Deletion card.
- Web app: The AI Assistant now reports connection problems, retries the initial connection and recovers stale conversations.

## 2026-09-07
- Maintenance and reliability improvements.

## 2026-09-06
- Added tenant data retention policies and a request-and-approve process for full data deletion.
- Fixed filter values not being passed to Metabase dashboards.
- Improved per-question QA analytics by counting abstentions separately.
- Web app: Added a Data Retention & Deletion card to tenant details.
- Web app: Added copying of dashboard views and restoring of archived views.
- Web app: Added per-card filters, multi-value filters and explicit card placement on dashboards.
- Web app: Dashboard pages now load their cards faster.
- Web app: Dashboards now show which other views will change before a query is unbound.
- Web app: Fixed card selection being lost when reordering, removing or duplicating cards, and the sizing of the Edit query dialog.
- Web app: Outcome review items in the inbox now have their own label.

## 2026-09-04
- New dashboard workspaces are now created on native dashboards.
- Added support for multi-value filters in dashboard queries.
- Improved QA evaluation accuracy by giving the evaluator a timed transcript with speaker labels.
- The CallRail integration can now include additional call fields.
- Expanded and corrected the MCP connector's dashboard tools.
- Fixed Metabase sign-in and template filter handling in some cases.

## 2026-08-31
- Fixed QA evaluations so they always score against the published form version.
- Improved reliability of QA evaluations.
- Web app: Not-found pages now appear immediately, and copied links to inbox items open the item.
- Web app: Fixed the inbox failing to load when it contained an unrecognised item type.

## 2026-08-29
- Improved speaker identification in transcripts for both single-channel and multi-channel recordings.

## 2026-08-28
- Added an ingestion API for partners to send interactions, recordings and transcripts, including CSV and SFTP delivery.
- HubSpot form submissions are now linked to the customer who submitted them.
- Added the option to exclude specific skills from NICE CXone ingestion.

## 2026-08-27
- Improved matching of interactions to the same customer across data sources.
- Improved reliability of NICE CXone recording sync.
- Improved reliability of the AI Assistant in long conversations.
- Web app: Simplified the signal authoring form.
- Web app: The AI Assistant now tells you when a response fails.

## 2026-08-26
- Signals now have a dedicated instruction field, separate from their description.
- Improved reliability of call transcription.

## 2026-08-25
- Fixed CallRail call times recorded with the wrong time zone offset.
- Strengthened authorization enforcement and stopped error responses revealing internal details.
- Web app: Refreshed the visual design, typography and sidebar navigation.
- Web app: Redesigned signal authoring.
- Web app: Added an admin area for signal tiers, vocabularies, subjects and personas.
- Web app: Added a Feedback list with item details, links to the related record, status filters and actions.
- Web app: The theme now follows changes to the system light or dark setting.
- Web app: The transcript timeline now shows analysis annotations as chips.
- Web app: Improved accessibility of icon-only buttons.
- Web app: Fixed the AI Assistant hanging while connecting or when no assistants are available.
- Web app: Fixed inbox pagination and a spurious error message on signal pages.
- Web app: Strengthened protection of account sessions.

## 2026-08-20
- HubSpot interactions now link to the customer and show the customer's name.
- Added protection against conflicting edits to signal definitions overwriting each other.

## 2026-08-19
- Added management of signal personas.
- Fixed QA evaluations to respect the insufficient-evidence setting.
- Fixed the inbox combining separate findings about the same record.
- Added ingestion of HubSpot events.
- Strengthened authorization checks across platform services.

## 2026-08-18
- Added sorting to the integrations connections list, and fixed status filtering across pages.
- HubSpot interactions now show the agent's name.
- Fixed HubSpot call recording downloads and improved HubSpot data ingestion.
- Improved reliability of NICE CXone ingestion.
- Improved signal processing speed.
- Added management of signal tiers, vocabularies and subjects, and revision history for signal definitions.
- Fixed sign-in and consent for the MCP connector.
- Strengthened access controls for API clients.
- Web app: Added a Form History tab to QA forms with version comparison and per-question score trends.
- Web app: Added sorting to the integrations connections list.
- Web app: Added static rendering for native dashboard workspaces, with alerts and subscriptions available for them.
- Web app: Inbox alert details now show the alert condition, and the header's backlog count is labelled correctly.
- Web app: Fixed users being signed out unexpectedly.
- Web app: Error messages no longer show raw server error text.
- Web app: Fixed dashboard view, workspace and query settings that could be dropped when saving.
- Web app: Fixed several navigation and display issues, including dashboard breadcrumbs, settings links, empty filter results and retrying analytics errors.

## 2026-08-11
- Fixed duplicate signal results for the same interaction.

## 2026-08-10
- Fixed clearing a dashboard's saved default view settings.
- Improved reliability of call transcription.

## 2026-08-09
- Improved handling of very long transcripts.

## 2026-08-07
- Added ingestion of HubSpot call recordings.
- Improved speed of NICE CXone recording retrieval.
- Fixed evaluation counts shown for QA form versions.

## 2026-08-06
- Maintenance and reliability improvements.

## 2026-08-05
- Added scheduled delivery of dashboard subscriptions for native dashboards.
- Added alerts for native dashboards.
- Added cross-query cascading filters on dashboards.
- Added secure embedding for native dashboards.
- Added acknowledgement of notifications from Slack and email.
- Added status grouping and filtering to the inbox.
- Added QA form version comparison and per-question score trends.
- Added reasoning to interaction alerts.
- Added optional filtering of NICE CXone interactions with no agent or no talk time.
- Improved speed and reliability of NICE CXone recording retrieval.

## 2026-08-04
- Web app: Redesigned the inbox queue into separate, collapsible sections by status.
- Web app: Added a pivot table visualization to native dashboards.
- Web app: Added a guardrail for cascading filters that span queries.
- Web app: Transcript channel badges now show a distinct icon for each channel.

## 2026-08-03
- Added an MCP server so customers can connect AI assistants such as Claude Desktop to design and manage QA forms, signals and dashboards.
- The agents API now returns only active agents by default, with an option to include inactive ones.

## 2026-08-02
- Maintenance and reliability improvements.

## 2026-07-30
- Improved the detail shown on inbox alerts.
- API keys now have a maximum lifetime of one year.
- Fixed an error when updating a notification channel.
- NICE CXone ingestion can now take in all skills without listing each one, and fetches completed contacts more reliably.

## v4.35.2 — 2026-07-28
- Fixed a reliability issue in NICE CXone interaction ingestion where recently completed
  interactions could be silently skipped; ingestion now tolerates delayed update timestamps.

## v4.34.3 — 2026-07-27
- QA evaluation workflows can now fan out across all production QA forms.

## v4.33.6 — 2026-07-27
- Process-management and CRM integrations generalized into a source-neutral model,
  enabling additional CRM/case-management providers.

## v4.32.1 — 2026-07-24
- NICE CXone ingestion supports allow/deny filtering by skill.

## v4.31.1 — 2026-07-24
- Fixed mapping of individual NICE CXone contact lookups into the interaction store.

## v4.30.10 — 2026-07-24
- Faster transcript interaction search (query consolidation).

## v4.29.4 — 2026-07-23
- Faster QA evaluation list loading.
- Bulk ingestion pipeline for Connect rubric signals.
- Transcript support for asynchronous conversation channels (accreting transcripts).

## v4.28.1 — 2026-07-23
- Fixed case lookups in Connect enrichment to key on the source interaction.
