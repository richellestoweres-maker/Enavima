# Enavima

Website for **Enavima** — the congenital CMV (cCMV) point-of-care testing program of
[Microgen Laboratories](https://microgenlabs.com), La Marque, Texas.

Seven static pages. No build step, no dependencies, no framework. Every page is a single
self-contained HTML file with its CSS inlined, so you can open any of them by double-clicking.

---

## Pages

| File | Page |
|---|---|
| `index.html` | Home |
| `congenital-cmv.html` | About congenital CMV — the education hub |
| `parents.html` | For parents & expecting families |
| `clinicians.html` | For clinicians |
| `labs.html` | For hospitals & laboratories, plus the evaluation request form |
| `test.html` | The Enavima point-of-care test |
| `about.html` | About, team, collaborators, contact |

## Editing the site

**Changing wording?** See **[EDITING-GUIDE.md](EDITING-GUIDE.md)** — written for non-developers,
no software to install.

**Changing the design?** The `<style>` block near the top of each file is identical across all
seven pages. A design change means making the same edit seven times, or regenerating the set
from the source templates.

## Publishing with GitHub Pages

1. **Settings** → **Pages**
2. Source: **Deploy from a branch**, branch **main**, folder **/ (root)**
3. Save. The site appears at `https://<username>.github.io/<repo>/` within a minute or two.

GitHub Pages is free on **public** repositories. On a private repository it requires a paid plan.

When the real domain is purchased: add a file named `CNAME` at the root containing just the
domain (e.g. `enavima.com`), then point the domain's DNS at GitHub Pages and tick
**Enforce HTTPS** in Settings → Pages.

The `.nojekyll` file tells GitHub Pages to serve these files exactly as written. Leave it there.

---

## Before this goes live — three things to confirm

1. **Regulatory wording.** The footer of every page, and `test.html`, state that Enavima assays
   are in development, are not available for sale, and have not been cleared or approved by the
   FDA. **Dr. Kommineni (QA/RA) should confirm this is the exact language Microgen wants.**

2. **No performance claims appear anywhere.** No sensitivity, specificity or limit-of-detection
   figures. The site says these are available on request under confidentiality. Add real numbers
   only once they are cleared for publication.

3. **The two contact forms use `mailto:` links**, which open the visitor's email program and do
   not always work. Before launch, replace them with a real form service — Formspree, Netlify
   Forms, or whatever the host provides.

## Sources for every statistic on the site

- [CDC — About CMV and Congenital CMV Infection](https://www.cdc.gov/cytomegalovirus/about/index.html)
- [CDC — Clinical Overview of Congenital CMV Infection](https://www.cdc.gov/cytomegalovirus/hcp/clinical-overview/index.html)
- [AAP — Congenital Cytomegalovirus (cCMV)](https://www.aap.org/en/patient-care/congenital-cytomegalovirus-ccmv/)
- [Minnesota Department of Health — CMV](https://www.health.state.mn.us/diseases/cytomegalovirus/index.html) (the Vivian Act; universal screening from 6 February 2023)
- [AAO–HNS — State cCMV Laws](https://www.entnet.org/resource/state-ccmv-laws/) — 2 universal / 13 hearing-targeted / 8 education
- [microgenlabs.com](https://microgenlabs.com) — products, team, funded research

**State screening laws change often.** Re-check the AAO–HNS tracker before launch, and every few
months afterwards. The counts appear on `index.html` and `labs.html`.
