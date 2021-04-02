universal frontmatter:

published: true/false


link background_color is in /_sass/basics.scss.s

image links MUST lead with a / and MUST NOT finish with one...0-


changing look (display) of titles on smaller screens is in basic.scss?


---

In setting.yml:

*overlay_background_color*

Gives a nice background color for the small menu background (great), BUT: also
affects a little bit the overlay on main page (bad)

*overlay_opacity* should maybe fix this, but it doesn't seem to -- WHY?? [fixed]

---

In _sass folder:

_content.scss: change page content width…

_listing.scss: that's where the grid overlay opacity problem was… I turned it fully off now here, but there's still the nice yellow background on the mini menu.
