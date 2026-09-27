# FIVE / AM

A running log for the early hours, presented as a local-first app. It opens with built-in history so every view works from the first visit. Add your own runs in the browser; entries persist in localStorage on that device. There is no account, backend, or sync.

## Start
`npm install && npm run dev` then `npm run build` for a production build.

## Backend

The log is a shared Supabase Postgres table (`public.fiveam_runs`) read over PostgREST with the project's publishable browser key. Row Level Security: anyone can read, anyone can insert (validated server-side by check constraints — sane date/km/minutes ranges, fixed run-type enum, capped title), nobody can update or delete. Logging a run posts straight to the shared log; if the database is unreachable the entry saves to `localStorage` and the built-in sample seed shows instead (footer switches from "SHARED LOG · LIVE" to "PROTOTYPE / SAMPLE DATA"). No account, nothing personal asked. The seeded rows carry `demo: true` and are labeled "sample entry" in the UI.
