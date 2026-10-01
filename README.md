# 84RV Manual Publishing System

A browser-first, print-ready manual framework for 84RV Rentals.

## Goals

- Produce high-quality Letter-size manuals with HTML and CSS.
- Keep layout reusable and maintainable.
- Separate content from presentation.
- Make browser print output the canonical PDF/print workflow.
- Support multiple RV models without duplicating shared content.

## Structure

```
/
├── index.html
├── css/
│   ├── tokens.css
│   ├── components.css
│   ├── layout.css
│   └── print.css
├── content/
│   └── sunseeker-24/
│       ├── driving.html
│       ├── thermostat.html
│       ├── ac-troubleshooting.html
│       └── propane-leak-detector.html
├── assets/
│   ├── images/
│   └── icons/
└── docs/
    ├── architecture.md
    └── authoring-guide.md
```

## Preview

Open `index.html` in Chrome or Edge.

## Print

Use the browser print dialog:

- Paper size: Letter
- Scale: 100%
- Margins: None
- Background graphics: On
- Headers and footers: Off

The print stylesheet defines page dimensions, page breaks, and print-specific behavior.

## Design philosophy

The project treats the manual as a publication, not as a conventional web page. Reusable classes provide consistent treatments for:

- procedures
- tips
- facts
- warnings
- important notices
- troubleshooting grids
- specifications
- photographs and captions
- section headers
- model-specific metadata

The repository now contains a first-pass conversion of the original 24’ 6 Series Sunseeker manual. The original manual remains the content source of truth. Some source photographs/maps still need to be migrated into repository assets, and editorial cleanup is intentionally deferred to a separate review pass.\n\nAfter editing modular content, run `node build.js` to regenerate `index.html`.
