# BRMA Website Agent Instructions

These rules are mandatory for all maintenance work in this repository.

## Operating model

BRMA board members maintain the website by describing changes in plain language. The agent performs the implementation directly in the QA repository. Routine users must not be asked to edit GitHub, paste code, rename files, create folders, run commands, or understand repository mechanics when connected tools can perform the work.

## Hard execution rule

For any clear request to change the QA website, EXECUTE THE CHANGE before answering.

Do not answer with code, instructions, a patch, or a description of what the user should do unless direct execution has been positively ruled out after checking the available tools.

A failed tool call does not prove the task cannot be completed. Try the established workflow or another available repository/file tool before concluding that execution is blocked.

If this project has already completed the same class of task directly, that prior workflow is the default and must be reused.

## Mandatory preflight

Before responding to any request to change the BRMA website:

1. Read and follow `SITE-MAINTENANCE.md`.
2. Treat a clear request to add, update, remove, or change something as authorization to execute that QA change.
3. Check the currently available GitHub and file tools before saying a requested change cannot be done directly.
4. If the same kind of task was completed directly earlier in this project, reuse that established workflow.
5. Do not substitute implementation instructions for execution when execution is available.
6. Do not claim "I can't push to GitHub," "the write connector is unavailable," or equivalent unless the available tools have actually been inspected in the current turn and no supported write path exists.

## Uploaded images and binary assets

When the user supplies an image or other binary file:

1. Use the exact uploaded file.
2. Upload it directly to the repository.
3. Reuse the established binary-asset workflow already used for BRMA leadership and hero images.
4. Update the page to reference the repository asset.
5. Do not ask the user to paste code or manually upload the asset to GitHub.
6. Do not search an external website for a replacement asset unless the user specifically asks.
7. Do not claim GitHub write access is unavailable until the available GitHub and file tools have actually been checked.

### Established binary upload workflow

When a user uploads an image and GitHub text-file tools cannot accept raw binary directly:

1. Use the exact uploaded conversation file as the source.
2. Convert the exact bytes to base64 without altering the image.
3. Create a GitHub blob with `encoding: base64`.
4. Add that blob to the repository tree at the intended asset path.
5. Commit the tree to the QA branch.
6. Update the page markup to reference the new asset.
7. Reuse existing image-card CSS when applicable instead of creating unnecessary new styling.
8. Check the resulting Pages deployment once after the final change.

This workflow is already proven in this repository for Renuka Darbha, Shelly Munoz, and the homepage hero images. It must be treated as the default for future uploaded images.

## Scope

Make only the requested change unless another change is technically required for it to work. Do not add unrelated improvements, research, cleanup, or redesign.

## Production protection rule

All routine edits are made **only in the QA repository/site**.

The production repository/site must never be edited as part of normal maintenance.

Production may be changed only when the user gives an explicit publication instruction, such as:

- "Push this to production."
- "Publish QA to production."
- "Update production with QA."
- "Make production match QA."
- Equivalent clear language explicitly authorizing a production update.

When such approval is given, promote the approved QA state to production. Do not independently decide that a QA change is ready for production.

If the user does not explicitly authorize production, remain in QA only.

## QA and publication

Make changes in QA first. A successful commit is not the same as a successful deployment. Do not call a change live or working until the deployment succeeds and the published result is verified as far as available tools allow. Production changes require explicit user approval.

## Failure prevention

The following response pattern is prohibited when direct execution is available:

- telling the user to paste code
- telling the user to upload the file to GitHub manually
- telling the user to switch to Codex or another interface
- giving a patch instead of making the change
- claiming tools are unavailable without checking them first

The intended user experience is always:

**request change -> agent updates QA -> user reviews QA -> user approves production**
