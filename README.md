# @imogen/shared

Zod schemas and the types inferred from them for the [imogen](https://github.com/ergofobe/imogen-server) API contract, shared by the server and every client. This repository is that package on its own: `package.json` is at the repo root.

```bash
bun add @imogen/shared
```

The server uses the schemas to validate requests and generate its OpenAPI document.

```ts
import { Asset, AssetQuery, ERROR_CODES } from '@imogen/shared'

const parsed = Asset.parse(payload)          // throws on a shape that does not match
const query = AssetQuery.parse(searchParams) // coerces and applies defaults
```

## Licence

AGPL-3.0-or-later. See `LICENSE`.
