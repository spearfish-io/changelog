# Spearfish Platform Changelog

Release notes for the Spearfish platform. Entries are summarized at the product level;
internal details are omitted.

## 2026-09-17
- Maintenance and reliability improvements.

## 2026-09-16
- Strengthened access controls for role assignments.
- Web app: Fixed removing a user's role for users who belong to more than one organization.
- Web app: Strengthened permission checks on user role changes.

## 2026-09-15
- Web app: Added click-through from dashboard tables, KPIs and gauges to detail pages and linked records.
- Web app: Improved dashboard tables, KPIs and gauges so column headers, hidden columns, number formats, units and column order carry over.
- Web app: Fixed gauges missing their colour bands or being cut off on small cards.
- Web app: Fixed the drill-through banner sometimes misreporting which filters were applied.

## 2026-09-12
- Fixed dashboard tiles showing unfiltered, empty or failing results when using filter defaults, optional filters, variables or column names shared by more than one table.
- Fixed signal value reports grouping every value as "(unmapped)" for signals backed by a reference list.

## 2026-09-11
- Fixed QA evidence quotes pointing to the wrong moment in the conversation.
- Fixed dashboard filters that could not apply to a column the tile does not display.

## 2026-09-07
- Maintenance and reliability improvements.

## 2026-09-06
- Fixed remaining errors on dashboard cards when filters were applied.
- Fixed an error that stopped signal definitions from being created or archived.
- Web app: Added dashboard filters that accept more than one value.
- Web app: Added per-card filter wiring, so the same query can be filtered differently on different dashboards.
- Web app: Added restoring archived dashboard views, and made duplicating a view more reliable.
- Web app: Added support for explicit card placement in dashboard layouts.
- Web app: Improved dashboard loading so cards no longer briefly show unfiltered data and load in a single request.
- Web app: Improved dashboard editing so saving no longer overwrites changes made elsewhere, selection is kept when reordering, and removing a filter binding first lists the other views it affects.
- Web app: Improved the Edit query dialog, which is now sized to fit long queries.
- Web app: Renamed the Inbox "Stage review" label to "Outcome review".

## 2026-09-04
- Added multi-select dashboard filters, so one filter can match several values at once.
- Added restoring deleted dashboards and copying dashboards.
- Added a warning when you edit a query that other dashboards also use.
- Improved automated QA evaluations, which now read timestamped, speaker-labelled transcripts so timing questions can be scored.
- Fixed dashboard cards that failed when a date filter was applied.
- Fixed publishing and unpublishing dashboards, which could fail with an error.
- Fixed analytics single sign-on failing when started from the analytics sign-in page.

## 2026-08-31
- Fixed QA evaluations sometimes scoring against an unpublished draft of a form instead of the published version.
- Fixed QA evaluations sometimes leaving questions in a form section unanswered.
- Improved recording sync and transcription so delayed or throttled calls are no longer skipped.
- Web app: Fixed "not found" pages taking about 30 seconds to appear.
- Web app: Fixed copied Inbox item links not opening the item.
- Web app: Fixed the Inbox failing to load when it held new item types.

## 2026-08-29
- Improved telling the agent apart from the customer in call transcripts, for both stereo and single-channel recordings.
- Fixed reviewer corrections in the Reviews inbox that could fail to apply while showing as done; corrections are now confirmed before an item is marked actioned.
- Improved NICE CXone recording downloads so temporary failures are retried instead of skipped.

## 2026-08-28
- Maintenance and reliability improvements.

## 2026-08-27
- Fixed some SQL-based signals that failed to compute.
- Improved nightly processing so provider rate limiting or a temporary outage at a connected data source no longer stops the rest of the day's processing.
- Fixed calls that could be left untranscribed after a missed nightly run.
- Fixed calls that were transcribed late being skipped for signal extraction and QA scoring.
- Improved matching of the same customer across phone and email records from different sources, including their lifecycle stage history.
- Web app: Improved the Signals editor, which now keeps the question asked separate from the description, changes only one section when switching between AI and query mode, and accepts long descriptions.

## 2026-08-26
- Improved call transcription so a missing recording or a high-volume day no longer stops the rest of the day's calls from being processed.

## 2026-08-25
- Strengthened enforcement of role permissions across the platform.
- Fixed CallRail call and SMS times being off by several hours.
- Fixed occasional duplicate inbox items.
- Web app: Improved the look and feel of the whole app with a refreshed design, new typography and reorganized navigation, with Integrations now a sub-menu in the sidebar.
- Web app: Improved Signals authoring with a simpler editor, a picker for data tables, version history with change comparison, and clearer states when no data exists yet.
- Web app: Added organization-level Signals settings for tiers, vocabularies, subjects and personas.
- Web app: Fixed signal definitions failing to save with "Name is required".
- Web app: Fixed a stray error notice on Signals pages.
- Web app: Added a fuller Feedback list where you can open an item, act on it, filter by status and jump to the record it is about; feedback from evaluations now records whether it is praise, a correction or a comment.
- Web app: Improved transcript timelines so sentiment, topic, intent and entity notes appear as tags on the relevant turn.
- Web app: Fixed the app not following a light/dark mode change in the operating system while open.
- Web app: Fixed the sidebar sometimes highlighting the wrong page after back/forward navigation.
- Web app: Strengthened protection of account sessions.

## 2026-08-20
- Added protection against two people's edits to the same signal definition silently overwriting each other.

## 2026-08-19
- Fixed the inbox dropping additional findings raised on the same interaction.
- Fixed QA questions set to disallow "insufficient evidence" answers still receiving them.
- Improved role management so permissions for every platform feature can be granted.
- Improved nightly processing so one stalled interaction no longer holds up the rest.
- Fixed signals being listed only by their ID instead of their name.

## 2026-08-18
- Fixed NICE CXone daily imports failing when NICE responded slowly; those requests are now retried.
- Added sorting by name and created date to the Connections list, and fixed status filters returning incomplete pages.
- Fixed saving a dashboard workspace without a description clearing its existing description.
- Fixed invalid dashboard requests and workspace imports returning server errors instead of clear validation errors.
- Fixed dismissed inbox items reappearing when the same finding was raised again.
- Improved reliability of automated QA evaluation during temporary AI provider errors.
- Strengthened data isolation for custom SQL-based signals.
- Web app: Added a Form History tab for QA forms that compares any two versions of a form and charts each question's score over time.
- Web app: Added alerts and subscriptions management for dashboard workspaces.
- Web app: Improved alert items in the Inbox, whose detail view now shows the alert condition's plain-language description.
- Web app: Fixed the Inbox header count so its "open + in progress" label matches what it counts.
- Web app: Fixed dashboard edits that could quietly reset settings such as filter wiring, link and drill-through behaviour, render mode or workspace status.
- Web app: Fixed the default-dashboard form keeping old values after its scope was changed.
- Web app: Fixed sorting on the Integrations Connections list.
- Web app: Fixed users sometimes being signed out of the whole app when a single area failed to load; pages now show a proper error instead.
- Web app: Added a Retry button when Analytics fails to load.
- Web app: Fixed the Jobs and Batches links in Settings leading to a "not found" page.
- Web app: Fixed dashboard breadcrumbs showing internal keys instead of readable titles.
- Web app: Fixed a misleading error message on connection details when no provider is set up.
- Web app: Added an empty state when the Flows catalog has nothing to show.
- Web app: Improved permission handling in dashboard admin, which now shows a clear message to users without access instead of an error.
- Web app: Improved error messages so unexpected server errors show a clear, generic message.

## 2026-08-11
- Maintenance and reliability improvements.

## 2026-08-10
- Fixed sort direction handling in the transcripts API, which now accepts "ascending" and "descending" and rejects invalid values.
- Fixed some interactions being skipped for QA evaluation and signal extraction.
- Fixed removing saved default dashboard views.

## 2026-08-09
- Maintenance and reliability improvements.

## 2026-08-07
- Fixed QA form versions always showing zero evaluations.
- Fixed NICE CXone recording imports stalling on contacts that have no recording.

## 2026-08-06
- Maintenance and reliability improvements.

## 2026-08-05
- Improved the speed and reliability of call recording imports from NICE CXone.
- Added side-by-side comparison of any two versions of a QA form, separating scoring changes from wording-only changes.
- Added per-question score trends across QA form versions.
- Added the option for signals to include a plain-language explanation of their result in interaction alerts.
- Fixed daily reporting totals that could be incomplete when the same day was processed more than once.
- Fixed an issue that could delay newly imported interactions from appearing.

## 2026-08-04
- Web app: Added a distinct icon for each conversation channel (voice, SMS, chat, email, form and more) on the transcript list and transcript details.
- Web app: Improved the Reviews Inbox, which is now split into separately paged, collapsible Open, In progress and Closed sections.
- Web app: Added a pivot table chart type to dashboards.
- Web app: Added a warning in the dashboard view editor when a dependent filter won't be narrowed by its parent filter.

## 2026-08-03
- Fixed some NICE CXone call recordings not importing after a temporary interruption.
- Changed the agents list to show only active agents by default, with an option to include inactive agents.

## 2026-08-02
- Maintenance and reliability improvements.

## 2026-07-30
- Added the option for signals to attach supporting transcript quotes to interaction alerts, with custom alert titles and descriptions.
- Fixed editing and turning notification channels on and off.
- Fixed scheduled NICE CXone imports not picking up newly completed contacts.

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
