# Video Republish Assistant

A portable ChatGPT and Codex plugin for downloading videos the user is authorized to reuse, preserving source metadata, and drafting Chinese copy for the destination platform.

## What it does

- Reads the original post and records the creator, source URL, caption, tags, and publication date.
- Downloads the highest practical MP4 quality through a browser-based tool without bypassing access controls.
- Saves a same-name Markdown provenance file beside the video.
- Checks that the downloaded file is readable and that picture and audio are present when expected.
- Drafts platform-appropriate Chinese titles, captions, tags, and source attribution.

The plugin never includes account cookies, access tokens, passwords, or temporary download URLs.

## Install from GitHub

Add this repository as a plugin marketplace:

```bash
codex plugin marketplace add HR2AY/video-republish-assistant
```

Restart the ChatGPT desktop app, open the Plugins Directory, select **HR2AY Video Tools**, and install **Video Republish Assistant**.

The host needs browser control and local file access. Optional media-inspection tools such as `ffprobe` can improve verification, but they are not bundled or required by the plugin.

## Example requests

```text
我有转载权限。把这个视频保存到 Downloads/搬运，目标平台是小红书，并写一版中文文案：https://example.com/video
```

```text
本次对话中我提供的所有链接都已获得转载授权。后续视频统一保存到 ~/Downloads/搬运，并生成同名来源信息文件。
```

## Responsible use

Only use this plugin for media you own or are authorized to download and republish. It does not bypass DRM, paywalls, authentication, CAPTCHAs, regional restrictions, or other technical protections. Review attribution requirements and the destination platform's current rules before publishing.

## Repository layout

```text
.agents/plugins/marketplace.json
plugins/video-republish-assistant/
├── plugin.json
└── skills/video-republish-assistant/
    ├── SKILL.md
    └── references/
```

## License

MIT
