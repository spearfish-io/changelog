# Spearfish Platform Changelog

Release notes for the Spearfish platform. Entries are summarized at the product level;
internal details are omitted.

## 2026-10-25
- Maintenance and reliability improvements.

## 2026-10-24
- Maintenance and reliability improvements.

## 2026-10-23
- Fixed requests sometimes being refused as too frequent when several users signed in from the same network.
- Strengthened security of platform services.

## 2026-10-20
- Fixed completed contacts from the NICE CXone integration not being processed.
- Strengthened security of account sign-in and platform services.

## 2026-10-19
- Added Workflows: build automation workflows in a visual designer, save drafts, check and publish versions, revert to earlier versions, and start runs with their own inputs.
- Added a run viewer for workflows, with each run's step-by-step history and progress for repeating steps.
- Improved workflow run reliability: interrupted or waiting steps now resume correctly, and runs no longer report success before every step has finished.
- Added tools to the Spearfish connector for AI assistants for managing account users and roles and creating dashboard workspaces, and gave the connector a clearer display name.
- Added a filter for interactions with or without a transcript.
- Added support for importing interactions from bulk text-file exports made by other systems.
- Added a QA option to score every leg of a multi-leg call, such as a virtual agent handing over to a person, as one conversation.
- Fixed manual QA evaluations hiding the AI evaluation of the same call, and evaluation details showing only one question for some forms.
- Fixed QA evaluations that rely on signals sometimes being scored before those signals were available.
- Added date ranges and per-signal totals to signal metrics.
- Fixed new signals being shown as overrides of a global signal, signal versions always showing 1, and changes to global signals being slow to reach every account.
- Improved signal extraction speed on large batches and fixed interactions occasionally being missed under load.
- Fixed sign-out failing for some applications.
- Fixed some connected applications getting stuck on the consent screen during sign-in.
- Strengthened protection of account sign-in, sessions and access permissions.
- Web app: Fixed users with workflow trigger or webhook permissions being unable to open the Triggers and Webhooks screens.
- Web app: Added Capture evidence and Capture reasoning options to the signal editor.
- Web app: Fixed columns on the Signals list appearing empty because they sat off-screen.
- Web app: Improved Transcripts to open on the newest interactions, with the "Has transcript" filter on by default.
- Web app: Improved Evaluations to open on the newest evaluations.
- Web app: Improved evaluation evidence so quotes link to the right point in the conversation, showing "No start time" when none is known.
- Web app: Fixed switching between accounts sometimes returning you to the account you started on.
- Web app: Fixed account management actions being shown to users who are not permitted to use them.
- Web app: Improved the data deletion audit log, which is now downloaded as a file.
- Web app: Fixed transcript details showing a quality assessment loading error; scores remain in the Evaluations section.
- Web app: Fixed archived dashboard views appearing clickable in the views list.

## 2026-09-17
- Maintenance and reliability improvements.

## 2026-09-16
- Strengthened access controls for user role management.

## 2026-09-15
- Web app: Added drill-through and clickable links to dashboard tables, KPI tiles and gauges.
- Web app: Added dashboard table column settings (labels, hidden columns, number formats and column order) and suffixes such as % for KPIs and gauges.
- Web app: Fixed gauges with wide colour bands, and gauges on short cards, displaying incorrectly.
- Web app: Fixed drill-through banners so they say accurately whether the destination page applied the filter.

## 2026-09-12
- Fixed signal values from reference lists showing as "(unmapped)" in reports instead of their labels.

## 2026-09-11
- Fixed evidence quotes in QA evaluations so they point to the right moment in the call transcript.
- Web app: Added an audit log of completed data purges and deletions to the Data Retention & Deletion section.

## 2026-09-07
- Fixed an issue where some CallRail call and text records could be missing after data was refreshed.

## 2026-09-06
- Fixed an issue where some dashboards with filters could fail to load.
- Fixed an issue where creating or archiving a signal definition could fail.
- Web app: Added multi-select filters to dashboard views that match any of the selected values.
- Web app: Added per-card filter connections, so the same query can be filtered differently on different dashboards.
- Web app: Added a warning that lists every other dashboard view affected before you remove a shared filter connection.
- Web app: Added restoring archived dashboard views, and duplicated views now always get a unique name.
- Web app: Added support for exact card positions on dashboard pages, including layouts with gaps.
- Web app: Fixed saving a dashboard undoing changes made elsewhere, such as a rename in another tab, and editing a query removing its filter connections.
- Web app: Improved dashboard loading so filtered cards no longer briefly show unfiltered data.
- Web app: Improved the dashboard editor so the selected card stays selected when cards are reordered, removed or duplicated.
- Web app: Improved the Edit query dialog to use more of the screen.
- Web app: Added a Data Retention & Deletion section to account details, where admins can set how long data is kept and request full deletion of the account's data.
- Web app: Improved the Inbox label for stage review items, which now read "Outcome review".

## 2026-09-04
- Added a warning when editing a query that other dashboards also use.
- Fixed date filters and some dashboard actions failing on certain dashboards.
- Fixed single sign-on into Metabase failing when started from the Metabase login page.
- Improved QA evaluations so questions about timing, such as greeting speed and long silences, can now be answered.

## 2026-08-31
- Fixed QA evaluations sometimes leaving most questions in a form section unanswered.
- Fixed QA evaluations sometimes being scored against an unpublished draft of a form instead of the published version.
- Improved reliability of recording imports from NICE CXone.
- Web app: Fixed "not found" pages taking around 30 seconds to appear.
- Web app: Fixed copied links to Inbox items not opening the item.
- Web app: Fixed the Inbox failing to load when it contained item types it did not recognise.
- Web app: Added stage review items to the Inbox, with their own filter.

## 2026-08-29
- Improved identification of which speaker is the agent and which is the customer in call transcripts, so QA questions that depend on who spoke can now be scored.

## 2026-08-28
- Fixed HubSpot form submissions not being linked to the matching customer.

## 2026-08-27
- Improved matching of the same customer across connected sources that share a phone number or email, and used that unified identity in customer lifecycle tracking.
- Web app: Improved the Signals authoring form: related settings are grouped together, the question to ask is kept separate from the description, and long descriptions no longer block editing.

## 2026-08-26
- Improved signal definitions with a separate AI instruction field, so editing a signal's description no longer changes how the signal is evaluated.

## 2026-08-25
- Fixed CallRail call and SMS times being off by several hours.
- Strengthened access controls and error handling across the platform.
- Web app: Improved the look and feel of the web app with a refreshed visual design, new typography, polished dialogs and tables, and a reorganised sidebar.
- Web app: Improved accessibility by adding labels to icon-only buttons.
- Web app: Improved Integrations navigation so Connections, Workflow Actions, Triggers and Webhooks appear as sub-items in the sidebar.
- Web app: Improved Signals authoring with a simpler editor, a choice between AI-answered and query-based signals, and version history with revision comparison.
- Web app: Fixed saving changes to existing signal definitions, and removed an unnecessary error message on the Signals page.
- Web app: Added Signal Config administration for managing tiers, vocabularies, subjects and personas.
- Web app: Added a detail view to the Feedback list, where reviewers can open an item, act on it, jump to the record it is about and filter by status.
- Web app: Improved QA feedback submission to record the kind of feedback and any structured corrections.
- Web app: Improved the transcript timeline so sentiment, topic, intent and entity annotations appear as tags on the conversation turn they belong to.
- Web app: Fixed misleading "not found" messages when a page failed to load for another reason.
- Web app: Fixed the app not following a light/dark mode change in your operating system until the page was reloaded.
- Web app: Fixed the sidebar sometimes highlighting the wrong item after using browser back/forward.
- Web app: Strengthened protection of sign-in credentials and account sessions.

## 2026-08-20
- Fixed HubSpot calls showing blank agent and customer names.

## 2026-08-19
- Fixed the inbox showing only one finding when a single call had several.
- Fixed QA questions returning "insufficient evidence" when the form did not allow that answer.

## 2026-08-18
- Added a Claude Code plugin that sets up the Spearfish connector and its guides in a few commands.
- Fixed sign-in for the Spearfish connector in AI assistants such as Claude, so the login and consent steps now complete.
- Fixed HubSpot call recordings not downloading.
- Improved HubSpot imports so calls and activities fall in the right date range, link to the right contacts, and show agent names.
- Improved the reliability of NICE CXone data imports when NICE responds slowly.
- Added sorting by name and created date to the Connections list.
- Fixed filtering connections by status returning incomplete pages and wrong totals.
- Fixed updating a dashboard workspace clearing its description or theme when those fields were left out.
- Improved error handling and validation for dashboard date filters, saved queries and workspace imports.
- Web app: Added a Form History tab to QA forms that compares any two versions of a form and charts each question's score over time.
- Web app: Improved Inbox alert details to show a plain-language description of the alert condition.
- Web app: Improved the Inbox header so its backlog count is clearly labelled as open plus in progress.
- Web app: Fixed column sorting on the Integrations Connections list.
- Web app: Fixed users being signed out of the whole app when a single page failed to authorize.
- Web app: Improved error messages so unexpected server errors show a clear, generic message, including during password reset.
- Web app: Added a Retry button when Analytics fails to load.
- Web app: Fixed the Jobs and Batches links in Settings, which led to a missing page.
- Web app: Fixed Dashboards breadcrumbs showing an internal key instead of the view's name.
- Web app: Fixed an unnecessary error message on some connection detail pages.
- Web app: Fixed the Flows picker in workflow actions showing a blank tab instead of a "No flows available" message.

## 2026-08-11
- Maintenance and reliability improvements.

## 2026-08-10
- Fixed removing a default dashboard assignment in dashboard workspace settings.
- Improved the reliability of call transcription when processing large volumes of recordings.

## 2026-08-09
- Maintenance and reliability improvements.

## 2026-08-07
- Added importing and transcription of HubSpot call recordings.
- Improved the speed and reliability of importing call recordings from NICE CXone.
- Fixed QA form versions always showing an evaluation count of zero.

## 2026-08-06
- Maintenance and reliability improvements.

## 2026-08-05
- Improved the Inbox with Open, Working and Closed sections, each with its own pages, and filters that accept several values at once.
- Fixed dashboard filters that depend on another filter so their options narrow correctly when the two filters are on different charts.
- Added an option for signals to include a short plain-language explanation, shown on interaction alerts.
- Improved the speed and reliability of call recording imports from NICE CXone.
- Fixed delays in processing newly imported interaction data.

## 2026-08-04
- Web app: Fixed the Channel badge on transcripts so each channel (voice, chat, email, SMS and so on) shows its own icon.

## 2026-08-03
- Changed the agents list to show only active agents by default, with an option to include inactive agents.

## 2026-08-02
- Maintenance and reliability improvements.

## 2026-07-30
- Strengthened API key security: new API keys now expire after at most one year.
- Added optional supporting transcript quotes to interaction alerts, along with clearer alert titles and descriptions.
- Fixed importing of completed contacts from NICE CXone so new contacts are picked up reliably.

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
