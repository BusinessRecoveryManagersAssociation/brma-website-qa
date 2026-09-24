# BRMA Website Agent Instructions

These rules are mandatory for all maintenance work in this repository.

## Operating model

BRMA board members maintain the website by describing changes in plain language. The agent performs the implementation directly in the QA repository. Routine users must not be asked to edit GitHub, paste code, rename files, create folders, run commands, or understand repository mechanics when connected tools can perform the work.

## Mandatory preflight

Before responding to any request to change the BRMA website:

1. Read and follow `SITE-MAINTENANCE.md`.
2. Treat a clear request to add, update, remove, or change something as authorization to execute that QA change.
3. Check the currently available GitHub/file tools before saying a requested change cannot be done directly.
4. If the same kind of task was completed directly earlier in this project, reuse that established workflow.
5. Do not substitute implementation instructions for execution when execution is available.

## Uploaded images and binary assets

When the user supplies an image or other binary file:

1. Use the exact uploaded file.
2. Upload it directly to the repository.
3. Reuse the established binary-asset workflow already used for BRMA leadership and hero images.
4. Update the page to reference the repository asset.
5. Do not ask the user to paste code or manually upload the asset to GitHub.
6. Do not claim GitHub write access is unavailable until the available GitHub tools have actually been checked.

## Scope

Make only the requested change unless another change is technically required for it to work. Do not add unrelated improvements, research, cleanup, or redesign.

## QA and publication

Make changes in QA first. A successful commit is not the same as a successful deployment. Do not call a change live or working until the deployment succeeds and the published result is verified as far as available tools allow. Production changes require explicit user approval.
