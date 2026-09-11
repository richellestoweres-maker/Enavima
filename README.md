# Enavima

Website for **Enavima**, the congenital CMV (cCMV) point-of-care testing program of
[Microgen Laboratories](https://microgenlabs.com), La Marque, Texas.

Seven static pages. No build step, no dependencies, no framework. Every page is a single
self-contained HTML file with its CSS inlined, so you can open any of them by double-clicking.

---

## Pages

| File | Page |
|---|---|
| `index.html` | Home |
| `congenital-cmv.html` | About congenital CMV, the education hub |
| `parents.html` | For parents and expecting families |
| `clinicians.html` | For clinicians |
| `labs.html` | For hospitals and laboratories, plus the evaluation request form |
| `test.html` | The Enavima point-of-care test |
| `about.html` | About, team, collaborators, contact |

## Brand

| Color | Hex | Where it is used |
|---|---|---|
| Enavima blue | `#2395D3` | Large numbers, rules, callout borders, graphics |
| Enavima purple | `#73519D` | Section labels, the timeline day markers |
| Working blue | `#1A73A6` | Buttons and links, dark enough for white text and small type |
| Deep brand | `#1E1633` | Footer and the dark sections |

The first two are the exact colors in the logo. The working blue is the same blue
darkened just enough that white button text and small link text stay readable, which the
lighter logo blue is not at small sizes. All four are defined once at the top of every
page, in the `:root` block, so a color change is one line per file.

Logo files live in `assets/`:

| File | Use |
|---|---|
| `enavima-logo.png` | Header, on light backgrounds |
| `enavima-logo-white.png` | Footer and any dark background |
| `microgen-logo.png` / `microgen-logo-white.png` | Parent company mark |
| `favicon.png`, `apple-touch-icon.png` | Browser tab and phone home screen |
| `og-image.png` | The preview card shown when a link is shared |

## Editing the site

**Changing wording?** See **[EDITINGGUIDE.md](EDITINGGUIDE.md)**, written for non-developers,
with no software to install.

**Changing the design?** The `<style>` block near the top of each file is identical across all
seven pages, so a design change means making the same edit seven times.

## Publishing with GitHub Pages

1. **Settings**, then **Pages**
2. Source: **Deploy from a branch**, branch **main**, folder **/ (root)**
3. Save. The site appears at `https://<username>.github.io/<repo>/` within a minute or two.

GitHub Pages is free on **public** repositories. On a private repository it requires a paid plan.

When the real domain is purchased: add a file named `CNAME` at the root containing just the
domain (for example `enavima.com`), point the domain's DNS at GitHub Pages, and tick
**Enforce HTTPS** in Settings, then Pages.

The `.nojekyll` file tells GitHub Pages to serve these files exactly as written. Leave it there.

---

## Open items before launch

1. **Regulatory wording.** The footer of every page, and `test.html`, state that Enavima assays
   are in development, are not available for sale, and have not been cleared or approved by the
   FDA. Dr. Kommineni (QA/RA) should confirm this is the exact language Microgen wants.

2. **No performance claims appear anywhere.** No sensitivity, specificity or limit-of-detection
   figures. The site says these are available on request under confidentiality. Add real numbers
   only once they are cleared for publication.

3. **The two contact forms use `mailto:` links**, which open the visitor's email program and do
   not always work. Before launch, replace them with a real form service such as Formspree or
   Netlify Forms.

4. **The `noindex` tag.** Every page carries `<meta name="robots" content="noindex, nofollow">`
   so the temporary URL stays out of Google. Delete that line from all seven files on the day
   the real domain goes live.

## Sources for every statistic on the site

- [CDC, About CMV and Congenital CMV Infection](https://www.cdc.gov/cytomegalovirus/about/index.html)
- [CDC, Clinical Overview of Congenital CMV Infection](https://www.cdc.gov/cytomegalovirus/hcp/clinical-overview/index.html)
- [AAP, Congenital Cytomegalovirus (cCMV)](https://www.aap.org/en/patient-care/congenital-cytomegalovirus-ccmv/)
- [Minnesota Department of Health, CMV](https://www.health.state.mn.us/diseases/cytomegalovirus/index.html) (the Vivian Act, universal screening from 6 February 2023)
- [AAO-HNS, State cCMV Laws](https://www.entnet.org/resource/state-ccmv-laws/), 2 universal, 13 hearing-targeted, 8 education
- [microgenlabs.com](https://microgenlabs.com), products, team, funded research

**State screening laws change often.** Re-check the AAO-HNS tracker before launch, and every few
months afterwards. The counts appear on `index.html` and `labs.html`.
