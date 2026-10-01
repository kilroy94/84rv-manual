# Architecture

## Overview

The project is intentionally browser-first.

The browser is responsible for:
- screen preview
- Letter-size pagination
- print layout
- PDF creation through the native print dialog

No separate PDF rendering engine is required for the primary workflow.

## Layers

### 1. Design tokens

`css/tokens.css`

Contains shared colors, typography choices, dimensions, radii, and spacing values.

### 2. Page layout

`css/layout.css`

Defines:
- Letter-size page geometry
- running headers
- page footers
- section titles
- generic layout helpers

### 3. Components

`css/components.css`

Defines the publication vocabulary:
- specification cards
- callouts
- procedure steps
- troubleshooting diagrams
- warning panels
- photographs
- highlights

These classes should be reused rather than recreated per page.

### 4. Print behavior

`css/print.css`

Defines:
- exact Letter page size
- print page breaks
- background color preservation
- break avoidance for important components

## Content strategy

The current `index.html` is deliberately simple for the initial framework.

The next architectural step is to split model content into discrete source files and introduce a lightweight build step that assembles those files into the finished publication. That build step should remain transparent and easy to maintain.

Shared content should ultimately live separately from model-specific overrides so common procedures can be reused across RV types.
