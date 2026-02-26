# RMz Injector

A cross-platform desktop tool that injects tweaks (.deb files) into iOS apps (.ipa files). Works on **macOS, Windows, and Linux** — no jailbreak required on the host machine.

## What it does

- Select an IPA and one or more .deb files containing dylibs or frameworks
- Extracts the dylibs/frameworks from the .deb packages
- Patches the app's executable with the necessary load commands
- Reorders load commands so frameworks initialize in the correct order
- Outputs a patched IPA ready for signing

## How to use

1. Download the zip for your OS from the [latest release](https://github.com/hliriano03/rmz-injector-releases/releases/latest)
2. Extract and run `RMzInjector`
3. Select your IPA file
4. Add your .deb file(s)
5. Click **Inject**
6. Sign the patched IPA with your preferred signing tool

### Platform notes

**macOS** — You may need to remove the quarantine attribute on first run:
```bash
xattr -d com.apple.quarantine RMzInjector
```

**Windows** — If SmartScreen blocks it, click "More info" → "Run anyway".

**Linux** — Make it executable first:
```bash
chmod +x RMzInjector
```

## Downloads

| Platform | File |
|----------|------|
| macOS (Apple Silicon) | [RMzInjector-osx-arm64.zip](https://github.com/hliriano03/rmz-injector-releases/releases/latest/download/RMzInjector-osx-arm64.zip) |
| macOS (Intel) | [RMzInjector-osx-x64.zip](https://github.com/hliriano03/rmz-injector-releases/releases/latest/download/RMzInjector-osx-x64.zip) |
| Windows (x64) | [RMzInjector-win-x64.zip](https://github.com/hliriano03/rmz-injector-releases/releases/latest/download/RMzInjector-win-x64.zip) |
| Linux (x64) | [RMzInjector-linux-x64.zip](https://github.com/hliriano03/rmz-injector-releases/releases/latest/download/RMzInjector-linux-x64.zip) |

No additional software or runtime needed — everything is bundled in the executable.
