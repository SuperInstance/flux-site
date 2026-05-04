# FLUX Community Site

> Playground, benchmarks, PLATO→FLUX timeline, and PHP integration kit. Deploy at [cocapn.ai](https://cocapn.ai).

## What's Here

- **`pages/`** — Timeline (PLATO→FLUX evolution), Safe-TOPS/W comparison table
- **`php-kit/`** — Drop-in PHP widgets for Oracle1 and fleet sites
- **`static/`** — Shared CSS and assets
- **`Dockerfile`** — Containerized deployment

## PHP Integration Kit

Drop-in widgets for fleet sites:

| Widget | File | Description |
|--------|------|-------------|
| Constraint Playground | `php-kit/examples/constraint-playground.php` | Interactive FLUX constraint editor |
| Safe-TOPS/W Comparison | `php-kit/examples/benchmark-table.php` | Side-by-side benchmark table |
| PLATO Knowledge Browser | `php-kit/examples/plato-browser.php` | Browse PLATO rooms via FLUX |

### Quick Start

```php
<?php
require_once 'php-kit/flux-tiles.php';
require_once 'php-kit/flux-compiler.php';
// See php-kit/examples/ for full examples
```

## Deployment

```bash
docker build -t flux-site .
docker run -p 8080:80 flux-site
```

## License

Apache-2.0 — see [LICENSE](LICENSE).
