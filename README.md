# NovaGear Theme

A premium Shopify storefront theme for modern gaming, technology, and lifestyle retail brands.

NovaGear is a clean, conversion-focused Shopify theme designed to showcase products, support promotional campaigns, and provide a scalable foundation for merchants seeking a refined digital storefront. Built around Shopify’s recommended architecture, the project emphasizes maintainability, section-based customization, and a professional e-commerce experience.

<p align="center">
  <a href="./LICENSE.md"><img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License"></a>
</p>

## Overview

NovaGear provides a polished storefront structure with:

- a branded header and navigation system
- a high-impact hero banner for campaigns and seasonal promotions
- featured collection sections for merchandising priority products
- reusable product cards with product pricing and quick-add functionality
- customizable typography, spacing, and color settings
- modular Shopify sections built for flexible storefront management
- a responsive layout optimized for product discovery and conversion

## Business and technical objectives

The theme is designed to help teams:

- launch a premium storefront quickly
- tailor the experience through the Shopify theme editor
- reuse common storefront patterns across multiple pages
- maintain a clean and scalable theme architecture
- adapt the brand for gaming, accessories, electronics, and lifestyle product catalogs

## Stack and tooling

NovaGear is built with the standard Shopify theme stack, including:

- Liquid templates
- JSON templates and schema configuration
- Shopify section architecture
- reusable snippets and embedded styles
- Shopify CLI for local development, preview, and deployment

## Repository structure

```bash
.
├── assets/                # Static assets including CSS, images, icons, and fonts
├── blocks/                # Reusable block definitions for modular section content
├── config/                # Theme configuration and schema settings
├── layout/                # Global page wrappers and theme shell
├── locales/               # Translation and locale files
├── sections/              # Storefront sections for homepage and nested content
├── snippets/              # Reusable UI components and shared logic
├── templates/             # Product, collection, page, and storefront templates
├── README.md              # Project documentation
├── LICENSE.md             # MIT license
├── CONTRIBUTING.md        # Contribution guidance
├── config/settings_data.json
└── config/settings_schema.json
```

## Core storefront components

### Header
Defined in [sections/header.liquid](sections/header.liquid), the header includes:

- brand navigation and home link
- storefront menu links
- customer account integration
- cart indicator with item count

### Hero banner
The hero section in [sections/hero-banner.liquid](sections/hero-banner.liquid) supports:

- background image selection
- headline and descriptive copy
- primary call-to-action button
- merchant-editable settings within the Shopify admin

### Featured products
The featured products section in [sections/featured-products.liquid](sections/featured-products.liquid) enables merchants to highlight curated collections and promote key inventory.

### Product card
The reusable product card in [snippets/product-card.liquid](snippets/product-card.liquid) includes:

- product image rendering
- secondary image support
- pricing display
- direct product linking
- quick-add functionality with variant handling

### Theme styling and configuration
Theme-wide design tokens and settings are managed through [layout/theme.liquid](layout/theme.liquid), [snippets/css-variables.liquid](snippets/css-variables.liquid), and [config/settings_schema.json](config/settings_schema.json).

## Prerequisites

Before working with the theme, ensure the following are available:

- [Shopify CLI](https://shopify.dev/docs/api/shopify-cli)
- an active Shopify store for preview and deployment
- optional editor support through the [Shopify Liquid extension](https://shopify.dev/docs/storefronts/themes/tools/shopify-liquid-vscode)

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

This launches a local preview environment for testing and refining storefront changes in real time.

### 4. Sync changes with Shopify

```bash
shopify theme pull
shopify theme push
```

## Customization guide

### Theme settings
Branding and layout controls such as typography, spacing, page width, and color values are managed through [config/settings_schema.json](config/settings_schema.json).

### Section-based editing
Most storefront content is defined in [sections](sections), with each section exposing merchant-editable schema settings within the Shopify admin.

### Adding a new section
To extend the storefront:

1. create a new Liquid section under [sections](sections)
2. define merchant-facing schema settings
3. render the section in the relevant template or section group
4. validate the experience in the local preview

### Template updates
Main storefront structures live under [templates](templates), where reusable sections are combined to build homepage, collection, product, cart, and supporting pages.

## Recommended development workflow

1. connect the project to the target Shopify store
2. run the theme in preview mode
3. edit the relevant section, snippet, or settings file
4. review changes in the browser
5. push the updated theme when ready for QA or launch

## Deployment

When the theme is ready for production, push it to Shopify and publish it from the admin:

```bash
shopify theme push --allow-live --unpublished
```

Then publish the theme in the Shopify admin to make it live for customers.

## Contributing

Contributions are welcome when they improve storefront quality, maintain clean code standards, and align with the project’s branding and technical direction.

Please review [CONTRIBUTING.md](CONTRIBUTING.md) before submitting changes.

## License

This project is licensed under the [MIT License](LICENSE.md).

## Summary

NovaGear is structured as a flexible and scalable storefront foundation for modern commerce brands. It is designed to support future expansion, campaign customization, and a refined shopping experience while maintaining Shopify best practices and code clarity.
