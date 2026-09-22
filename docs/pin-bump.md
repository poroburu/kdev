# Pin bump

After a child commit is pushed, update the kdev gitlink.

```powershell
cd C:\Users\porob\git\kdev
git add kparser2   # or kpacket2, kparser, ...
git status         # expect a gitlink SHA change
git commit -m "chore: bump kparser2"
git push
```

Verify:

```powershell
git submodule status
```

A fresh clone should show the new SHA:

```powershell
git clone https://github.com/poroburu/kdev.git kdev-verify
cd kdev-verify
git submodule update --init
git submodule status
```

`ffxi-captures` and `FFXILogs` use `update = none`. Initialize them only when you have access:

```powershell
git submodule update --init ffxi-captures
git submodule update --init FFXILogs
```
