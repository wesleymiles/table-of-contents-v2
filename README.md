# Red Hat Documentation Prototype

A prototype for recreating Red Hat documentation pages to test TOC split buttons and layout variations.

## Setup

The project uses:
- **Red Hat Design System** (RHDS) v4.0.0 via jsDelivr CDN
- **Design Tokens** for typography, colors, and spacing
- **Navigation Components** (`rh-navigation-primary` and `rh-navigation-secondary`)

## Using Red Hat Design System Components

The navigation components are already loaded and available. You can use them like this:

### Primary Navigation
```html
<rh-navigation-primary>
  <a href="#" slot="logo">Red Hat</a>
  <a href="#" slot="item">Products</a>
  <a href="#" slot="item">Support</a>
</rh-navigation-primary>
```

### Secondary Navigation
```html
<rh-navigation-secondary>
  <a href="#" slot="item">Documentation</a>
  <a href="#" slot="item">Guides</a>
</rh-navigation-secondary>
```

## Design Tokens

The design tokens CSS is loaded and provides CSS custom properties like:
- `--rh-font-family-body-text` - Body text font
- `--rh-font-family-heading` - Heading font
- `--rh-color-brand-red-on-white` - Red Hat brand red
- And many more...

See the [Red Hat Design System documentation](https://ux.redhat.com) for full token reference.

## Running Locally

Simply open `index.html` in a browser, or use a local server:

```bash
# Python 3
python3 -m http.server 8000

# Node.js (with http-server)
npx http-server

# PHP
php -S localhost:8000
```

Then visit `http://localhost:8000`

