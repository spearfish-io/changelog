# Spearfish Platform Changelog

Release notes for the Spearfish platform. Entries are summarized at the product level;
internal details are omitted.

## 2026-11-23
- Added conditions on signal values to QA steps, so a step evaluates only the interactions whose latest values match, for example only enrollment calls; a malformed condition is now refused when the workflow is published.
- Improved export bindings so worksheet lines can be matched by a reference set's mapping across several columns; lines whose match is missing or ambiguous are skipped and counted, never guessed.
- Added "some" and "every" expressions to decision documents, and fixed several edge cases in how their expressions compare lists and read dates and large numbers.
- Fixed decision documents that match or attribute records failing when run from a workflow step.
- Web app: Added History previews to dashboards: pick a past version to see it on the dashboard, then go back or restore it, keeping the current version in History.
- Web app: Added one card editor for a dashboard card's query and its chart, with a Query tab to edit and run the SQL, New query from Add card, and Save as a new query when other views use the same query.
- Web app: Added Create alert to a dashboard card's menu and Set as default to a view's menu.
- Web app: Added Undo for 10 seconds after removing a card or deleting a page in dashboard edit mode.
- Web app: Changed dashboard edit mode to move cards by dragging and resize them from their edges or with the arrow keys, with other cards making way.
- Web app: Changed dashboard card heights to finer steps; existing dashboards keep their exact layout.
- Web app: Changed dashboard charts, numbers, gauges, funnels and tables to fit their card's size, shortening or hiding what does not fit with the full text on hover, and set a minimum size for each chart type; Legend, Label angle and Data labels now offer Auto, and charts whose label angle was saved as Level now use Auto.
- Web app: Changed dashboard charts to leave out zero values by default, with a Show zero values switch in the card editor.
- Web app: Fixed number values, card titles, axis titles, pie labels and bar value labels overlapping or running outside their card.
- Web app: Removed the separate dashboards admin area; views, queries, workspace settings and default dashboards are managed on the dashboards themselves, and New workspace and Import workspace are in a + menu.
- Web app: Fixed creating a new dashboard workspace failing; new workspaces always use the built-in query engine.

## 2026-11-22
- Added campaigns: a past time window can be run as a series of shorter slices, one after another, through the API and the copilot.
- Added reference sets whose entries come from an uploaded CSV or Excel file or from a connected spreadsheet, with a version history and rows that cannot be read reported by sheet row.
- Added export bindings, which write the results of a saved query into mapped columns of an Excel worksheet, matched by a key column. ([details](details/2026-11-22-export-bindings.md))
- Added a Decision review item to the inbox for decisions the platform flags for a person to confirm or correct.
- Improved the HubSpot integration so contact lifecycle stages can be built from the change history of a single property.
- Fixed some copilot requests to create QA forms failing with an internal error instead of saying what to correct.
- Web app: Added Reference sets and Export bindings pages under Settings, where administrators can edit, upload, review versions of and manage them.
- Web app: Added Subscriptions and Alerts icons to a dashboard's header, to manage its subscriptions and its alerts without the admin pages.
- Web app: Added a "…" menu to a dashboard with Details, History (with Revert), Duplicate and Delete.
- Web app: Added Views and Queries tabs to a dashboard workspace's home page for people who manage dashboards, listing every view, drafts and deleted views included, with a New view action and the workspace settings.
- Web app: Added a View layout panel to dashboard edit mode for the view's width, auto-refresh and opening page, and moved the view's render mode to its Details, so a static view can be switched back.
- Web app: Added a Filters panel to dashboard edit mode to add, edit, reorder and remove the view's filters, previewed live before you save.
- Web app: Added page management to the page tabs in dashboard edit mode: rename, hide or show, reorder by dragging, and delete; a new page is now part of your unsaved changes.

## 2026-11-21
- Added one-time runs of chosen steps of a workflow or of a past time window, each with a required reason that is recorded with the run, through the API and the copilot.
- Changed the copilot's ruleset tools to work with the new rulesets, so its proposed changes show each edit, the checks and the test results before you confirm them.
- Fixed NICE CXone recording and administration syncs sometimes failing when several ran at the same time.
- Fixed a VisionLink sync step failing, which held back integration health reporting.
- Strengthened permission checks for rerunning a workflow from a later step.
- Strengthened protection of the audit log against changes.
- Strengthened auditing of changes to sign-in tokens and API keys.
- Strengthened protection of record data in ruleset reports.
- Web app: Replaced the ruleset editor with a simpler one, where rules are edited in place as a table of conditions and results, with tests and versions, and each new ruleset chooses what kind of result it produces.
- Web app: Added a required Reason to the Run dialog when running chosen blocks or a past window, shown on the run's page.
- Web app: Fixed steps a backfill run leaves out showing as failed on the run canvas and Timeline; they now show as left out, with the reason.
- Web app: Added a US counties map to dashboards, so a state map can drill through to its counties.
- Web app: Fixed map tooltips and click targets sitting away from the drawn regions in some browsers.
- Web app: Changed the dashboard chart editor to a large dialog with tabbed settings, previewing the chart at its size on the dashboard.
- Web app: Removed the separate Analytics page; dashboards that still show its charts keep them until they move to built-in dashboards.

## 2026-11-19
- Improved the data catalog so tables list their columns, types and units with platform descriptions, and limited a tenant's own edits to table and column names and descriptions.
- Strengthened auditing of sign-ins with Google and Microsoft accounts.

## 2026-11-18
- Added checks of the values and references given to each workflow step; a missing required input, a value of the wrong type or an option the step does not offer now prevents publishing.
- Fixed workflow runs that resumed after a pause sometimes finishing without running their remaining steps, and several smaller issues with how steps read their inputs.
- Added a credential check for every supported connection sign-in method, run when credentials are saved or tested.
- Added more HubSpot options to workflow blocks: edited contacts, calls, emails, meetings, deals, notes and tasks, a contact filter and lifecycle tracking, all off unless chosen.
- Added a team filter to the QA and signals workflow blocks.
- Added an option to leave chosen phone lines out of RingCentral recording sync.
- Added rulesets to the copilot: it can read, check and try rulesets, and prepare changes to them, which are made only after you confirm them.
- Added editing of workflows built from activities to the copilot, with changes made only after you confirm them.
- Improved the Claude connector with built-in guidance and ready-made prompts for reviewing a QA form, auditing signals, building a dashboard for a question and exploring your data.
- Fixed the copilot cutting off replies that took more than a few seconds to start.
- Fixed copilot links to workflows not opening the right part of the workflow page.
- Improved dashboard loading speed.
- Strengthened workflow webhook security: webhook keys are now generated by the platform, stored securely and shown only once.
- Strengthened protection of stored integration credentials.
- Strengthened auditing of switches between tenants.
- Web app: Added Workflow Studio, one page with Properties, Blocks, Activities, Code, Runs and Versions tabs to build, check and run a workflow, with a searchable step catalogue grouped by integration and help on every step setting.
- Web app: Added lists to choose from for step settings that refer to data sources, AI models, reference datasets, QA forms, connections, agents, customers, HubSpot, CallRail and Microsoft 365 items, searched on the server when a list is long.
- Web app: Changed the workflow Code tab to check a definition against the platform's own definition rules.
- Web app: Added starting a new workflow from a template; it is always created as a draft to review and publish.
- Web app: Added the triggers that start a workflow to its page, where schedules and webhooks can be added, edited, switched off and removed, and moved the Triggers page under Workflows. ([details](details/2026-11-18-workflow-webhooks.md))
- Web app: Added Last run, Starts on, authoring, integrations, 7-day run and failure counts and step count columns to the workflows list, and a Health card on a workflow's Properties tab.
- Web app: Renamed decision policies to Rulesets, and grouped Definitions, Triggers, Rulesets and Run History under one Workflows menu.
- Web app: Added a ruleset editor with Facts, Rules, Results, Versions and Code tabs, where rules and conditions are edited as a form and every issue is shown where it is.
- Web app: Added fact lists per tenant for rulesets, shown by your tenant's names for them, with an explanation when a ruleset reads a list your tenant does not have.
- Web app: Added a summary of what a ruleset or workflow change would do to the copilot's confirmation card, with any problems listed first.
- Web app: Fixed copilot links dropping parts of their address, such as opening a ruleset's default version instead of the one linked.
- Web app: Added provider availability to the integrations catalog, with Enable and Disable for tenant administrators and Contact Sales for providers available on request.
- Web app: Improved connection forms to keep their fields in the intended order.
- Web app: Added a Map chart type to dashboards that shades US states or supported county maps by a query's values, and can draw your own regions as a region map or as outlines.
- Web app: Changed clickable dashboard values to look like plain text until you point at them, and one-row cards to show their description as a tooltip.
- Web app: Fixed dashboard cards where an expanded description squeezed the chart, an X-axis title overlapped the legend, or a one-row text card cut off its second line.
- Web app: Fixed dialogs showing about twice as wide as intended.
- Web app: Fixed manual evaluation forms with an Observational question that has no options, which could not be submitted, and Observational answers not being saved.
- Web app: Strengthened protection of the requests the web app sends on your behalf.

## 2026-11-14
- Completed the removal of the Halt workflow step: a workflow that still contains one can no longer be started, and past runs that ended at a Halt keep their status.

## 2026-11-13
- Added transcript search to the copilot: it can find conversations by what was said over a date range, count matches by day, agent, queue and more, read whole calls, and link to the moment something was said.
- Improved the copilot's handling of failed actions, so it learns why an action failed and can correct its next attempt.
- Fixed the copilot sometimes saying it could not start workflow runs.
- Changed workflow publishing to refuse workflows that contain a Halt step; use the run summary instead. Workflows already published with a Halt step keep running.
- Fixed filters on transcript, quality and insights data that are meant to ignore letter case matching only the exact case.
- Web app: Added chart variants and editor controls to dashboards, including a second value axis, line styles and markers, stack groups, horizontal bars, goal lines and shaded bands, donut, half and two-level pies, scatter trend lines and grouped treemaps.
- Web app: Added expandable card descriptions on dashboards, and an option to show a card's description as a tooltip.
- Web app: Added links that open a call's transcript at a specific moment, which the copilot uses in its transcript search results.
- Web app: Added a notice in copilot replies when an action fails for a reason it cannot fix itself, with a reference to give support.
- Web app: Fixed dashboard chart options that had no effect: legend position, series breakout, distinct colours beyond the fifth series, and PNG download.
- Web app: Fixed sankey charts not labelling their nodes and rendering blank when a value appeared on both sides.
- Web app: Fixed the dashboard Edit card dialog's controls sliding off-screen for cards with a long description or a wide table.

## 2026-11-12
- Added workflow help to the copilot: it can look up workflows and runs and prepare changes to them, which are made only after you confirm them.
- Changed copilot conversations so that only the user who had them and administrators can read them.
- Added backfills of a past date range to workflows built from blocks, optionally for only some of their blocks; a running backfill no longer causes the scheduled run to be skipped.
- Added a run summary to workflows, recorded when a run reaches its end.
- Added an option to keep HubSpot contacts up to date when they are edited after they were created.
- Improved workflow validation so problems with a stored decision policy are shown on the step and field they belong to.
- Improved workflow validation speed for very large workflow definitions.
- Strengthened auditing of account changes made through API clients.
- Web app: Added a Decision policies section for creating, versioning and activating stored decision policies, and the option to use a stored policy in a workflow step.
- Web app: Added a Blocks view for workflows built from blocks, where they can be viewed and edited block by block.
- Web app: Added a run view grouped by block, and options in the Run dialog to run only some blocks or backfill a past date range.
- Web app: Added a confirmation card for workflow changes the copilot prepares, and the copilot can now point to steps on workflow and run diagrams.
- Web app: Added a Finish step to the workflow designer for editing a workflow's run summary; the Halt step is no longer offered.
- Web app: Added searchable pickers in the workflow designer for inputs that refer to forms, signals, connections or other workflows.
- Web app: Added an editor for signal path maps in the workflow designer.
- Web app: Added the Completed with failures run status and skipped steps to workflow run views.
- Web app: Improved the workflow designer to hide inputs that are filled in automatically unless a step sets them.
- Web app: Fixed the cursor being lost when a workflow designer field switched editors while typing.
- Web app: Strengthened protection of web app pages.

## 2026-11-10
- Fixed customer lifecycle tracking keeping entries for contacts that had since been excluded, which could inflate funnel counts.
- Strengthened auditing of changes to user roles, permissions and account membership.
- Strengthened protection of platform credentials.

## 2026-11-07
- Maintenance and reliability improvements.

## 2026-11-06
- Fixed very large numeric identifiers losing precision when passed between workflow steps.
- Strengthened data isolation between accounts in workflow runs.

## 2026-11-05
- Fixed calls whose recording or transcript arrived after the call itself not showing that transcript or audio.
- Fixed HubSpot calls sometimes reaching transcripts, signals and reports a day late.
- Improved nightly data processing so it fully catches up in one run after a delayed or missed night.
- Fixed dashboard queries that cannot run showing a generic error; they now explain why the query was refused.
- Fixed some automated quality evaluations failing to complete.
- Improved workflow run reports so steps that had nothing new to process are no longer flagged as warnings.
- Strengthened auditing of changes to workflows, including who made each change.
- Strengthened access controls for workflows.

## 2026-11-04
- Maintenance and reliability improvements.

## 2026-10-31
- Fixed workflow runs failing when an interrupted step could not be restarted straight away; the step is now retried with its remaining attempts first.

## 2026-10-30
- Strengthened auditing of account sign-in and sign-out.
- Strengthened protection of customer data processed by AI services.
- Web app: Added Open and Preview actions to the dashboard views list, so draft and disabled views can be checked before they go live.
- Web app: Fixed options in dashboard filter drop-downs being cut off so that similar names could not be told apart.
- Web app: Fixed tables picked from the data catalog in the SQL query editor being rejected on save.
- Web app: Improved admin screens to hide options that account admins cannot use, instead of showing an error when they are opened.
- Web app: Fixed copilot tour steps closing on their own before Done or Next could be pressed.
- Web app: Strengthened browser security protections.

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
