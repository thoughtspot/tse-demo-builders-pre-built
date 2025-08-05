# TSE Demo Builders Pre-built Private

This repository contains pre-built configurations and assets for the TSE (ThoughtSpot Everywhere) Demo Builder system. It serves as a centralized location for storing and managing demo configurations, icons, and other resources that can be used to quickly set up and customize TSE demo environments.

NOTE: Do not upload content directly to the public repository.  It will get deleted.  Coordinate with [@billdback-ts](https://github.com/billdback-ts) on the TSE team to add files.

## Repository Structure

### 📁 `configs/`
Contains pre-built TSE Demo Builder configurations in JSON format. These configurations define menu structures, content selections, and demo environment settings that can be imported and used to quickly set up demo environments.

### 📁 `icons/`
A collection of saved icons that can be used for custom menu items and navigation elements. **Note: Custom icon support is coming soon!** This folder is prepared for future functionality.

### 📁 `.github/`
Contains GitHub Actions workflows for CI/CD processes, including:
- Jenkins trigger workflows
- Sonar scan configurations
- Sync to public mirror workflows

## Usage

### Configurations
The `configs/` folder contains ready-to-use demo configurations that can be imported into the TSE Demo Builder. Each configuration file includes:
- Standard menu definitions (Home, Spotter, Favorites, Reports, Search, Full App)
- Custom menu configurations with specific content selections
- Content filtering by tags or specific IDs
- Menu icons and navigation settings

### Icons (Coming Soon)
The `icons/` folder will support custom icon uploads and management for personalized demo experiences.

## Getting Started

1. Browse the `configs/` folder to find a configuration that matches your demo needs
2. Import the JSON configuration file into your TSE Demo Builder
3. Customize the configuration as needed for your specific use case

## Contributing

When adding new configurations:
- Use descriptive filenames that indicate the demo purpose
- Include comprehensive documentation in the configuration description
- Test configurations before committing

## Support

For questions about using these pre-built configurations or contributing to this repository, please refer to the TSE Demo Builder documentation or contact the development team. 