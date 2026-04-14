# Voqa Calculator Tools

A collection of free, browser-based tools for businesses evaluating EV charging installations. Built and maintained by [Voqa](https://www.voqa.com) — EV charging solutions for hotels, workplaces, and commercial sites across the UK.

Live at: **[tools.voqa.com](https://tools.voqa.com)**

---

## Tools

| Tool | Path | Description |
|------|------|-------------|
| **Workplace EV Charging RoI Calculator** | `/workplace-roi/` | Analyse the financial return on installing workplace EV chargers — costs, grants, payback period |
| **WCS Eligibility Checker** | `/wcs-eligibility/` | Step-by-step checker to see if a business qualifies for the UK Workplace Charging Scheme grant (up to £500/socket, closes March 2027) |
| **Hotel EV Charging RoI Calculator** | `/hotel-calculator/` | Calculate additional room bookings needed to justify a hotel EV charging investment |
| **Holiday Park EV Charging Calculator** | `/holiday-park-ev/` | Revenue, payback, and infrastructure planning for guest EV charging at holiday parks |
| **EV Charging Range Calculator** | `/ev-charging/` | Estimate energy delivered and range added for different vehicles, charger ratings, and dwell times |
| **EV Charger Environmental Impact Calculator** | `/sustainability/` | CO2 avoided, litres of fuel saved, and ESG metrics for an EV charging deployment |

---

## Technical notes

- Each tool is a **single self-contained HTML file** — no build step, no dependencies, no back-end
- Styling uses **Red Hat Display** (Google Fonts) and a consistent Voqa design system (`#005C80` primary, `#F7D7BC` accent)
- Calculator state is persisted to **localStorage** so users can return to their inputs
- All pages include **Open Graph and Twitter Card meta tags** for social sharing
- Tax and grant figures are current as of **April 2026**

---

## Deployment

Files are served statically. Push to `main` to deploy.

---

© 2026 Voqa Ltd.
