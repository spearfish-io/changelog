# Export bindings: query results written to an Excel worksheet

Released 2026-11-22.

## What changed

- An export binding connects a saved query to an Excel worksheet. It names the worksheet's key column and maps each query output to a column of the sheet.
- When the export runs, each row of the query's results is matched to the sheet line with the same key, and the mapped columns of that line are updated.
- Export bindings are listed under Settings → Export bindings, with each binding's mapping and its earlier versions.

## How to use it

- Open Settings → Export bindings and create a binding: choose the saved query, the worksheet, its key column and the column each output goes to.
- Editing a binding saves a new version; earlier versions stay listed with the binding.
- The query runs with your tenant's own data access, so a binding can export only data your tenant can query.

## What it guarantees

- Only the mapped columns are written. The key column is never written.
- Cells that hold a formula are never overwritten.
- A sheet line the query has no row for, and a query value that is empty, leave the sheet as it is.
- Values are written as their type: text stays text (including values such as `00123` or `TRUE`, and text that starts with `=`), so text is never turned into a formula; numbers, true/false values and dates are written as such.
- Every cell written is read back straight away; if it does not match, the export fails rather than reporting success.
- Creating, editing or deleting a binding requires a tenant administrator.

## Limits

- A sheet whose key values or column headers are ambiguous (for example, the same key on two lines) is refused rather than guessed at.
- Each export has a limit on the number of cells and the time it may spend writing.
