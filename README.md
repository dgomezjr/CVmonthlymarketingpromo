# September 2026 promotions mockup

**Status:** Prototype / design review. Not the production build.

## What this is

A single-file HTML mockup of the monthly "what Res & Sales need to know"
promotions briefing, built from the Master Marketing Calendar. It splits
offers into two groups:

- **Client & traveler offers** — eligible for Special Offers on the
  public site.
- **Advisor incentive offers** — commission and booking incentives that
  can't appear pre-login, since they'd reveal commission structure.

This is a design and content prototype, not the recurring monthly tool.
The plan is for this format to become a Jinja2 + WeasyPrint build (same
pattern as the RSS and CS Ops Guides) fed by a proper data file — this
file is what that build should eventually produce.

## How to open it

Just open `september-promo-mockup.html` in a browser. No build step,
no dependencies beyond an internet connection for the Google Fonts.

## Editing content

There's no visible edit button by design — the page should look clean
to anyone who opens it. To turn on editing:

- **Click "Classic Vacations" in the header 5 times quickly**, or
- **Press Alt+Shift+E**

Either one opens a small toolbar in the bottom corner and makes every
field on the page click-to-edit (offer name, timing, what's included,
channels, and the advisor booking/travel window fields). You can also
add or remove offer cards while in edit mode.

**Important:** edits save to that browser's local storage only. They
are not shared across computers and are not saved anywhere central.
Opening this file on a different machine, or in a different browser,
starts from the original data again. "Reset to original" in the edit
toolbar clears local edits and restores the data below.

## What's still a placeholder

- **Terms and restrictions** aren't captured anywhere in the Master
  Calendar yet — only the advisor booking incentive has booking/travel
  window data, pulled from free text in the sheet. Everything else is
  missing this field entirely.
- **Tis the Season** only has a launch date confirmed; the actual offer
  specifics haven't come through from marketing.
- **5-Star Stays** was left out as a paid banner placement (no offer
  value for Res/Sales), same as Classic Picks — worth a second look
  since it may carry an actual Last Minute/EBB deal rather than pure
  ad space.
- Expired-by-publication offers (Classic Picks, Classic Celebrates
  Signature) were dropped rather than shown — worth deciding as a
  standing rule once this goes into production: exclude, or show with
  an "ending soon" flag.

## Source

Data pulled from the `2026 Campaigns` tab of the Master Marketing
Calendar (last updated 9/6/26), plus live copy from
classicvacations.com for the Takeoff destination offers.
