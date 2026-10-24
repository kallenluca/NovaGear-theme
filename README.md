# NovaGear Theme

Modern Shopify storefront theme for premium gaming, tech, and lifestyle retail brands.

NovaGear is a clean, conversion-focused Shopify theme built to showcase products, highlight campaigns, and support a scalable storefront experience for merchants who want a polished digital presence without sacrificing flexibility. The codebase follows Shopify’s recommended architecture and is organized for easy customization, section-based editing, and long-term maintainability.

<p align="center">
  <a href="./LICENSE.md"><img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License"></a>
</p>

## Overview

NovaGear delivers a premium storefront foundation with:

- branded header and navigation structure
- promotional hero banner for campaigns and seasonal offers
- collection-driven featured product sections
- reusable product card components with pricing and quick add support
- theme-wide typography, spacing, and color configuration
- modular Shopify sections designed for merchants and developers
- responsive storefront layout focused on product discovery and conversion

## Business and technical goals

This project is designed to help teams:

- launch a polished storefront quickly
- customize experiences through the Shopify theme editor
- reuse product and layout patterns across multiple pages
- maintain a scalable and structured theme architecture
- adapt the storefront for gaming gear, accessories, electronics, and lifestyle products

## Stack and tooling

NovaGear is built using the standard Shopify theme stack:

- Liquid templating
- JSON templates and schema configuration
- Shopify section architecture
- embedded styles and reusable snippets
- Shopify CLI for local theme development, previewing, and deployment

## Repository structure

```bash
.
├── assets/                # Static assets such as CSS, images, icons, and fonts
├── blocks/                # Reusable block definitions for section content
├── config/                # Theme settings and configuration files
├── layout/                # Main page wrappers and global theme structure
├── locales/               # Translation and language JSON files
├── sections/              # Modular storefront sections for homepage and other templates
├── snippets/              # Reusable Liquid components and shared UI patterns
├── templates/             # Product, collection, page, and storefront template definitions
├── README.md              # Project documentation
├── LICENSE.md             # MIT license
├── CONTRIBUTING.md        # Contribution guidance
├── config/settings_data.json
└── config/settings_schema.json
```

## Key storefront components

### Header
Implemented in [sections/header.liquid](sections/header.liquid), the header includes:

- brand/logo navigation
- storefront menu links
- customer account access
- cart summary indicator with item count

### Hero banner
The homepage hero section in [sections/hero-banner.liquid](sections/hero-banner.liquid) supports:

- image-based promotional background
- headline and supporting copy
- primary call-to-action button
- merchant-controlled section settings

### Featured products
The featured products section in [sections/featured-products.liquid](sections/featured-products.liquid) allows merchants to showcase selected collections with a curated product layout.

### Product card
Reusable product cards in [snippets/product-card.liquid](snippets/product-card.liquid) include:

- featured and secondary product images
- product title and pricing
- product URL linking
- quick add access with variant selection

### Theme styling and configuration
Global design tokens and theme configuration are managed in [layout/theme.liquid](layout/theme.liquid), [snippets/css-variables.liquid](snippets/css-variables.liquid), and [config/settings_schema.json](config/settings_schema.json).

## Prerequisites

Before working on the theme, make sure you have:

- [Shopify CLI](https://shopify.dev/docs/api/shopify-cli)
- a Shopify store connected to your development environment
- optional editor support from the [Shopify Liquid extension](https://shopify.dev/docs/storefronts/themes/tools/shopify-liquid-vscode)

## Quick start

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd NovaGear-theme
```

### 2. Authenticate with Shopify

```bash
shopify login --store your-store-name.myshopify.com
```

### 3. Run the theme locally

```bash
shopify theme dev
```

This starts a local preview environment for testing and refining storefront changes in real time.

### 4. Sync theme changes

```bash
shopify theme pull
shopify theme push
```

## Customization guide

### Theme settings
Theme-wide customizations such as fonts, page spacing, layout width, and color values are controlled through [config/settings_schema.json](config/settings_schema.json).

### Section-based editing
Most visible storefront content is defined in [sections](sections). Each section includes a schema enabling merchant edits without direct code changes in the theme editor.

### Adding new sections
To extend the storefront:

1. create a new Liquid section in [sections](sections)
2. define merchant-facing settings in the section schema
3. render the section in the relevant template or group
4. validate the result in the local preview

### Template updates
The main store templates live under [templates](templates). These files combine reusable sections to structure homepage, collection, product, cart, and other pages.

## Recommended development workflow

1. connect the project to the target Shopify store
2. run the theme in local preview mode
3. edit the relevant section, snippet, or setting
4. review the storefront in the browser
5. push the updated theme when ready for QA or launch

## Deployment

When the theme is ready for production, push it to Shopify and publish it from the admin panel:

```bash
shopify theme push --allow-live --unpublished
```

Then publish the theme in the Shopify admin to make it live for customers.

## Contributing

Contributions are welcome when they improve product presentation, maintain clean code quality, and align with the project’s storefront goals and design direction.

Please review [CONTRIBUTING.md](CONTRIBUTING.md) before submitting changes.

## License

This project is licensed under the [MIT License](LICENSE.md).

## Summary

NovaGear is intentionally structured as a flexible, modular storefront foundation for modern commerce brands. It is built to support future expansion, campaign customization, and a more refined shopping experience without sacrificing maintainability or Shopify best practices.
