# zed-hackatime

A [WakaTime](https://wakatime.com/) extension for [Zed](https://zed.dev/), modified to support [Hackatime](https://github.com/hackclub/hackatime).

Uses the [wakatime-ls](https://github.com/wakatime/zed-wakatime/tree/master/wakatime-ls) to receive edit events from Zed and send heartbeats to WakaTime/Hackatime by [wakatime-cli](https://github.com/wakatime/wakatime-cli).

## Building from Source

1. Clone this repository:
```bash
git clone https://github.com/Sebastian-Alexis/zed-hackatime.git
cd zed-hackatime
```

2. Build the extension:
```bash
cargo build --release
```

3. The built extension will be at `target/wasm32-wasi/release/zed_wakatime.wasm`

## Loading into Zed

1. Open Zed
2. Open the command palette (Cmd+Shift+P on macOS)
3. Run "zed: install dev extension"
4. Select the directory containing this repository
5. The extension will be loaded and ready to use

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
