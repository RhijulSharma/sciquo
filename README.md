# Sciquo

Sciquo is a pnpm TypeScript workspace containing the project's API server,
component preview tooling, generated API libraries, database package, and
shared scripts.

## Getting started

```bash
pnpm install
pnpm run typecheck
```

## Workspace packages

- `artifacts/api-server` — Express API server, including `/api/healthz`
- `artifacts/mockup-sandbox` — Vite-powered component preview server
- `lib/api-spec` — OpenAPI source specification and code generation
- `lib/api-client-react` — generated React API client
- `lib/api-zod` — generated Zod schemas
- `lib/db` — Drizzle database package
- `scripts` — shared project utilities

## Development

Run the API server:

```bash
pnpm --filter @workspace/api-server run dev
```

Run the component preview server:

```bash
pnpm --filter @workspace/mockup-sandbox run dev
```

Regenerate API clients after changing the OpenAPI contract:

```bash
pnpm --filter @workspace/api-spec run codegen
```

## License

MIT