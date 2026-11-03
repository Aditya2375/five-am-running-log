# FIVE / AM

Live: https://aditya2375.github.io/five-am-running-log/

A browser-local running journal with a separate sample-data view. Personal runs are never sent to the shared database. Use MY RUNS for your metrics and SAMPLE LOG to explore the design. Every total, chart and calendar uses only the selected source.

`npm install`, `npm run dev`; `npm run build -- --base=/five-am-running-log/` builds for the original Pages path. Fonts are self-hosted; licenses accompany them.

## Data and limits

New runs save on this browser only. Export JSON to keep a backup. Clearing storage, changing browser or device loses access to local runs. If storage is full or restricted, a visible warning explains that this tab's memory is the only copy. Export before closing. At most1000local runs are retained. Date/title/type, distance0.1–300km and time1–3000minutes are validated, including when loading stored entries. Future dates cannot be saved.

The Supabase endpoint supplies only explicitly marked sample rows, with a500row limit,15s timeout,1MB parsed-text limit and client validation. Failure falls back to bundled samples. Browser publishable key is intentionally public, not a credential proving server policies. No client writes or personal uploads exist. Server RLS, moderation and retention are not audited here.

Pace rounds total seconds correctly, including minute carry. Pace chart scales to the selected data. Multiple sessions on a date add together on the calendar. ALL includes every selected-source run, not a hidden60row cutoff. Sample and personal numbers are never mixed. This is a journal, not medical or training advice.
