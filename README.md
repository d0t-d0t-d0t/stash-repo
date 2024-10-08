# Repo

https://raw.githubusercontent.com/d0t-d0t-d0t/stash-repo/refs/heads/dist/index.yml

# Plugins List

## stashAudioPlayer

This plugin adds an audio-only toggle button and support for audio files in the Stash player through hls transcoder.

> [!IMPORTANT]
> Now the plugin can automatically check for file extensions without the need of the `Audio` tag.
>
> Options can be modified in the plugin settings.

#### Requirements

-   CommunityScriptsUILibrary plugin

-   (Optional)
    This plugin can check for a tag to identify files as audio, if you want to use that function instead of the file extension, you may need to add that tag:
    1. Add audio extensions files in the library settings (ex. mp3, m4a).
    2. Create an `Audio` tag.
    3. Make an `Audio` directory to put the files in and use 'Auto Tag' to tag the files inside the folder, or add the tag manually.
    4. Enable the `Use Tag` option in the plugin settings.

---

<details>
<summary><b>How to manually add a plugin</b></summary>

#### Windows/Linux

`git clone` to `%USERPROFILE%\.stash\plugins` for Windows or `/root/.stash/plugins` for Linux

#### Docker

Clone the repository:

```
git clone https://github.com/d0t-d0t-d0t/stash-repo.git
```

Copy to the container:

```
docker cp stash-repo/Plugins/pluginName stash:/root/.stash/plugins/pluginName
```

Now you can delete the local copy

### How to remove the plugin

#### Windows/Linux

Delete the folder `%USERPROFILE%\.stash\plugins\pluginName` for Windows or `/root/.stash/plugins/pluginName` for Linux

#### Docker

```
docker exec stash rm -rf /root/.stash/plugins/pluginName
```

</details>
