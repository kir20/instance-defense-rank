# Instance Defense ranking data

Public data for the VRChat world **Instance Defense**: the server ranking board and the supporter board.

- `rank.json` is built automatically every 10 minutes by the `pages` workflow from the ranking server. It holds the TOP 10 by clear count and by talent level. Only VRChat display names and numbers are stored. There are no user IDs, timestamps per player, or connection data. It is deployed straight to GitHub Pages and never committed, so names do not stay in the git history. The `rank.json` in the repository is only an empty fallback.
- `supporters.txt` lists supporters, one VRChat display name per line. Lines starting with `#` are notes. Only add names of people who agreed to be listed. The list lives in the private repository variable `SUPPORTERS` and is deployed straight to GitHub Pages, never committed, so a removed name does not stay in the git history. To update it, edit the variable (Settings → Secrets and variables → Actions → Variables, or `gh variable set SUPPORTERS -R kir20/instance-defense-rank < list.txt`) and run the `pages` workflow (`gh workflow run pages -R kir20/instance-defense-rank`); the next scheduled run also picks it up.

Players are sent to the ranking only when they have enabled "Allow Untrusted URLs" in VRChat, and the world shows a notice about it.

Written with Claude (Anthropic).
