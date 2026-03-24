# BCF Theme

Based on the Discourse Mint theme.

## 🚀 Installation

The theme must be installed from Git so that updates to this repository are automatically available in Discourse.

### Installing from Git (fresh install)

1. Go to **Admin > Customize > Themes & components**
2. Click **Install** and select **From a Git repository**
3. Enter the repo URL: `https://github.com/Better-Conversations/discourse-theme-bcf`
4. Click **Install**
5. Once installed, click on the theme and set it as the **active theme** for your site

### Migrating from a manually pasted theme

If the theme was previously created by pasting CSS directly into the admin editor:

1. **Note down** any included components (e.g. Category Icons, Homepage Feature) — you'll re-add these
2. **Note down** any theme setting overrides (colour palette selections, etc.)
3. Install the theme from Git using the steps above
4. Re-add the same components to the new Git-linked theme
5. Re-apply any theme setting overrides
6. Set the new theme as active
7. Delete the old manually-created theme

### Updating the theme

Once installed from Git, go to **Admin > Customize > Themes & components > BCF-Bespoke-Theme** and click the **update** button (or enable auto-update in the theme settings to check for updates periodically).

## 🎨 Colour Palettes

The theme includes two colour palettes defined in `about.json`:

- **BCF-light** — white background, purple (#503F99) tertiary, orange (#FBB050) quaternary
- **BCF-dark** — dark background (#2d2d2d), lighter purple (#8b5ca2) tertiary

These are created automatically when the theme is installed from Git. Set them in **Admin > Customize > Themes > BCF-Bespoke-Theme** under Colour Palette / Dark Color Palette.

## 📦 Required Components

The theme requires two components:

1. **Homepage Feature** — `https://github.com/nolosb/discourse-featured-cards`
   (listed in `about.json`, may auto-install)
2. **Category Icons** — `https://github.com/discourse/discourse-category-icons`
   (see configuration below)

Add both via **Admin > Customize > Components > Install** and attach them to the BCF-Bespoke-Theme.

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

### Category Colours

Colours follow the BCF brand system:

| Colour | Hex | Used for |
|---|---|---|
| Teal | `#3DBBAA` / `#5BC3B6` | Foundation, brand identity |
| Purple | `#8854D0` / `#7C5CB8` | Online discussions, community |
| Orange | `#FBB050` / `#E8935A` | Course-related |
| Blue | `#4BBBF0` | Partners |
| Slate | `#6C7A89` / `#8E99A4` | Admin categories |

Set the **category badge colour** for each category in **Admin > Categories > [category] > Settings**:

| Category | Colour | Hex |
|---|---|---|
| start here | Teal | `#3DBBAA` |
| course updates | Orange | `#FBB050` |
| in action | Warm orange | `#E8935A` |
| the foundation | Teal | `#5BC3B6` |
| anything else? | Purple | `#8854D0` |
| digging deeper | Light purple | `#7C5CB8` |
| course delivery | Warm orange | `#E8935A` |
| translations | Teal | `#3DBBAA` |
| BCF faculty | Teal | `#5BC3B6` |
| staff | Slate | `#6C7A89` |
| site feedback | Light slate | `#8E99A4` |
| Outside The Walls | Teal | `#3DBBAA` |
| Partners | Blue | `#4BBBF0` |

### Category Icons

Icons are managed via the [discourse-category-icons](https://github.com/discourse/discourse-category-icons) theme component.

**Installation:**

1. Go to **Admin > Customize > Components > Install**
2. Add the Git URL: `https://github.com/discourse/discourse-category-icons`
3. Add the component to the BCF-Bespoke-Theme

**Configuration:**

In the component settings, set `category_icon_list` (one per line, format: `slug,icon,color`):

```
start-here,compass,#3DBBAA
course-updates,bell,#FBB050
in-action,rocket,#E8935A
foundation,building-columns,#5BC3B6
anything-else,comments,#8854D0
digging-deeper,microscope,#7C5CB8
delivering-better,chalkboard-user,#E8935A
translations,globe,#3DBBAA
bcf-faculty,graduation-cap,#5BC3B6
staff,shield-halved,#6C7A89
site-feedback,lightbulb,#8E99A4
otw,person-hiking,#3DBBAA
partners,handshake,#4BBBF0
```

Set `svg_icons` to:

```
compass|bell|rocket|building-columns|comments|microscope|chalkboard-user|globe|graduation-cap|shield-halved|lightbulb|person-hiking|handshake
```

> **Note:** Verify category slugs match your actual slugs in **Admin > Categories > [category] > Settings** (or from the category URL).

