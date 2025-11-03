# CodePush Storage

GitHub-based storage for React Native OTA updates.

## Structure

- `index.json` - Main index (checked by apps)
- `db/` - JSON databases
- `bundles/` - JS bundles by app/deployment/version

## Usage

Apps point to this repo's raw URLs:

```xml
<string name="CodePushServerUrl">https://raw.githubusercontent.com/YOUR-USER/YOUR-REPO/main</string>
```

Managed by `gh-codepush` CLI.
 
