# Spearfish Platform Changelog

Release notes for the Spearfish platform. Entries are summarized at the product level;
internal details are omitted.

## 2026-09-17
- Added editing of dashboard queries through the Spearfish MCP connector.

## 2026-09-16
- Strengthened access controls for user role management.

## 2026-09-15
- Web app: Added drill-through and links on dashboard tables, KPIs and gauges.
- Web app: Added column labels, hidden columns, number formats and column ordering to dashboard tables, and suffixes to KPIs and gauges.
- Web app: Fixed gauge colour bands not showing and gauge readings being cut off on small cards.
- Web app: Fixed the drill-through banner so it shows only the filters actually applied to the page.

## 2026-09-12
- Added the ability for the Spearfish MCP connector to look up descriptions of available reporting data and create dashboard queries.
- Fixed signal values from reference datasets showing as "(unmapped)" in signal reports.

## 2026-09-11
- Fixed QA evidence timestamps so highlighted evidence points to the right moment in the transcript.
- Strengthened access controls over the data that dashboard queries can use.

## 2026-09-07
- Maintenance and reliability improvements.

## 2026-09-06
- Added per-question QA form analytics to the Spearfish MCP connector, including why answers went unscored.
- Fixed an error when creating or archiving signal definitions.
- Web app: Added multi-select filters to dashboards.
- Web app: Improved dashboard loading so filtered cards load together and no longer briefly show unfiltered data.
- Web app: Dashboards now respect explicit card positions in page layouts.
- Web app: Renamed "Stage review" Inbox items to "Outcome review".

## 2026-09-04
- Added multi-value dashboard filters and improved dashboard editing through the Spearfish MCP connector.
- Improved AI QA evaluations with speaker- and time-stamped transcripts, so timing-based questions can be scored.
- Added support for capturing additional CallRail call fields.
- Fixed Analytics single sign-on failing when started from the Analytics login page.

## 2026-08-31
- Improved QA evaluations so every question in a form section receives an answer.
- Fixed QA evaluations to always score against the published form version, never an unpublished draft.
- Improved reliability of call recording sync and transcription so deferred calls are no longer skipped.
- Web app: Fixed "not found" pages taking a long time to appear.
- Web app: Fixed copied Inbox item links not opening the item.
- Web app: Fixed the Inbox failing to load when it contained certain item types.

## 2026-08-29
- Improved reliability of reviewer override decisions in the Reviews Inbox so every decision is recorded and applied.
- Improved identification of agent and customer speakers in call transcripts.

## 2026-08-28
- Fixed HubSpot form submissions not being linked to the customer who submitted them.

## 2026-08-27
- Fixed an issue that could stop some SQL-based signals from running.
- Improved reliability of call recording sync and transcription so calls missed by one run are picked up by later runs.
- Fixed signals and QA occasionally skipping calls whose transcripts arrived late.
- Improved matching of the same customer across connected sources, such as phone and email records.
- Web app: Simplified the signal authoring form with clearer grouping, a dedicated question field and no description length limit.
- Web app: Fixed sorting by the default-sorted column in lists.

## 2026-08-26
- Maintenance and reliability improvements.

## 2026-08-25
- Fixed CallRail call and text times appearing several hours off.
- Strengthened access controls across the platform API.
- Improved the guidance the Spearfish MCP connector gives AI assistants for dashboards, QA forms and signals.
- Web app: Refreshed the app's look with updated typography, colours, navigation sidebar and page layouts, plus accessibility improvements.
- Web app: Improved error states on pages that fail to load, replacing misleading "not found" messages and endless spinners.
- Web app: Redesigned signal authoring with an LLM/Query mode toggle, table picker, version history with revision comparison and clearer empty states.
- Web app: Fixed an issue that prevented existing signal definitions from being saved.
- Web app: Removed a spurious error notification when authoring signals.
- Web app: Added Signals administration for tiers, vocabularies, subjects and personas.
- Web app: Transcript timelines now show sentiment, topic, intent and entity annotations on the relevant speaker turn.
- Web app: Integrations pages now appear as sub-items in the sidebar.
- Web app: Added a Feedback detail view with status filters, actions and links to the related record.
- Web app: Feedback submitted from QA evaluations now captures intent and structured corrections.
- Web app: Fixed the theme not fully updating when the system switches between light and dark mode.
- Web app: Fixed the sidebar highlighting the wrong item after back/forward navigation.

## 2026-08-20
- Fixed blank agent and customer names on HubSpot interactions.

## 2026-08-19
- Fixed the inbox showing only one finding when an interaction triggered several alerts.
- Fixed QA questions that disallow "insufficient evidence" still returning that answer.

## 2026-08-18
- Fixed sign-in for the Spearfish MCP connector in AI assistants such as Claude.
- Added a Claude Code plugin so customers can install the Spearfish connector in a few commands.
- Improved reliability of NICE CXone data imports when NICE responds slowly.
- Fixed an issue that could delay processing of newly imported interactions.
- Added sorting to the Connections list and fixed status filtering returning incomplete pages.
- Improved validation and error handling across dashboards, views, queries, alerts, subscriptions and workspace imports.
- Fixed HubSpot call recordings not downloading and agent names missing on HubSpot interactions.
- Strengthened safeguards on custom SQL used in signals and dashboards.
- Web app: Added a Form History tab to QA forms with version-to-version comparison and per-question score trends.
- Web app: Clarified the Reviews Inbox header count to show open plus in-progress items.
- Web app: Inbox alert details now show a plain-language description of the alert condition.
- Web app: Enabled alerts and subscriptions management for built-in dashboards.
- Web app: Fixed sorting on the Integrations Connections list.
- Web app: Fixed users being signed out unexpectedly when a single page failed to load data.
- Web app: Added a Retry button when Analytics fails to load.
- Web app: Fixed the Jobs and Batches links in Settings.
- Web app: Fixed an error message on connection details for connections with no provider.
- Web app: Added an empty state to the Flows picker when no flows are available.
- Web app: Fixed dashboard breadcrumbs showing an internal key instead of the dashboard title.
- Web app: Improved error messages so unexpected server errors show a friendly message.

## 2026-08-11
- Fixed signal reports double-counting re-processed interactions.

## 2026-08-10
- Fixed resetting saved dashboard view defaults.

## 2026-08-09
- Maintenance and reliability improvements.

## 2026-08-07
- Added import and transcription of HubSpot call recordings.
- Fixed QA form versions showing zero evaluations.
- Improved NICE CXone call-recording download speed and completeness.

## 2026-08-06
- Maintenance and reliability improvements.

## 2026-08-05
- Added multi-value filters and status sections to the notifications inbox.
- Improved reliability of analytics processing and fixed cases where aggregated reports could be incomplete.
- Improved the speed and reliability of NICE CXone call-recording retrieval.
- Added optional plain-language reasoning to signal-based alerts.
- Improved reliability of interaction processing.

## 2026-08-04
- Web app: Fixed Transcripts channel badges so each channel (voice, chat, SMS, email and others) shows its own icon.
- Web app: Redesigned the Reviews Inbox queue into separate Open, In progress and Closed sections, each paginated and collapsible.
- Web app: Added a pivot table visualization to dashboards.

## 2026-08-03
- Agent lists now show active agents by default, with an option to include inactive agents.

## 2026-08-02
- Maintenance and reliability improvements.

## 2026-07-30
- Strengthened API key security: keys now expire after at most one year.
- Improved inbox alerts with clearer titles, descriptions and supporting transcript quotes.
- Fixed saving changes to notification channels.
- Fixed NICE CXone completed-contact sync missing new contacts on scheduled runs.

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
