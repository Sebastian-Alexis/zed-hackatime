# zed-hackatime

A [WakaTime](https://wakatime.com/) extension for [Zed](https://zed.dev/), modified to support [Hackatime](https://github.com/hackclub/hackatime).

Uses the [wakatime-ls](https://github.com/wakatime/zed-wakatime/tree/master/wakatime-ls) to receive edit events from Zed and send heartbeats to WakaTime/Hackatime by [wakatime-cli](https://github.com/wakatime/wakatime-cli).

## Installation

1. Clone this repository:
```bash
git clone https://github.com/Sebastian-Alexis/zed-hackatime.git
```

2. Install the extension in Zed:
   - Open Zed
   - Open the command palette (Cmd+Shift+P on macOS)
   - Run "zed: install dev extension"
   - Select the cloned `zed-hackatime` directory
   - Zed will automatically build and install the extension

## Configuration
In order to authenticate with the wakatime-cli, the language server needs to know your API token.
Here are two ways to set the lsp.

### WakaTime configuration file
create a file named `.wakatime.cfg`, locate your HOME directory.
```toml
[settings]
api_key = Your api key
```

### zed setting file
Zed setting.Open zed setting file, add your api key
```json
"lsp": {
  "wakatime": {
    "initialization_options": {
      "api-key": "You api key"
    }
  }
}
```

## Note
This plugin has been thoroughly tested only on macOS. If you encounter any issues on other systems, please submit an issue or a pull request.
