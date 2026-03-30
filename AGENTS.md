# AGENTS.md — sleepyjoe-website

## Deployment note

Pushing changes to GitHub is **not sufficient** for this website.
There is also a live copy served directly from this machine.

Current live web root:
- `/opt/sleepyjoe-site`

Nginx points `sleepyjoe.ru` at that directory, so after website changes you should usually:
1. commit and push the repo
2. copy/deploy the updated site files to `/opt/sleepyjoe-site`
3. verify the expected files exist on disk (and ideally verify over HTTP too)

Do not assume a Git push automatically updates production.

Current observed deploy method on this machine:
- copy the relevant site files into `/opt/sleepyjoe-site`
- `rsync` was not available during the last deploy, so a plain copy method was used

When editing project landing pages or downloads, remember that the live site currently serves files directly from `/opt/sleepyjoe-site`.
