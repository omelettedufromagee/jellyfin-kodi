<h1 align="center">Jellyfin for Kodi with WebDAV optimizations</h1>
<h3 align="center">Part of the <a href="https://jellyfin.org">Jellyfin Project</a></h3>

---

<table>
  <thead>
    <tr>
      <td align="left">
        :warning: Fork from Official
      </td>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        <p>
          This plugin version is a fork of the official with some modifications to improve WebDAV compatibilities when using the NATIVE mode for video playback.
        </p>
      </td>
    </tr>
  </tbody>
</table>

### How to use

To use NATIVE mode with WebDAV links, place a secrets.json file in plugin.video.jellyfin/jellyfin_kodi/helper/:
#### plugin.video.jellyfin/jellyfin_kodi/helper/secrets.json
```
{
    "nativepath": "davs://myserver.com/media"
}
```

It should work for SFTP, FTP, FTPS, HTTP, HTTPS, etc...

Example:
- Jellyfin movie is available locally on: /media/Movies/My Movie/my.movie.mkv
- Jellyfin movie is also available remotely on: https://myserver.com/media/Movies/My Movie/my.movie.mkv
- Configure the nativepath through a config file (see below) and select NATIVE mode during plugin setup.

### Install Jellyfin for Kodi

Detailed installation instructions can be found in the [Jellyfin Client Documentation](https://docs.jellyfin.org/general/clients/kodi.html).

<!-- Get started with the [wiki guide](https://github.com/MediaBrowser/plugin.video.emby/wiki) -->

### Known limitations

- Chapter images are missing unless native playback mode is used.
- Certain add-ons that depend on seeing where your content is located will not work unless native playback mode is selected.
