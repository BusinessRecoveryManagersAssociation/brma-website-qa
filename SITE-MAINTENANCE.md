# BRMA Website Maintenance Guide

This repository is the QA version of the BRMA website. Routine website maintenance should be performed through ChatGPT/Codex, with GitHub acting as the source of truth.

## Required workflow

1. Make requested changes in the QA repository first.
2. Wait for the GitHub Pages deployment to complete.
3. Verify the published QA result as far as available tools allow.
4. Do not report a change as "fixed," "live," or "working" merely because a commit succeeded.
5. Do not update the production site until the user explicitly approves the QA result for publication.

## Fast-path rules

Use the fastest safe path for routine website changes.

1. Treat a clear user request as authorization to make that specific QA change. Do not ask for confirmation again unless an ambiguity would materially change the result.
2. Read only the files directly needed for the requested change. Do not inspect unrelated files, pages, or external websites unless they are necessary.
3. Batch related HTML, CSS, JavaScript, and asset changes into as few commits as practical so one user request does not trigger unnecessary deployments.
4. For simple text, link, spacing, styling, or layout edits, make the repository change immediately. Do not wait for a Pages deployment before responding; say that the repository change is complete and that deployment is processing if it has not finished.
5. Only say a change is "live," "fixed," or "working" after the GitHub Pages deployment succeeds and the published result has been verified as far as available tools allow.
6. Do not repeatedly poll GitHub Pages while a deployment is still processing. Check once after the change; if it is still running, report that status and move on.
7. Reuse the known repository structure and current project decisions from the same working session. Do not rediscover information that is already known unless there is evidence it may have changed.
8. Make only the requested change. Do not add enhancements, cleanup, refactors, or troubleshooting that the user did not request.

## Image and binary file updates

When a user uploads an image or other binary asset:

1. Use the exact uploaded file as the source.
2. Do not recreate it, manually re-encode it, substitute another version, or use a guessed URL.
3. Upload the exact binary file to the repository.
4. Verify that the repository file matches the uploaded source before troubleshooting anything else.
5. Update the site code to reference the repository asset.
6. Do not search BRMA.com or another external site for an uploaded asset unless the user specifically asks.
7. Avoid resizing, converting, or otherwise modifying an uploaded asset unless required for the site or explicitly requested.
8. If the asset and page update can be committed together, do so to avoid multiple Pages builds.
9. Verify the published asset/site before reporting the change as live.

Never troubleshoot paths, CSS, caching, or layout until first confirming that the correct source file was actually uploaded.

## Scope discipline

Follow the user's requested scope exactly.

If the user asks to inspect one URL, file, image, or page element, inspect that item first and do not branch into unrelated troubleshooting or repository changes unless they are necessary to complete the requested task.

## Maintenance goal

Board members should be able to maintain the site by describing the desired change in plain language. Routine users should not need to understand GitHub, Jekyll, repository paths, branches, or deployment mechanics.
