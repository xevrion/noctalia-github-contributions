# GitHub Contributions

Displays your GitHub contribution graph as a desktop widget, themed with your Noctalia colors.

![preview](preview.png)

## Data Sources

| Mode | API Key | Coverage |
|------|---------|----------|
| **Public profile** (default) | Not required | Public contributions (plus private if enabled in your GitHub profile settings) |
| **GraphQL API** | Personal access token | Exact counts including private contributions |

- Without a token, the widget reads the contribution calendar from your public GitHub profile.
- With a token (create one at [github.com/settings/tokens](https://github.com/settings/tokens) with `read:user` scope), data comes from the GraphQL API.

## Features

**Desktop Widget**
- Contribution heatmap colored with the active Noctalia accent
- Total contributions and current streak
- Month and weekday labels
- Today's contribution count next to the username
- Hover a cell to see that day's contribution count (needs Noctalia >= 4.7.2, where desktop widgets accept mouse input)

**Settings**
- GitHub username
- Optional personal access token
- Weeks shown (4-53)
- Refresh interval (15-360 minutes)
- Toggles for totals and labels

**IPC**
- Refresh: `qs -c noctalia-shell ipc call plugin:github-contributions refresh`

## Installation

From the Noctalia plugin browser: Settings → Plugins, search for "GitHub Contributions" and install.

Manual install:

```bash
git clone https://github.com/xevrion/noctalia-github-contributions ~/.config/noctalia/plugins/github-contributions
```

Then enable the plugin in Settings → Plugins, and add the widget in Settings → Desktop Widgets.

## License

MIT
