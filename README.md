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

