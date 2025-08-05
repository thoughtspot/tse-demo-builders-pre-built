# Configs Folder

This folder contains pre-built TSE Demo Builder configurations in JSON format. These configurations are ready-to-use templates that can be imported into the TSE Demo Builder to quickly set up demo environments.

## Contents

### `sage-test.json`
A comprehensive demo configuration that includes:
- **Standard Menus**: Home, Spotter, Favorites, My Reports, Search, and Full App
- **Custom Menus**: Content menu, Banking, and Marketing with specific content selections
- **Content Filtering**: Both tag-based and specific content ID filtering
- **Menu Icons**: Mix of custom icons and emoji-based icons

## Configuration Structure

Each configuration file contains:
- **Version**: Configuration format version
- **Timestamp**: When the configuration was exported
- **Description**: Human-readable description of the demo purpose
- **Standard Menus**: Pre-defined menu items (Home, Spotter, etc.)
- **Custom Menus**: User-defined menu items with specific content selections

## Usage

1. Select a configuration file that matches your demo requirements
2. Import the JSON file into your TSE Demo Builder
3. Customize the configuration as needed for your specific use case
4. Test the configuration to ensure all menu items work as expected

## Adding New Configurations

When creating new configurations:
- Use descriptive filenames (e.g., `banking-demo.json`, `retail-dashboard.json`)
- Include a clear description in the configuration metadata
- Test the configuration thoroughly before committing
- Document any special requirements or dependencies

## File Format

All configuration files follow the TSE Demo Builder JSON schema and include:
- Menu definitions with icons and navigation settings
- Content selection criteria (tags, specific IDs, or patterns)
- Enabled/disabled states for menu items
- Custom properties for specialized functionality 