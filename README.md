# Project-Aertic
Remote control submarine project.
🛠 SolidWorks CAD Collaboration Guidelines

This repository is used to store and collaborate on SolidWorks CAD files. Because CAD files are binary and cannot be merged like code, the following rules must be followed to avoid broken references or lost work.

📦 Git LFS (Required)

This repository uses Git Large File Storage (LFS) for CAD files.

Before working on this repo:

Install Git LFS: https://git-lfs.com/

Run:

git lfs install


Pull the repository normally.

Tracked file types include:

.SLDPRT

.SLDASM

.SLDDRW

.STEP

.STL

📁 Folder Structure

Do not change the folder structure without team approval.

Parts/        → Individual SolidWorks parts (.SLDPRT)
Assemblies/   → SolidWorks assemblies (.SLDASM)
Drawings/     → Engineering drawings (.SLDDRW)
STEP_Exports/ → Neutral CAD exports
STL_Exports/  → Manufacturing / 3D print files
Docs/         → Documentation and notes


⚠ Important: SolidWorks relies on relative file paths. Moving or renaming files can break assemblies.

👤 File Ownership Rule (Critical)

Only ONE person may edit a CAD file at a time

CAD files cannot be merged

Always coordinate before editing shared assemblies

If you need to modify a file:

Confirm nobody else is working on it

Lock the file using Git LFS

git lfs lock path/to/file.SLDPRT


Make your changes

Commit and push

Unlock the file

git lfs unlock path/to/file.SLDPRT

🌿 Branching Workflow

main branch is stable

Create feature branches for changes

git checkout -b feature/your-feature-name


Examples:

feature/motor-mount

feature/chassis-update

Open a Pull Request when ready to merge.

🧩 Assemblies & References

Always keep all referenced files inside the repo

Use Pack and Go for new or major assemblies:

File → Pack and Go → Save to repository folder


Commit all referenced files together

✍️ Commit Messages

Use clear, descriptive messages:

Added motor mount part

Updated chassis hole pattern

Fixed assembly mate errors

Avoid vague messages like:

Update

Changes

Fix

📤 Exports for Review

When making significant design changes:

Export a .STEP file for easy viewing

Add it to STEP_Exports/

Commit alongside the SolidWorks file

🚫 What NOT To Do

❌ Do not edit the same file as someone else

❌ Do not force-push to main

❌ Do not rename or move files casually

❌ Do not commit temporary SolidWorks files

💬 Communication

Use GitHub Issues for design changes and discussions

Use Pull Requests for reviews

Communicate before touching shared assemblies
