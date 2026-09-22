# kdev

Parent repository for kparser / kparser2 / kpacket2 development. Collaborators only need this repo.

How we work: [CONTRIBUTING.md](CONTRIBUTING.md). Open work lives in GitHub Issues on the child that owns the change. Git holds facts.

## Clone

```powershell
git clone https://github.com/poroburu/kdev.git
cd kdev
git submodule update --init
git submodule update --init --recursive kpacket2
# private pins (if you have access):
git submodule update --init ffxi-captures
git submodule update --init FFXILogs
```

`git clone --recurse-submodules` also initializes nested modules under `server` (`navmeshes`, `ximeshes`), which are large, and will error on private `ffxi-captures` and `FFXILogs` unless you have access. Prefer the commands above.

## Layout

| Path | Role |
|------|------|
| `kparser2/` | Packet-native parser — primary write path |
| `kpacket2/` | Ashita v4 live capture plugin |
| `kparser/` | Legacy chat-log parser |
| `kpacket/` | Legacy Lua ZMQ addon |
| `XiPackets/` | Packet layout reference (upstream) |
| `VieweD/` | Capture viewer / field oracle (upstream) |
| `server/` | LandSandBoat SQL/item/zone source (upstream) |
| `ffxi-captures/` | Local reference captures (private pin; payloads untracked) |
| `FFXILogs/` | Community parse site and WebView2 shell (private pin) |

`kpacket2` pins its own `XiPackets` submodule. The root `XiPackets/` copy is the workspace reference pin.

## Build

From a PowerShell prompt at the kdev root:

```powershell
cd kparser2
dotnet build kparser2.sln
```

Live capture plugin:

```powershell
cd kpacket2
.\build.ps1
```

See [kparser2/README.md](kparser2/README.md) and [kpacket2/README.md](kpacket2/README.md). Wire contract: [kparser2/docs/COMPATIBILITY.md](kparser2/docs/COMPATIBILITY.md).
