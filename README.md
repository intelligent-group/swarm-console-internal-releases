# Swarm Console — Release Feed (Internal Edition)

This repository hosts the auto-update feed for **internal editions** of Swarm Console.
The app checks the latest published release here and offers a one-click download when
a newer build is available (Settings → **Update Swarm**, or the app menu → **Check for Updates**).

Client editions use a separate feed (`intelligent-group/swarm-console-releases`) and are
not served from here.

This repo is public — deliberately, matching `swarm-console-releases` — because
`desktop/updater.js`'s update check is an unauthenticated GitHub API call with no
token. A private repo here would silently break internal auto-update the same way
a private client-releases repo would break the client feed.
