# PIN Docs Contributor Guide

This repo powers the PIN Help site in Mintlify. Keep docs practical, simple, and
written for non-technical users who are learning how to use the app.

## Screenshots

Use one image per `Frame`. Do not mix Markdown image syntax and `<img>` for the
same screenshot.

Do not use raw Markdown screenshots inside `Frame`:

```mdx
<Frame>
  ![IMG 2427 Portrait](/images/IMG_2427-portrait.png)
</Frame>
```

Do not use ad hoc image widths such as `42%`, `57%`, or `97%`.

### Mobile Screenshots

Use this pattern for phone screenshots:

```mdx
<div style={{ maxWidth: "380px", margin: "1.5rem auto" }}>
  <Frame>
    <img
      src="/images/example-mobile.png"
      alt="Clear description of the PIN screen"
      title="Clear description of the PIN screen"
      style={{ width: "100%", display: "block" }}
    />
  </Frame>
</div>
```

### Desktop Screenshots

Use this pattern for desktop or landscape screenshots:

```mdx
<Frame>
  <img
    src="/images/example-desktop.png"
    alt="Clear description of the PIN screen"
    title="Clear description of the PIN screen"
    style={{ width: "100%", display: "block" }}
  />
</Frame>
```

## Image Files

- Put docs images in `/images`.
- Reference images as `/images/file-name.png`.
- Use descriptive alt text that names the screen or action.
- Do not reference root-level image paths like `/screenshot.png`.
- Remove stale screenshots instead of leaving unused image markup in a page.

## Writing Style

- Write for operators, managers, and field teams, not developers.
- Explain what users should do and what they should expect to happen.
- Link to an existing page instead of repeating long instructions.
- Keep headings task-based, for example `Create a Pin` or `Assign a User`.
- Avoid API language, implementation details, and internal system terms unless
  the user will see the same wording in the product.

## Before Publishing

Run the checks from the repo root:

```bash
npx mintlify@latest validate
npx mintlify@latest broken-links
```

For pages with screenshots, also start a local preview and visually spot-check
desktop and mobile-style images:

```bash
npx mintlify@latest dev --no-open
```
