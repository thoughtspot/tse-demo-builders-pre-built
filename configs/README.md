# Configs Folder

This folder contains pre-built TSE Demo Builder configurations in JSON format. Each configuration is a ready-to-import template for a specific industry vertical, including a custom HTML home page, standard menu settings, and custom menus linked to demo content.

## Available Configurations

| File | Demo Scenario |
|---|---|
| `Banking.json` | Retail and commercial banking analytics |
| `Commercial Insurance.json` | Insurance operations and underwriting analytics |
| `Corporate Finance.json` | Corporate financial planning and reporting |
| `Finance Ops.json` | EMEA finance operations and project profitability |
| `Healthcare Clinical Ops.json` | Healthcare clinical operations and patient analytics |
| `HR Analytics.json` | Human resources workforce analytics |
| `IoT Manufacturing.json` | IoT and manufacturing operations analytics |
| `Pharma Clinical Trials.json` | Pharmaceutical clinical trials and research analytics |
| `Pharma Supply Chain.json` | Pharmaceutical supply chain and inventory analytics |
| `Retail Sales.json` | Retail sales performance and inventory analytics |
| `Soccer Football.json` | Soccer/football performance and team analytics |
| `Spotflix.json` | Media streaming and content analytics |
| `Wealth Management.json` | Wealth management and investment portfolio analytics |

## Previews

The `previews/` subfolder contains a PNG screenshot of each configuration's home page. Use these to quickly identify the right configuration before importing.

## Configuration File Structure

Each JSON file follows this top-level structure:

```json
{
  "standardMenus": [...],
  "customMenus": [...],
  "settings": {...}
}
```

### Standard Menus

Standard menus are fixed menu items provided by the Demo Builder. Each configuration enables or disables them and sets their display properties:

| Menu ID | Purpose |
|---|---|
| `home` | Custom HTML home page — the main landing page for the demo |
| `spotter` | ThoughtSpot Spotter AI assistant, bound to a specific data model |
| `search` | Natural language search, bound to a specific data model |
| `my-reports` | User's saved reports |
| `favorites` | User's favorited content |
| `full-app` | Full ThoughtSpot app navigation |
| `all-content` | Browseable content library |

The `home` menu contains the full HTML for the landing page in its `homePageValue` field.

The `spotter` and `search` menus reference a model GUID (`spotterModelId` / `searchDataSource`) that must exist in the target ThoughtSpot instance.

### Custom Menus

Custom menus surface specific demo content:

```json
{
  "id": "...",
  "name": "Industry Analytics",
  "contentType": "collection",
  "collectionId": "<collection-guid>",
  "collectionName": "<leaf-name>",
  "icon": "..."
}
```

Typical configurations include two custom menus:
- A **collection browser** showing all content in the demo collection
- A **liveboard** linking directly to a featured dashboard

## Creating a New Configuration

The file `prompt-template.txt` contains a prompt you can paste into Claude (or another AI assistant) to generate a complete, import-ready configuration in one pass.

### Steps

1. **Gather the required GUIDs** from the target ThoughtSpot instance:
   - Liveboard GUID (for the featured dashboard custom menu)
   - Model GUID (used by Spotter, Search, and Chatbot)
   - Collection GUID and name (for the content browser custom menu)

2. **Check for an existing icon set** in `../icons/spotter/`. Look for `<industry>-01.svg` and `<industry>-preview-01.svg`. If they exist, use the CDN URLs (see the template for the base URL). If not, follow the template instructions to create them.

3. **Open `prompt-template.txt`** and fill in all `<placeholder>` values:
   - GUIDs from step 1
   - App/brand name, Spotter label, and industry name
   - Icon paths from step 2
   - A short scenario description for the home page content

4. **Paste the completed prompt** into Claude or another AI assistant to generate the JSON configuration.

5. **Save the output** as `<Industry Name>.json` in this folder.

6. **Take a screenshot** of the home page and save it as `previews/<Industry Name>.png`.

7. **Update `../README.md`** to add the new configuration to the available configurations list.

### Naming Conventions

- Configuration files: `Title Case With Spaces.json` (e.g., `Retail Sales.json`)
- Preview screenshots: matching filename with `.png` extension in `previews/`
- Icons: `<industry>-01.svg` and `<industry>-preview-01.svg` in `../icons/spotter/`

### Testing Before Committing

- Import the JSON into a Demo Builder instance
- Verify the home page renders correctly
- Confirm the Spotter and Search menus load without errors (GUIDs must resolve)
- Confirm the custom menus display the expected content
