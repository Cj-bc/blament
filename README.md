# Blament -- git BLAMe for unity componENT

blament provides `git blame` for unity component.
It'll take GUID and fileID, returns JSON  dictionary that has each serialized properties as key, commit hash as value. If they're not committed, it'll be shown as "uncommitted".

# Usage

you can use JSON parsing tools like [jq](https://jqlang.org) or shells support JSON e.g. powershell (using [ConvertFrom-Json](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/convertfrom-json?view=powershell-7.5 )), nushell to process output.

```sh
$ blament REV -- GUID:fileID | jq '.m_LocalPosition'
"commit_hash_that_modified_m_LocalPosition"
```

# roadmap
- [ ] Name to fileId resolution (Maybe SCENE.GameObject.ComponentType or something?)
- [ ] simple unity side UI
- [ ] Lookup caching