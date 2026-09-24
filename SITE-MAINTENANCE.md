# BRMA Website Maintenance Guide

This repository is the QA version of the BRMA website. Routine website maintenance should be performed through ChatGPT/Codex, with GitHub acting as the source of truth.

## Required workflow

1. Make requested changes in the QA repository first.
2. Wait for the GitHub Pages deployment to complete.
3. Verify the published QA result as far as available tools allow.
4. Do not report a change as "fixed," "live," or "working" merely because a commit succeeded.
5. Do not update the production site until the user explicitly approves the QA result for publication.

## Image and binary file updates

When a user uploads an image or other binary asset:

1. Use the exact uploaded file as the source.
2. Do not recreate it, manually re-encode it, substitute another version, or use a guessed URL.
3. Upload the exact binary file to the repository.
4. Verify that the repository file matches the uploaded source before troubleshooting anything else.
5. Update the site code to reference the repository asset.
6. Wait for the QA deployment to complete successfully.
7. Verify the published asset/site before reporting the change as complete.

Never troubleshoot paths, CSS, caching, or layout until first confirming that the correct source file was actually uploaded.

## Scope discipline

Follow the user's requested scope exactly.

If the user asks to inspect one URL, file, image, or page element, inspect that item first and do not branch into unrelated troubleshooting or repository changes unless they are necessary to complete the requested task.

## Maintenance goal

Board members should be able to maintain the site by describing the desired change in plain language. Routine users should not need to understand GitHub, Jekyll, repository paths, branches, or deployment mechanics.
