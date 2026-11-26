# Taking in NVIDIA's updates

This repository is a fork of https://github.com/NVIDIA/auto-ontology. NVIDIA ships often, so the
fork is kept close to it: our changes stay small and on the surface (branding first), and internal
names are left alone so upstream changes merge without conflicts.

```bash
git remote add upstream https://github.com/NVIDIA/auto-ontology.git   # once
git fetch upstream
git checkout -b upstream-sync origin/main
git merge upstream/main          # never rebase main: it is shared
# Conflicts are usually in files listed in NOTICE-CUBRIX.md. Keep NVIDIA's change and
# re-apply ours (for colors, use the --color-brand variables, not hex values).
```

After a merge:

1. Search for anything new that brings NVIDIA branding back into the UI:
   `grep -rIn -i "76b900\|NvidiaLogo\|Auto Ontology" frontend/app frontend/components frontend/common --include=*.tsx`
   (comments are fine; visible text should say Cubrix Ontology).
2. Note the new upstream commit in NOTICE-CUBRIX.md under "Based on upstream commit".
3. Open a pull request so the merge is reviewed like any other change.

Things to know about upstream (as of 2aec701): it does not accept outside contributions, so fixes we
want upstream can only be reported as issues; its ingestion endpoints have no authentication, so
never expose ports 3001 and 3002.
