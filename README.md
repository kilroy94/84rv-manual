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

The current pages are a starter framework and proof of concept, not the final complete manual.
