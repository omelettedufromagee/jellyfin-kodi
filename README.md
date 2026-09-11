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

<p align="center">
<img alt="Logo Banner" src="https://raw.githubusercontent.com/jellyfin/jellyfin-ux/master/branding/SVG/banner-logo-solid.svg?sanitize=true"/>
<br/>
<br/>
<a href="https://github.com/jellyfin/jellyfin-kodi"><img src="https://img.shields.io/github/license/jellyfin/jellyfin-kodi" alt="GPL 3.0 License" /></a>
<a href="https://github.com/jellyfin/jellyfin-kodi/releases"><img src="https://img.shields.io/github/v/release/jellyfin/jellyfin-kodi" alt="GitHub release (latest SemVer)" /></a>
<a href="https://matrix.to/#/+jellyfin:matrix.org"><img alt="Chat on Matrix" src="https://img.shields.io/matrix/jellyfin:matrix.org.svg?logo=matrix"/></a>
<br />
<a href="https://translate.jellyfin.org/engage/jellyfin/?utm_source=widget"><img src="https://translate.jellyfin.org/widgets/jellyfin/-/jellyfin-kodi/svg-badge.svg" alt="Translation status" /></a>
<a href="https://sonarcloud.io/dashboard?id=jellyfin_jellyfin-kodi"><img src="https://sonarcloud.io/api/project_badges/measure?project=jellyfin_jellyfin-kodi&metric=alert_status" alt="Quality Gate Status" /></a>
<a href="https://sonarcloud.io/dashboard?id=jellyfin_jellyfin-kodi"><img src="https://sonarcloud.io/api/project_badges/measure?project=jellyfin_jellyfin-kodi&metric=sqale_index" alt="Technical Debt" /></a>
<br />
<a href="https://sonarcloud.io/dashboard?id=jellyfin_jellyfin-kodi"><img src="https://sonarcloud.io/api/project_badges/measure?project=jellyfin_jellyfin-kodi&metric=code_smells" alt="Code Smells" /></a>
<a href="https://sonarcloud.io/dashboard?id=jellyfin_jellyfin-kodi"><img src="https://sonarcloud.io/api/project_badges/measure?project=jellyfin_jellyfin-kodi&metric=bugs" alt="Bugs" /></a>
<a href="https://sonarcloud.io/dashboard?id=jellyfin_jellyfin-kodi"><img src="https://sonarcloud.io/api/project_badges/measure?project=jellyfin_jellyfin-kodi&metric=vulnerabilities" alt="Vulnerabilities" /></a>
<br />
<img src="https://img.shields.io/github/languages/code-size/jellyfin/jellyfin-kodi" alt="GitHub code size in bytes" />
<a href="https://sonarcloud.io/dashboard?id=jellyfin_jellyfin-kodi"><img src="https://sonarcloud.io/api/project_badges/measure?project=jellyfin_jellyfin-kodi&metric=ncloc" alt="Lines of Code" /></a>
<a href="https://sonarcloud.io/dashboard?id=jellyfin_jellyfin-kodi"><img src="https://sonarcloud.io/api/project_badges/measure?project=jellyfin_jellyfin-kodi&metric=duplicated_lines_density" alt="Duplicated Lines (%)" /></a>
<br />
<a href="https://sonarcloud.io/dashboard?id=jellyfin_jellyfin-kodi"><img src="https://sonarcloud.io/api/project_badges/measure?project=jellyfin_jellyfin-kodi&metric=sqale_rating" alt="Maintainability Rating" /></a>
<a href="https://sonarcloud.io/dashboard?id=jellyfin_jellyfin-kodi"><img src="https://sonarcloud.io/api/project_badges/measure?project=jellyfin_jellyfin-kodi&metric=reliability_rating" alt="Reliability Rating" /></a>
<a href="https://sonarcloud.io/dashboard?id=jellyfin_jellyfin-kodi"><img src="https://sonarcloud.io/api/project_badges/measure?project=jellyfin_jellyfin-kodi&metric=security_rating" alt="Security Rating" /></a>
<br />
<a href="https://codecov.io/github/jellyfin/jellyfin-kodi"><img src="https://codecov.io/github/jellyfin/jellyfin-kodi/graph/badge.svg" alt="Code coverage" /></a>
<a href="https://github.com/jellyfin/jellyfin-kodi/actions/workflows/codeql.yaml"><img alt="CodeQL Analysis" src="https://github.com/jellyfin/jellyfin-kodi/actions/workflows/codeql.yaml/badge.svg" /></a>
</p>

Our informal Kodi support target is current release±1,
which currently translates to Nexus (old), Omega (current) and Piers (next).

Please note that next release is a moving target,
has a relatively low priority,
and is unlikely to receive active work before the release candidate stage.

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

### Contributing

#### AI/LLM

Please see [Jellyfin's official LLM policy](https://jellyfin.org/docs/general/contributing/llm-policies).

Any PR, issue or comment that is primarily LLM generated will be rejected outright on principle.

Machine translation as a communication aid is allowed,
but requires disclosure and that you also include the original language text.

LLM generated code has a high probability of getting rejected.
Relatively low effort AI contributions put an unsustainable
and unproportional extra burden on project maintainers,
which during the review process need to understand the suggested changes,
and evaluate whether they are good changes, whether there are better alternatives and so on.

LLM can be a decent tool to get up to speed and learn about the code-base,
but is highly likely to generate subpar code.

Fine for debugging, research and proof of concept,
but not currently suitable for production code.

#### Dev environment

The project use the following tools:

- [black](https://black.readthedocs.io/en/stable/) auto-formats the Python code (mandatory)
- [flake8](https://flake8.pycqa.org/en/latest/) to highlight potential issues
- [EditorConfig](https://editorconfig.org/) to ensure consistency in editor indentation and similar
- [pytest](https://docs.pytest.org/en/stable/) for code regression testing
- [pre-commit](https://pre-commit.com/) helps run the most important ones before commiting

[Visual Studio Code](https://code.visualstudio.com/) is my current editor of choice,
and as such the project is configured around this.
A [devcontainer](https://containers.dev/) config is available for consistency's sake
and quick setup, but I often don't use it myself.

[mypy](https://mypy.readthedocs.io/en/stable/index.html) is planned,
but there is a lot of work needed to properly implemet type-checking.
