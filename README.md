# Red Hat Documentation Prototype

A prototype for recreating Red Hat documentation pages to test TOC split buttons and layout variations.

## Navigation Versions

- **[Expanded Navigation (v1)](v1/index.html)** - Non-collapsible top-level categories
- **[Collapsible Navigation (v2)](v2/index.html)** - Split button categories with expand/collapse functionality

## Benefits Comparison

### Benefits of Expanded Navigation (v1)

- One less level of indenting
- User relies on scroll rather than opening and closing (arguably less work)
- Emphasizes label, since they stick

### Benefits of Collapsible Navigation (v2)

- Matches current site and design system
- Easier to select a category and drill down

## Setup

The project uses:
- **Red Hat Design System** (RHDS) v4.0.0 via jsDelivr CDN
- **Design Tokens** for typography, colors, and spacing
- **Navigation Components** (`rh-navigation-primary` and `rh-navigation-secondary`)

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

