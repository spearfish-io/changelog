# Spearfish Platform Changelog

Release notes for the Spearfish platform. Entries are summarized at the product level;
internal details are omitted.

## 2026-09-17
- Maintenance and reliability improvements.

## 2026-09-16
- Strengthened access controls for user role management.

## 2026-09-15
- Web app: Added drill-through and record links on dashboard tables, KPIs and gauges.
- Web app: Dashboard tables now respect each column's heading, visibility, number format and order, and KPIs and gauges show suffixes such as "%".
- Web app: Fixed gauge colour bands wider than half the scale not showing, and gauge readings being cut off on short cards.
- Web app: Fixed the drill-through banner incorrectly reporting whether a page was filtered.

## 2026-09-12
- Fixed report breakdowns for signals whose values come from a reference list, such as region, which showed every value as "(unmapped)".

## 2026-09-11
- Fixed QA evidence highlights that pointed to the wrong place in the transcript; evidence now lines up with the quoted turn.

## 2026-09-07
- Maintenance and reliability improvements.

## 2026-09-06
- Fixed dashboard cards with date filters that could fail to load.
- Web app: Added multi-value dashboard filters.
- Web app: Added per-card filter wiring, so a query used on several dashboards can be filtered differently on each.
- Web app: Removing a filter binding now first lists the other views, including archived ones, that it will change.
- Web app: Saving a dashboard now sends only what changed, so edits made elsewhere are no longer overwritten.
- Web app: Added restoring archived dashboard views, and duplicating a view no longer clashes with an archived view's name.
- Web app: Dashboards now honour explicit card placement, and authors can set it.
- Web app: Improved filtered dashboard loading: cards load together and no longer briefly show unfiltered data.
- Web app: The dashboard editor now keeps the selected card when cards are reordered, removed or duplicated.
- Web app: Widened the Edit query dialog.
- Web app: Inbox stage review items are now labelled "Outcome review".

## 2026-09-04
- Added speaker turns and timings to the transcript used for QA evaluation, so timing questions on QA forms can now be scored.
- Multi-select dashboard filters now match any of the selected values, and multi-value date filters return a clear validation error.
- Fixed single sign-on to analytics dashboards when starting from the dashboard login page.

## 2026-08-31
- Fixed QA evaluations sometimes leaving questions unanswered as "insufficient evidence".
- Fixed QA evaluations being scored against an unpublished draft form instead of the published version.
- Web app: Fixed the Inbox failing to load when it contained item types it did not recognise.
- Web app: Fixed "not found" pages taking up to 30 seconds to appear.
- Web app: Fixed copied Inbox item links not opening the item.

## 2026-08-29
- Improved identification of agent and customer speakers in call transcripts, including single-channel recordings.

## 2026-08-28
- Fixed HubSpot form submissions not being linked to the customer who submitted them.

## 2026-08-27
- Web app: Simplified signal authoring: the question is tied to the model instruction, the description is an optional label with no length limit, and the form is regrouped so the LLM/Query toggle changes one section.
- Web app: Fixed clicking the default-sorted column header on lists doing nothing.

## 2026-08-26
- Maintenance and reliability improvements.

## 2026-08-25
- Fixed CallRail call times being shifted because the call's time-zone offset was ignored.
- Web app: Refreshed the app's look with new brand colours and typography, a sidebar reorganised into four groups, consistent page layouts and accessible labels on icon-only buttons.
- Web app: Integrations is now an expandable sidebar section with Connections, Workflow Actions, Triggers and Webhooks.
- Web app: Redesigned signal authoring with an LLM/Query toggle, a table picker, version history with revision comparison, and clearer empty and loading states.
- Web app: Transcript timeline annotations (sentiment, topic, intent, entity) now show as chips on the speaker turn, and the expand controls work from the keyboard.
- Web app: Fixed saving signal definitions that had no name, and removed a spurious error message in the signal editor.
- Web app: Fixed pages showing a misleading "not found" or loading forever when the real problem was an access or server error.
- Web app: The app now follows operating-system light and dark mode changes live.
- Web app: Fixed the sidebar highlighting the wrong item after back or forward navigation.

## 2026-08-20
- Maintenance and reliability improvements.

## 2026-08-19
- Fixed the Inbox merging several alerts about the same record into one item.
- Fixed QA questions set to disallow "insufficient evidence" still receiving that answer.

## 2026-08-18
- Fixed saving a dashboard workspace clearing its description when the description was not included in the update.
- Improved NICE CXone syncs so reporting requests that time out are retried instead of skipping data.
- Fixed HubSpot call recordings not being downloaded.
- Added sorting by name and created date to the Connections list, and fixed its status filter returning incomplete pages and wrong totals.
- Web app: Added a Form History tab for QA forms, with version-to-version comparison and a per-question score trend chart.
- Web app: Inbox item details now show the alert condition's plain-language description.
- Web app: Fixed cases where saving a dashboard view, query, workspace or default-view setting could silently discard settings.
- Web app: Fixed column sorting on the Connections list.
- Web app: Fixed being signed out of the whole app when a single area failed to load.
- Web app: Added a Retry button when Analytics fails to load.
- Web app: Fixed the Jobs and Batches links in Settings.
- Web app: Fixed an error on connection details for connections with no provider.
- Web app: Added an empty state to the Flows filter when there are no flows.
- Web app: Fixed dashboard breadcrumbs showing an internal key instead of the view title.
- Web app: Fixed the Inbox header's count label so it matches the badge.
- Web app: Improved error messages so unexpected server errors show a clear, generic message.

## 2026-08-11
- Maintenance and reliability improvements.

## 2026-08-10
- Fixed the interactions list API sometimes ignoring the requested sort direction; invalid values now return an error.
- Fixed an error when removing a saved default dashboard view.

## 2026-08-09
- Maintenance and reliability improvements.

## 2026-08-07
- Added HubSpot call recordings: calls are imported and their recordings downloaded and transcribed.
- Fixed QA form versions always showing zero evaluations.
- Improved NICE CXone recording retrieval: missing recordings are detected in seconds and downloads are much faster.

## 2026-08-06
- Maintenance and reliability improvements.

## 2026-08-05
- Improved the speed and reliability of NICE CXone recording downloads, so recordings and QA evaluations keep up with call volume.
- Fixed non-English transcripts that could wait a long time for translation.
- Added a field-level comparison between any two versions of a QA form, showing scoring changes separately from wording-only changes.
- Added per-question QA score trends across form versions, including sample counts.
- Removed an always-empty field from QA evaluation API responses.

## 2026-08-04
- Web app: Added a pivot table chart type to dashboards.
- Web app: Redesigned the Reviews Inbox queue into separate, collapsible Open, In progress and Closed sections, each with its own paging.
- Web app: Added a warning in the dashboard view editor when a dependent filter's parent is wired to a different query.
- Web app: Fixed transcript channel badges always showing a phone icon; each channel now has its own icon.

## 2026-08-03
- The agents list now shows only active agents by default, with an option to include inactive ones.

## 2026-08-02
- Maintenance and reliability improvements.

## 2026-07-30
- API keys now expire after at most one year, and new keys default to a one-year expiry.
- Fixed an error that stopped changes to a notification channel from being saved.
- Fixed NICE CXone completed-contact syncs missing new contacts.

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
