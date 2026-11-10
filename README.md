# Library of Congress (loc.gov) API — Postman Collection

A Postman (v2.1) collection for the **[loc.gov JSON/YAML API](https://www.loc.gov/apis/json-and-yaml/)** (19 requests). It includes **Chronicling America**, the historic US newspapers from 1756–1963 with full text. Since 2025 Chronicling America is only available through loc.gov, and the old chroniclingamerica.loc.gov API has been retired. The collection also covers Sanborn fire-insurance maps, photos, maps, manuscripts, digitized books, and Library of Congress name headings (id.loc.gov).

**Import link** (Postman → Import → Link):
```
https://raw.githubusercontent.com/mikeyeves/Library-of-Congress-API-Postman/main/Library_of_Congress_API.postman_collection.json
```
No key and no environment file are needed. Settings are in the collection's **Variables** tab.

## ⚠️ Rate limit
The JSON API allows **20 requests per minute**. If you go over, you're **blocked for 1 hour**. Under heavy load you may also get a 429 error or a CAPTCHA page; the collection warns you in the Postman console when that happens. Use the Collection Runner with a delay of at least 3 seconds.

## Folders
| Folder | Requests |
|---|---|
| ★ Chronicling America (newspapers) | 7 |
| Core loc.gov endpoints | 6 |
| Other genealogy-useful collections | 6 |

Search requests show results in a **Visualizer** table with title, date, newspaper, location and format.

## Useful parameters
| Param | Meaning |
|---|---|
| `q` | Keyword search, including newspaper OCR text |
| `dates` | Date range, `YYYY/YYYY` |
| `fa` | Facet filter `name:value`, joined with `\|`, e.g. `location_state:new york`, `location_city:...`, `partof_title:...`, `subject_ethnicity:...` |
| `dl=page` | Return one result per newspaper page (Chronicling America) |
| `c`, `sp` | Results per page; page number |
| `sb` | Sort, e.g. `date` or `date_desc` |
| `at` / `at!` | Return only, or exclude, certain parts of the response |
| `fo` | `json` or `yaml` |

## Tested at build time
- `Bukovsky` matched 982 Chronicling America pages, mostly from Maryland and Ohio papers between the 1910s and 1950s.
- The facet, date and state filters all work.

## Related collections
[WikiTree](https://github.com/mikeyeves/WikiTree-API-Postman) · [FamilySearch](https://github.com/mikeyeves/FamilySearch-API-Postman) · [NYC Historical Vital Records](https://github.com/mikeyeves/NYC-Historical-Vital-Records-Postman) · [Unified Census ED Finder](https://github.com/mikeyeves/Unified-Census-ED-Finder-Postman) · [UK & Ireland Archives](https://github.com/mikeyeves/UK-Ireland-Archives-APIs-Postman) · [European Archives](https://github.com/mikeyeves/European-Archives-APIs-Postman)

*Unofficial. Not affiliated with the Library of Congress. Built from the public API documentation.*
