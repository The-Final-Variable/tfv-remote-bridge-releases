# TFV Remote Bridge — Downloads

Pre-built binaries for [TFV Remote Bridge](https://github.com/The-Final-Variable) — a secure remote execution tool for MSP workflows.

## Download

Grab the latest release for your platform from the [Releases](https://github.com/The-Final-Variable/tfv-remote-bridge-releases/releases) page, or use the one-liner commands below.

## Quick Deploy (One-Liner)

### Windows (PowerShell):
```powershell
irm "https://github.com/The-Final-Variable/tfv-remote-bridge-releases/releases/latest/download/tfv-remote-bridge-windows-amd64.exe" -OutFile "$env:TEMP\tfv-rb.exe"; & "$env:TEMP\tfv-rb.exe" --code CODE --cleanup
```

### Linux (bash):
```bash
curl -sL "https://github.com/The-Final-Variable/tfv-remote-bridge-releases/releases/latest/download/tfv-remote-bridge-linux-amd64" -o /tmp/tfv-rb && chmod +x /tmp/tfv-rb && /tmp/tfv-rb --code CODE --cleanup
```

### macOS (bash):
```bash
curl -sL "https://github.com/The-Final-Variable/tfv-remote-bridge-releases/releases/latest/download/tfv-remote-bridge-macos-arm64" -o /tmp/tfv-rb && chmod +x /tmp/tfv-rb && /tmp/tfv-rb --code CODE --cleanup
```

Replace `CODE` with the pairing code provided by your support technician.

## Flags

| Flag | Description |
|------|-------------|
| `--code CODE` | Provide pairing code (skips interactive prompt) |
| `--cleanup` | Auto-delete binary on exit (zero trace) |

## Platforms

| File | Platform |
|------|----------|
| `tfv-remote-bridge-windows-amd64.exe` | Windows x64 |
| `tfv-remote-bridge-windows-arm64.exe` | Windows ARM |
| `tfv-remote-bridge-linux-amd64` | Linux x64 |
| `tfv-remote-bridge-linux-arm64` | Linux ARM |
| `tfv-remote-bridge-macos-amd64` | macOS Intel |
| `tfv-remote-bridge-macos-arm64` | macOS Apple Silicon |

## Security

- Pairing codes are single-use and expire in 15 minutes
- All traffic encrypted via TLS (WSS over port 443)
- Binary is useless without the paired server instance
- `--cleanup` flag removes all traces after disconnect

---

© Akshay Sood
