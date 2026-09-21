# Cyberbiosecurity Wiki Task List

## Goal

Create and publish a Quartz-based wiki on GitHub with the title `Cyberbiosecurity`.

## Phase 1: Repository and hosting setup

- [x] Confirm that `https://github.com/grebbel/quartz` is the active repository for this project.
- [x] Confirm repository identity and hosting approach: the current repo is the project repo and the site is intended to use GitHub Pages.
- [x] Connect this workspace to `https://github.com/grebbel/quartz` as `origin`.
- [x] Confirm the deployment method: the repo contains a GitHub Pages workflow in `.github/workflows/deploy-v5.yaml`.
- [x] Verify that the site builds locally with `npx quartz build -d docs -v`.
- [ ] Enable GitHub Pages in the repository settings for the `grebbel/quartz` repo so the site publishes.
- [ ] Record the final public URL once GitHub Pages is enabled.

Phase 1 setup is complete from a build and configuration perspective. The code passes validation (`npm run check`) and the site builds successfully, but the live GitHub Pages site is not yet active because the repo's Pages settings are still not enabled. Remote verification currently returns `404` for `https://grebbel.github.io/quartz`.

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

Phase 2 initial content is complete. The wiki has a project homepage, linked topic pages, and a bibliography, but the Zotero-reading task still needs to be incorporated into the public site content.

## Phase 3: Review and publication

- [x] Check links, navigation, spelling, and page titles. The Quartz production build passes without broken-link errors.
- [x] Confirm that the initial content is appropriate for the intended audiences, including laboratory management and biosafety officers.
- [x] Check that no restricted or confidential material from the available source set is published unintentionally. Source PDFs remain outside `docs`.
- [ ] Publish the wiki after the GitHub Pages settings are enabled.
- [ ] Open the deployed site and confirm that the main pages and literature links work.
- [ ] Record the final public URL here: https://grebbel.github.io/quartz (currently returns `404` until GitHub Pages is enabled in the repository settings).

Local release checks pass, but publication is still blocked by the repository's Pages activation rather than by the site build itself.

## Completion criteria

The task is complete when the GitHub Pages site is enabled, the wiki builds successfully, the selected literature is available with citations, and the live public URL has been tested and recorded above.
