# Red Hat Documentation Prototype

A prototype for recreating Red Hat documentation pages to test TOC split buttons and layout variations.

## Navigation Versions

This prototype includes 4 different navigation layout variations:

1. **[v2 - Categories get split buttons](https://wesleymiles.github.io/table-of-contents-v2/v2/index.html)** - Categories have split buttons with chevrons for expand/collapse functionality
2. **[v1 - Categories don't, styled like vertical nav](https://wesleymiles.github.io/table-of-contents-v2/v1/index.html)** - Categories exposed, styled like vertical nav
3. **[Local:8002 - Categories don't, chunkier layout](http://localhost:8002/index.html)** - Categories exposed, chunkier layout (run locally)
4. **[Local:8001 - Categories don't, compact layout](http://localhost:8001/index.html)** - Categories exposed, compact layout (run locally)

All versions include a floating widget in the bottom-right corner that allows you to switch between versions.

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

## Setup

### 1. Download Versions from GitHub Pages

First, download all versions from GitHub Pages:

```bash
./download-from-github.sh
```

This will download v1, v2, v3, and v4 (if they exist) from the GitHub Pages site.

### 2. Update Widget Links

After downloading, update all widgets to use localhost links:

```bash
./update-widgets.sh
```

This ensures all widgets link to the local server instead of GitHub Pages.

### 3. Start Local Server

Start a single server that serves all versions:

```bash
./start-server.sh
```

This starts a server on port 8000. Access versions at:
- **v1**: http://localhost:8000/v1/index.html
- **v2**: http://localhost:8000/v2/index.html
- **v3**: http://localhost:8000/v3/index.html
- **v4**: http://localhost:8000/v4/index.html

All versions include a widget in the bottom-right corner that allows you to switch between versions.

### Alternative Server Options

```bash
# Node.js (with http-server)
npx http-server -p 8000

# PHP
php -S localhost:8000
```

