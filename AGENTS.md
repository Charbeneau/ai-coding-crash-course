# AGENTS.md

Modules in `app/services` and `app/lib` open with a `// ─── Name ───` header recording their responsibility and the reasoning behind non-obvious choices — read it before changing the module.

- `app/routes.ts` — the route table; a new page is registered here as well as created in `app/routes/`.
- `app/lib/access.server.ts` — authorisation; read before a loader or action touches course data.
- `app/test/setup.ts` — the test database and the `~/db` mock pattern; read before writing a service test.
- `app/lib/comment-markdown.server.ts` — the only renderer for user-written markdown.
- `npm run typecheck` regenerates `./+types/*` before `tsc`; bare `tsc` reports them missing.
