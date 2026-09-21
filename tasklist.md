# Cyberbiosecurity Wiki Task List

## Goal

Create and publish a Quartz-based wiki on GitHub with the title `Cyberbiosecurity`.

## Phase 1: Repository and hosting setup

- [ ] Confirm whether `https://github.com/grebbel/quartz` is the intended repository or a template to fork.
- [ ] Decide whether the GitHub repository should be renamed from `quartz` to `cyberbiosecurity`.
- [x] Connect this workspace to `https://github.com/grebbel/quartz` as `origin`.
- [x] Confirm the deployment method: the existing Cloudflare Pages workflow is configured for `main`.
- [x] Verify that the site builds locally with `npx quartz build -d docs -v`.

Phase 1 setup is complete. Repository ownership and the final public URL still need to be confirmed before publishing. The full `npm run check` now passes: TypeScript validation and Prettier checks are successful, and the Quartz build passes.

## Phase 2: Wiki structure and content

- [x] Define the initial page structure for the wiki:
  - [x] Home and project overview
  - [x] Definition of cyberbiosecurity
  - [x] Scope and key concepts
  - [x] Relevant sectors
  - [x] Target audiences
  - [x] Assessment tool and other outputs
  - [x] Bibliography
- [ ] Review the Zotero folder `CyberBioSecurity` and identify the literature to include.
- [ ] Export or convert the selected literature into Markdown pages or references suitable for Quartz.
- [x] Add consistent metadata and tags to the initial project pages.
- [x] Add an initial bibliography with DOI links and local source references.
- [x] Mark initial gaps for further research, including definitions and applicable standards such as ISO guidance.

Phase 2 initial content is complete. The wiki now has a project homepage, five linked topic pages, and a four-source bibliography. The Zotero collection still needs to be reviewed and incorporated.

## Phase 3: Review and publication

- [x] Check links, navigation, spelling, and page titles. The Quartz production build passes without broken-link errors.
- [x] Confirm that the initial content is appropriate for the intended audiences, including laboratory management and biosafety officers.
- [x] Check that no restricted or confidential material from the available source set is published unintentionally. Source PDFs remain outside `docs`.
- [ ] Publish the wiki.
- [ ] Open the deployed site and confirm that the main pages and literature links work.
- [ ] Record the final public URL here:

Local release checks pass. Publication is pending confirmation that `https://github.com/grebbel/quartz` is the intended repository and configuration of the required Cloudflare Pages secrets.

## Completion criteria

The task is complete when the selected repository is connected, the wiki builds successfully, the agreed literature is available with citations, and the published URL has been tested and recorded above.
