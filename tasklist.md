# Cyberbiosecurity Wiki Task List

## Goal

Create and publish a Quartz-based wiki on GitHub with the title `Cyberbiosecurity`.

## Phase 1: Repository and hosting setup

- [ ] Confirm whether `https://github.com/grebbel/quartz` is the intended repository or a template to fork.
- [ ] Decide whether the GitHub repository should be renamed from `quartz` to `cyberbiosecurity`.
- [x] Connect this workspace to `https://github.com/grebbel/quartz` as `origin`.
- [x] Confirm the deployment method: the existing Cloudflare Pages workflow is configured for `main`.
- [x] Verify that the site builds locally with `npx quartz build -d docs -v`.

Phase 1 setup is complete. Repository ownership and the final public URL still need to be confirmed before publishing. The full `npm run check` is currently blocked by Prettier errors in the existing guidance document and workspace file; TypeScript and the Quartz build pass.

## Phase 2: Wiki structure and content

- [ ] Define the initial page structure for the wiki:
  - [ ] Home and project overview
  - [ ] Definition of cyberbiosecurity
  - [ ] Scope and key concepts
  - [ ] Relevant sectors
  - [ ] Target audiences
  - [ ] Assessment tool and other outputs
  - [ ] Bibliography
- [ ] Review the Zotero folder `CyberBioSecurity` and identify the literature to include.
- [ ] Export or convert the selected literature into Markdown pages or references suitable for Quartz.
- [ ] Add consistent metadata, tags, authors, dates, and source links to each literature page.
- [ ] Add citations and a bibliography to the relevant wiki pages.
- [ ] Mark gaps that require further research, including definitions and applicable standards such as ISO guidance.

## Phase 3: Review and publication

- [ ] Check links, navigation, spelling, and page titles.
- [ ] Confirm that the content is appropriate for the intended audiences, including laboratory management and biosafety officers.
- [ ] Check that no restricted or confidential material from the Zotero collection is published unintentionally.
- [ ] Publish the wiki.
- [ ] Open the deployed site and confirm that the main pages and literature links work.
- [ ] Record the final public URL here:

## Completion criteria

The task is complete when the selected repository is connected, the wiki builds successfully, the agreed literature is available with citations, and the published URL has been tested and recorded above.
