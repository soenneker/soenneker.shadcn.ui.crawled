# Soenneker.Shadcn.UI.Crawled

A generated crawl of the shadcn/ui site used as source material for component-preview extraction and comparison.

## Contents

- `index.html` is the captured site entry page.
- `docs/`, `blocks/`, `charts/`, `examples/`, `preview/`, and related directories mirror captured routes.
- `_next/` and `_vercel/` contain framework assets referenced by the HTML.
- `llms.txt`, `rss.xml`, icons, CSS, images, fonts, and SVG files are captured site resources.

This repository is a point-in-time artifact, not the shadcn/ui source project and not a package to install in an application.

## Inspecting the crawl

The HTML uses root-relative paths such as `/_next/...`. To inspect pages with their captured assets, serve the repository root through a local static HTTP server rather than opening files with `file://`.

Some pages may still depend on runtime behavior, network endpoints, or assets that were not captured. A page rendering successfully does not mean its original application interactions work offline.

Captured content can include hashed asset names, deployment identifiers, generated element IDs, and framework hydration data. Treat those values as unstable. Use route structure and semantic component markup when comparing generations.

The crawl is refreshed by `Soenneker.Shadcn.UI.Runner`. Direct changes to captured files may be replaced by a later refresh.
