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

### Recommended Category Icons

Set these in **Admin > Categories > [category] > Settings > Category Icon**.
Use the Font Awesome icon name (without `fa-` prefix).

| Category | Icon | FA Name |
|---|---|---|
| start here | Compass | `compass` |
| course updates | Bell | `bell` |
| in action | Rocket | `rocket` |
| the foundation | Pillars | `building-columns` |
| anything else? | Chat bubbles | `comments` |
| digging deeper | Microscope | `microscope` |
| course delivery | Chalkboard | `chalkboard-user` |
| translations | Globe | `globe` |
| BCF faculty | Graduation cap | `graduation-cap` |
| staff | Shield | `shield-halved` |
| site feedback | Lightbulb | `lightbulb` |
| Outside The Walls | Open door | `door-open` |
| Partners | Handshake | `handshake` |

