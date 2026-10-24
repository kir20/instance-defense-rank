# Instance Defense ranking data

Public data for the VRChat world **Instance Defense**: the server ranking board and the supporter board.

- `rank.json` is written automatically by the ranking server. It holds the TOP 10 by clear count and by talent level. Only VRChat display names and numbers are stored. There are no user IDs, timestamps per player, or connection data. The file is replaced by a single commit each time, so old names do not stay in the history.
- `supporters.txt` lists supporters, one VRChat display name per line. Lines starting with `#` are notes. Only add names of people who agreed to be listed.

Players are sent to the ranking only when they have enabled "Allow Untrusted URLs" in VRChat, and the world shows a notice about it.

Written with Claude (Anthropic).
