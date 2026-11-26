# Cubrix Ontology: notice of changes

Cubrix Ontology is a modified version of **NVIDIA Auto Ontology**
(https://github.com/NVIDIA/auto-ontology), Copyright (c) 2024-2026 NVIDIA CORPORATION & AFFILIATES,
licensed under the Apache License, Version 2.0 (see [LICENSE](./LICENSE)). NVIDIA's copyright
headers, LICENSE, OPEN_SOURCE_NOTICE and third-party notices are kept as they were.

Changes are by Cubrix (ThirtyThree Industries LLC), https://cubrix.ai. Each file we changed says so
in its header (`Modified by Cubrix ...`). Cubrix Ontology is not made, endorsed or supported by
NVIDIA. "NVIDIA" and the NVIDIA logo are trademarks of NVIDIA Corporation; this project does not use
them as its own brand. NVIDIA's name appears only where it credits the original work, in copyright
notices, and in names of NVIDIA software it still uses (such as the `@nvidia/foundations-react-core`
component library and NVIDIA-hosted model names in configuration).

## Changes

Based on upstream commit `2aec7013a4d6ef75b29237703f24a53dcc5fd929` (2026-11-25).

**2026-11-26: Cubrix branding**

- Product name in the web app and the MCP server's messages: "Cubrix Ontology".
- The NVIDIA logo is replaced by the Cubrix mark (`frontend/common/icons/svg/cubrix-logo.svg`,
  `frontend/public/favicon.svg`); `nvidia-logo.svg` is removed.
- Colors: the NVIDIA green is replaced by CSS variables (`--color-brand` and friends in
  `frontend/app/globals.css`) set to the Cubrix palette: `#3DDC97` in dark mode and a deeper
  `#0A8F62` in light mode so text stays legible on white. Text on solid brand fills uses
  `--color-on-brand`.
- Fonts: Inter for text, Space Grotesk for headings, JetBrains Mono for code (as on cubrix.ai).
- Example admin addresses in `.env.example` use `cubrix.ai`.
- README introduction, this notice and UPSTREAM.md added.

Internal names (Python package `auto_ontology`, `AUTO_ONTOLOGY_*` settings, API paths, token
prefixes, database names, Helm chart) are unchanged so NVIDIA's updates keep merging cleanly.
