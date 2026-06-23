# Repository Guidelines

## Scoop manifests

- Keep package manifests in `bucket/`.
- After adding or changing a manifest, run `./bin/formatjson.ps1 <app>` to format it through Scoop's manifest formatter.
- Prefer `"checkver": "github"` for GitHub release manifests when the homepage points to the repository.
- After adding or changing a manifest with `autoupdate`, run `./bin/checkver.ps1 <app> -ForceUpdate` to verify the autoupdate URL and hash refresh path. This catches cases where normal `checkver` succeeds but forced autoupdate cannot compute or locate hashes.
- Run `./bin/test.ps1` before calling the change complete.
