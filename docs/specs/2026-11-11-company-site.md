# The apps done well — company website brief

Date: 2026-11-11.
Status: Tickets published; website implementation has not started.

## Goal

Remake the website as the company home of **The apps done well**, with **Sheet Change Detector** as its first product. The identity must accommodate more useful apps, including future Chrome extensions, without inventing a catalogue that does not exist.

The user explicitly requested `grill-with-docs` and `frontend-design`. The latest instruction is: "once all has been recorded, @to-tickets". Prepare and approve tickets before implementation; the desired delivery includes deployment after verification.

## Recorded interview decisions

1. **Company scope:** useful apps generally; Chrome extensions are the starting point, not the permanent boundary.
2. **Hierarchy:** company-first homepage, with the extension's full details on its own product page.
3. **Personality:** a careful maker — clear, practical, quietly confident; not a fictional large company.
4. **Evidence:** demonstration first, supported by a short statement of approach. Show a real product problem rather than unsupported claims.
5. **Family:** one recognizable company identity, with small product-specific accents.
6. **Product name:** keep **Sheet Change Detector**; identify **The apps done well** as publisher.
7. **Scope:** marketing website with sample demonstrations and product links. No accounts, checkout, or live spreadsheet uploads.
8. **Language:** English only for this version; no language switcher or translation project.
9. **Delivery:** build and deploy, rather than stopping at a local preview.
10. **Launch copy:** the user asked, "Publish it as if the extension was ready, I will provide you the link later (create a human task for it)". Use polished capability-forward copy, not "coming soon" messaging.
11. **Pricing ownership:** per product, not a company-wide subscription or invented future bundle.
12. **Pending installation:** the user accepted a visibly inactive install action until the real store URL is supplied. Do not publish a fake or unverified install link, or claim verified store availability.
13. **Next step:** record this understanding and turn it into tickets; do not treat the recording request as approval to start coding.

## Pages and visitor journeys

- `/`: company identity first, then the real first product and a concrete sample of its value. No empty product cards or fictional future releases.
- `/apps/sheet-change-detector/`: dedicated product explanation, demonstration, workflow, capabilities, and product-specific pricing.
- Keep the existing public privacy and terms routes working. Preserve the published legal files exactly.
- A visitor can understand the company, discover the product, read its details, examine sample data, and find support without encountering a broken route.
- The install action stays inactive until its official destination is supplied and verified. Other company/product navigation remains usable.
- A sample demonstration must be identified as sample data. It is not a hosted version of the extension and must not request spreadsheet access or accept uploads.

## Frontend-design direction

The designer proposed **A good fit**: an identity grounded in useful apps and careful construction rather than spreadsheet imagery as the company brand.

Proposed compact palette:

- Paper `#F6F8FA`: page background.
- Ink `#172C32`: primary text.
- Slate `#52636B`: secondary text.
- Tool blue `#2457C5`: links, focus, and primary actions.
- Mist `#E7EDF0`: quiet demonstration surfaces.

Proposed typography: **Bricolage Grotesque** for the company name/headings and **Source Sans 3** for body/navigation/controls. Use an intentional scale, roughly 48–64 px page titles, 32–40 px section headings, 24 px subheadings, 18 px body, and 14 px supporting text, adapted responsively. Body lines should stay around 60–70 characters.

Use one restrained fitted-corner/square gesture to suggest careful construction. A static version must work fully. Keep the rest quiet and left aligned; do not repeat the gesture as decoration everywhere.

The company owns the introduction; the product earns attention through a concrete demonstration. Keep comparison grids and change colors inside product demonstrations, not as the entire company identity.

Before coding, the designer must review this token/layout plan against the brief, reject generic defaults, and record any deliberate refinement. This is a direction, not permission to preserve weak copy or ship unverified assets. Keep the exact spaced product name **Sheet Change Detector**.

Avoid generic card grids, invented testimonials, user counts, awards, claims of company size, decorative uppercase eyebrows, and unnecessary motion. Respect reduced motion, keyboard focus, readable contrast, and small screens.

## Product information and installation

Keep product-specific pricing consistent with the existing offering: Free at €0; Pro at €9.99/year or €1.99/month. Twelve monthly payments total €23.88; the annual saving is €13.89. Do not create checkout, a new billing model, or a company-wide subscription.

Existing Free limits are 5 comparisons/day, up to 1,000 cells, and the first 25 differences listed. Existing Pro limits are unlimited comparisons, up to 10,000 cells, and 250 differences listed. Confirm product wording against the source before publishing; do not embellish trial claims.

The existing ten Pro capabilities are highlight Apply, CSV export, merge review, fuzzy matching, number tolerances, composite keys, saved presets, comparison history, scheduled comparisons, and side-by-side rows. Preserve accurate distinctions; do not imply all features are free or that every product shares these plans.

Human task **#145**: https://github.com/strinkrf851none/373-sheets-diff/issues/145 — provide the actual public Chrome Web Store URL, verify the product listing, and activate installation. This task may start immediately and **does not block publishing** the company website with installation inactive.

The currently hard-coded store URL is not verified as an available listing. A public fetch redirected to an `empty-title` shell, returned a generic Chrome Web Store title, and did not identify the product. HTTP 200 alone is not proof. Do not infer a public destination from the local extension ID.

## Repository and deployment facts

- Site repository: `theappsdonewell/theappsdonewell.github.io`.
- Local checkout: `/home/usuario/opencode-projects/theappsdonewell-site`.
- Public URL: https://theappsdonewell.github.io/.
- At recording, local `site/redesign` is clean at `a9e1645aba1a45a00d5df7a25f2e6b259c81c3b0`; deployed `main` is `7ce9724d852b6d35f0570b05709298b8b6d44715`.
- GitHub Pages uses a legacy branch build from `main:/`. Its generated `pages-build-deployment` workflow is the only workflow. Extension verification does not gate this site's publication.
- The site is static HTML/CSS with no existing package/build system. Preserve the no-framework/no-build deployment model; small local demonstration behavior is allowed.
- Existing other routes/assets include `app-ads.txt` and the Google verification file; preserve them.
- No other product content was found. Do not introduce placeholders for products that do not exist.
- Existing locally served fonts are Public Sans and Fragment Mono, but their licenses are absent from the repository. Verify and include the license for every shipped font; self-host assets rather than adding a font CDN.
- Restore/preserve the legal files from deployed `main`, not the markup-modified copies on `site/redesign`. Exact deployed SHA-256: privacy `5b5fe9156700e4836d13b2458c4bec3d41bce6b37a0d47cbd04323daefa40bd6`; terms `adbc62af460941c733cb590f835ea91712a52c6f22ef4f59f267bcbefde355b3`.
- Public robots/sitemap currently return 404; the existing redesign contains versions. Publish correct company/product URLs, absolute canonicals, and updated discovery metadata.

The earlier exploration incorrectly attributed extension CI to this site and claimed legal-file identity and store proof. Those claims are rejected. Authoritative raw API/source evidence is in the extension checkout's `.local/verification/2026-11-11-website-recon/`; the facts and legal hashes needed for implementation are recorded here.

## Acceptance and verification

- Company-first identity and a working, separately addressable product page.
- The exact publisher/product distinction in the glossary is reflected in navigation, headings, metadata, and copy.
- Only real products; no fake metrics, testimonials, availability claims, or active unverified installation links.
- A coherent family identity and a real, clearly identified sample comparison; no accounts, checkout, or uploads.
- Correct product-specific pricing/limits and a visible pending installation state linked operationally to #145.
- Working navigation, contact and legal routes; no placeholder `#` install destinations.
- Responsive browser checks at 375, 768, 1280, and 1920 px on both main journeys, with keyboard operation, focus, reduced motion, contrast checks, and no horizontal overflow.
- Retained screenshots and focused accessibility/performance evidence. Fix material defects; do not claim scores that were not measured.
- Legal-file hashes equal deployed main; font licenses and existing verification/advertising assets are preserved.
- Verify the built branch locally before any public push. After deployment, verify the Pages build commit and actual public routes/assets/content; do not equate a push with successful publication.

## Boundaries and related work

- This request replaces the old product-only homepage direction in related extension-tracker issue #133. Preserve relevant correctness/performance constraints, not its obsolete company hierarchy.
- Related #134 pricing requirements remain product-specific. Do not invent shared pricing because the company can publish more apps.
- Do not close or modify existing parent/related issues as part of ticket creation. The new tickets come from this recorded conversation.
- Do not refactor the extension or treat website work as completion of extension PR #144.
- PR #144 remains draft/unmerged. Its last full-gate attempt at `00292bb` failed because archived source/test copies under `.local` were discovered as test suites: 1,409 actual tests passed, nine archived suites failed import resolution, and later build/smoke/E2E stages were not reached. That is not site verification or evidence of a released extension.
- No new ADR is needed for reversible visual choices. Record the domain terms in `GLOSSARY.md` and keep this brief as the implementation source.

## Approved ticket graph

1. **site: company-first homepage and first-product discovery** — [GitHub issue #146](https://github.com/strinkrf851none/373-sheets-diff/issues/146) — no native blockers. A complete company-first homepage and functioning minimum product overview, shared identity, legal/support navigation, and a concrete sample illustration.
2. **site: complete the Sheet Change Detector product journey** — [GitHub issue #147](https://github.com/strinkrf851none/373-sheets-diff/issues/147) — native blocker: #146. A full product page, sample demonstration, workflow, accurate product-specific plans/capabilities, and safe inactive installation handoff.
3. **site: verify and publish the company and product website** — [GitHub issue #148](https://github.com/strinkrf851none/373-sheets-diff/issues/148) — native blocker: #147 (#146 transitively). Browser/accessibility/performance/legal/link verification, publication through Pages, and live post-deploy proof.
4. Existing **human #145** — can start immediately; supplies the official store URL and activates installation. It does not gate website publication.

The user approved this granularity and dependency structure on 2026-11-11. The three tickets were published on 2026-11-11 as #146, #147, and #148 with native dependencies #147 blocked by #146 and #148 blocked by #147. Human task #145 remains independent and does not gate publication.
