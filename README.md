# NovaGear Theme

NovaGear is a custom Shopify storefront theme designed for a modern gaming and tech retail brand. It combines a clean, conversion-focused storefront with modular sections, reusable snippets, and a structured theme architecture that makes it easy to adapt for branding, merchandising, and campaign content.

This theme is built for fast storefront customization, strong product presentation, and a strong online shopping experience that matches a premium gaming audience.

<p align="center">
  <a href="./LICENSE.md"><img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License"></a>
</p>

## Overview

NovaGear includes:

- A branded storefront layout with a simple header and navigation
- A large promotional hero banner for campaigns and collections
- Featured product sections powered by Shopify collections
- Reusable product cards with pricing and quick add functionality
- Global theme settings for typography, layout, colors, and page spacing
- Modular, Shopify-native sections that are easy to extend
- Responsive storefront structure designed for product discovery and conversions

## Project goals

The theme is structured to help a store owner or developer:

- Launch a premium storefront quickly
- Customize experiences via Shopify theme editor
- Reuse sections and snippets across multiple templates
- Maintain a clear component structure for future growth
- Adapt the theme for gaming, peripherals, accessories, and lifestyle products

## Tech stack

This project is built with the standard Shopify theme stack:

- Liquid templates
- JSON templates
- Shopify section schema configuration
- CSS styling via embedded styles and theme assets
- Shopify CLI for local theme development and deployment

## Theme structure

```bash
.
├── assets/              # Static assets such as CSS, images, icons, and fonts
├── blocks/              # Reusable block definitions for section content
├── config/              # Theme settings and configuration files
├── layout/              # Main page wrappers such as the theme layout
├── locales/             # Translation and locale JSON files
├── sections/            # Full-width storefront sections used by templates
├── snippets/            # Reusable Liquid snippets for shared UI patterns
├── templates/           # Page templates for products, collections, home, and more
├── README.md            # Project documentation
├── LICENSE.md           # MIT license
├── CONTRIBUTING.md      # Contribution guidelines
└── config/settings_data.json
```

## Core storefront components

### Header
The header section is defined in [sections/header.liquid](sections/header.liquid) and provides:

- Store branding and home link
- Main navigation menu
- Customer account link support
- Cart icon with item count badge

### Hero banner
The homepage hero is defined in [sections/hero-banner.liquid](sections/hero-banner.liquid). It supports:

- Background image selection
- Headline and supporting text
- CTA button with custom URL
- Shopify section presets for easy reuse

### Featured products
The featured collection section is defined in [sections/featured-products.liquid](sections/featured-products.liquid). It allows merchants to select a collection and display up to several promoted products.

### Product card snippet
Reusable product cards are built in [snippets/product-card.liquid](snippets/product-card.liquid). They include:

- Product image rendering
- Secondary image support
- Price display
- Direct product URL
- Quick add form with variant handling

### Global theme styling
Theme-wide tokens and styles are managed through [layout/theme.liquid](layout/theme.liquid) and [snippets/css-variables.liquid](snippets/css-variables.liquid). This keeps layout spacing, colors, and typography consistent across the storefront.

## Getting started

### Prerequisites

Before working on the theme, install:

- [Shopify CLI](https://shopify.dev/docs/api/shopify-cli)
- A Shopify store where the theme can be previewed and published
- Optional: [Shopify Liquid VS Code extension](https://shopify.dev/docs/storefronts/themes/tools/shopify-liquid-vscode) for improved editing support

### Clone the project

```bash
git clone <your-repository-url>
cd NovaGear-theme
```

### Log in to Shopify

```bash
shopify login --store your-store-name.myshopify.com
```

### Run a local preview

```bash
shopify theme dev
```

This starts a local preview that lets you test storefront updates live in a development environment.

### Pull or push theme changes

To sync the current theme with your Shopify store:

```bash
shopify theme pull
shopify theme push
```

## Customization guide

### Updating brand and colors
The theme uses theme settings located in [config/settings_schema.json](config/settings_schema.json). You can adjust:

- Typography
- Page width
- Page margins
- Background and foreground colors
- Input styling details

### Editing sections
Most storefront content is generated through section files in [sections](sections). Each section includes a schema, which lets merchants modify content through the Shopify theme editor without touching Liquid code.

### Adding new sections
To add a new feature:

1. Create a new Liquid section under [sections](sections)
2. Add a schema block for merchant-controlled settings
3. Render it on a template or section group
4. Test the layout in the local preview

### Working with templates
The main storefront pages live in [templates](templates), including product, collection, page, blog, cart, and homepage structures. These templates combine reusable sections and support store-level layouts.

## Recommended development workflow

1. Connect the repo to a Shopify store with Shopify CLI.
2. Run the theme in preview mode.
3. Update the relevant section or snippet.
4. Review the storefront in the local preview.
5. Push the theme when it is ready for testing or launch.

## Deployment

When the theme is ready to go live:

```bash
shopify theme push --allow-live --unpublished
```

Then publish the theme in the Shopify admin to make it live on the store.

## Contributing

Contributions are welcome as long as they improve the storefront experience, maintain code readability, and stay aligned with the project’s brand and theme architecture.

Please review [CONTRIBUTING.md](CONTRIBUTING.md) before proposing changes.

## License

This project is licensed under the [MIT License](LICENSE.md).

## Notes

NovaGear is intentionally structured as a flexible, modular storefront foundation. It is designed to be easy to extend for future campaigns, additional sections, and deeper e-commerce customization without sacrificing maintainability.

If you are using this theme as a starter for a gaming or lifestyle brand, the current structure already supports scaling toward more advanced product merchandising, landing pages, and promotional themes.
