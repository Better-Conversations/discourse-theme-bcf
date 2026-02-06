# BCF Theme

Based on the Discourse Mint theme.

## ⚙️ Configuration

### Discourse Settings

Following setting changes are required for this theme to render properly:

- `top menu` needs to be set to **category, latest, new, unread, top**
- `desktop category page style` needs to be set to **Boxes with Subcategories**

### Welcome Banner (Core)

The old `discourse-search-banner` theme component has been removed from this theme.  
Use Discourse core welcome banner functionality instead:

- Configure your banner from the admin interface using the current Discourse "welcome banner" feature.
- If the old search banner component is still installed on your site, remove it from your active theme/component list.

