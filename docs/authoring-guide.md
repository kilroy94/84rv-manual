# Authoring Guide

## General rule

Use semantic publication components instead of styling individual elements inline.

## Tips

```html
<div class="callout tip">
  <div class="callout-label">TIP</div>
  <div class="callout-body">Helpful information goes here.</div>
</div>
```

## Facts

```html
<div class="callout fact">
  <div class="callout-label">FACT</div>
  <div class="callout-body">Reference information goes here.</div>
</div>
```

## Procedures

```html
<div class="procedure">
  <div class="step">
    <div class="step-number">1</div>
    <div class="step-body">Perform the first step.</div>
  </div>
</div>
```

## Troubleshooting

Use the standard five-column flow:

```
Problem -> Possible Cause -> Possible Solution
```

Each troubleshooting row should correspond to one problem/cause/solution relationship.

## Warnings

Use `.warning-panel` for safety-critical instructions that need a visually dominant treatment.

## Page rules

- Each printable page is a `.page` section.
- Use the page header consistently.
- Keep footer page numbering inside `.page-footer`.
- Avoid inline styles except during temporary experiments.
- Prefer reusable classes whenever a treatment appears more than once.
