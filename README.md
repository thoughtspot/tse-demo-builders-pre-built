# TSE Demo Builders Pre-built Private

This repository contains pre-built configurations and assets for the TSE (ThoughtSpot Everywhere) Demo Builder system. It serves as a centralized location for storing and managing demo configurations, icons, styles, and other resources that can be used to quickly set up and customize TSE demo environments.

NOTE: Do not upload content directly to the public repository.  It will get deleted.  Coordinate with [@billdback-ts](https://github.com/billdback-ts) on the TSE team to add files.

## Repository Structure

### 📁 `configs/`
Contains pre-built TSE Demo Builder configurations in JSON format for industry-specific demo scenarios. Each configuration defines menu structures, a custom HTML home page, content selections, and navigation settings ready to import into the Demo Builder.

**Available configurations:**
- **Banking** — Retail and commercial banking analytics demo
- **Commercial Insurance** — Insurance operations and underwriting analytics demo
- **Corporate Finance** — Corporate financial planning and reporting demo
- **Finance Ops** — EMEA finance operations and project profitability demo
- **Pharma Supply Chain** — Pharmaceutical supply chain and inventory analytics demo

The `configs/previews/` subfolder contains PNG screenshots of each configuration's home page for quick reference.

### 📁 `icons/`
A collection of SVG icons for use with the TSE Demo Builder's Spotter interface. Icons are organized by industry vertical and include both full-size and preview variants.

**Available icon sets** (in `icons/spotter/`):
- Airbnb / B2C Marketing / Banking / Finance / Finance Ops
- Generic / Insurance / IoT & Manufacturing / Pharma
- Sales & Services / Super Shopper

Each icon ships as a pair: a primary SVG and a `-preview` SVG for thumbnail display.

### 📁 `styles/`
A collection of pre-built color theme JSON files that can be imported into the TSE Demo Builder to quickly apply consistent branding.

**Available themes:**
- `blue-dark` / `blue-light`
- `green-dark` / `green-light`
- `orange-dark` / `orange-light`
- `red-dark` / `red-light`
- `dark-mode`

## Getting Started

1. Browse the `configs/` folder (and `configs/previews/` screenshots) to find a configuration that matches your demo needs
2. Import the JSON configuration file into your TSE Demo Builder
3. Optionally import a style from `styles/` to apply a color theme
4. Optionally assign a Spotter icon from `icons/spotter/` to your demo menus
5. Customize as needed for your specific use case

## Contributing

When adding new configurations:
- Use descriptive filenames that indicate the demo purpose (e.g., `retail-banking.json`)
- Include a clear description in the configuration metadata
- Add a preview screenshot to `configs/previews/`
- Test configurations before committing

When adding new icons or styles:
- Follow the existing naming convention (`<vertical>-<variant>.svg` / `<color>-<mode>.json`)
- Provide both primary and preview SVG variants for icons

## Support

For questions about using these pre-built configurations or contributing to this repository, please refer to the TSE Demo Builder documentation or contact the development team.