# Kuwait company navigator

**[Open the navigator](https://jalalhussein1982.github.io/kw-companies/)**

Browse a public-source snapshot of **1,757 company candidates across 23 fields of work**, collected on **24 October 2026**. A separate eligibility-review view contains 144 review or excluded records.

Search company names, activities, emails or phones; combine sector, email availability, department and phone filters. Open a company to inspect its published contacts, source links and review notes. Export the filtered results as CSV or copy a company's attributed email addresses.

## Downloads

These are the same files linked from the navigator's **Files** menu:

| File | Contents |
|---|---|
| [Excel workbook](outputs/kuwait-directory-2026-10-24/kuwait-company-directory.xlsx) | Company directory, contacts, coverage and eligibility review. |
| [Company list · CSV](data/companies.csv) | One row per candidate, including grouped attributed emails and phones. |
| [Contact observations · CSV](data/contacts.csv) | Published contact values, department labels, attribution flags, source URLs and collection dates. |
| [SQLite database](outputs/kuwait-directory-2026-10-24/kuwait-companies.sqlite) | Queryable companies, contacts, categories and source evidence. |

CSV files use UTF-8 with BOM and protect cells beginning with formula characters with an apostrophe. The workbook stores phone values as text. Repeated observations of a contact on different source pages are intentional evidence, not additional unique contacts.

## Use locally

Download or clone this repository and open `index.html` in a browser. The page embeds its data, CSS and JavaScript, so search and filtering work offline. External company and source links require internet. Keep the accompanying folders to use the Files menu.

To serve the folder locally:

```sh
python3 -m http.server 8766 --bind 127.0.0.1
```

Then open `http://127.0.0.1:8766/`. Press `/` to focus search and Escape to return from company details.

## Homepage publishing

GitHub Pages serves the navigator from the root `index.html` on the `main` branch. The `.nojekyll` file allows the standalone page and its downloads to be served directly. The repository website link points to the navigator.

Commit changes to `index.html` and any updated downloads, then push to `main` to publish. There is no backend or API credential to configure.

This repository contains the standalone browser and its linked downloads. Collection caches, processing logs, supplementary datasets and local development files are excluded.

## Reading the directory

This is a collected public-source directory, not a complete national register or a verified list of SMEs. **SME status is unverified.** A Kuwait listing establishes neither current operations nor Kuwaiti ownership.

- Activity summaries are published excerpts or labelled category-only fallbacks. Promotional claims are not independently verified.
- Department labels are inferred navigation aids, not confirmed departmental assignments.
- Contact location hints may refer to overseas branches or group contacts. They do not establish a recipient's location.
- Flagged email addresses requiring attribution review remain visible in the contact details but are excluded from the main attributed-email totals.
- Blank contact fields mean no value was found in the collected pages. Published details may be outdated; email delivery and telephone reachability were not tested.
- The observation date records collection, not the company's last confirmation. The page does not refresh its data from the internet.

No emails were guessed, messages sent, forms submitted or private accounts accessed during collection.
