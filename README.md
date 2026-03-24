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

### Category Icons

Icons are managed via the [discourse-category-icons](https://github.com/discourse/discourse-category-icons) theme component.

**Installation:**

1. Go to **Admin > Customize > Components > Install**
2. Add the Git URL: `https://github.com/discourse/discourse-category-icons`
3. Add the component to the BCF-Bespoke-Theme

**Configuration:**

In the component settings, set `category_icon_list` (one per line, format: `slug,icon,color`):

```
start-here,compass,#EF404E
course-updates,bell,#EF404E
in-action,rocket,#8854D0
foundation,building-columns,#503F99
anything-else,comments,#FBB050
digging-deeper,microscope,#4BBBF0
delivering-better,chalkboard-user,#EF404E
translations,globe,#A8D381
bcf-faculty,graduation-cap,#EF404E
staff,shield-halved,#EF404E
site-feedback,lightbulb,#454545
otw,door-open,#4BBBF0
partners,handshake,#503F99
```

Set `svg_icons` to:

```
compass|bell|rocket|building-columns|comments|microscope|chalkboard-user|globe|graduation-cap|shield-halved|lightbulb|door-open|handshake
```

> **Note:** Verify category slugs match your actual slugs in **Admin > Categories > [category] > Settings** (or from the category URL).

