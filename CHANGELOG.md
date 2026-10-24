# Changelog

## 0.1.4

- Listing name: `displayName` is "Bluesky by Content Mill".

## 0.1.3

- README: add a troubleshooting section.
- PRIVACY: state that the audit record of tool calls includes the arguments Claude sent.

## 0.1.2

- Drop `privacyPolicyUrl` from `plugin.json`: the plugin directory reads the privacy policy URL from the README, and Claude Code does not recognise the field.

## 0.1.1

- Declare `privacyPolicyUrl` (https://contentmill.dev/privacy) in `plugin.json`.

## 0.1.0

- First release: Content Mill for Bluesky as a Claude plugin, pointing at `https://bsky-mcp.contentmill.dev/mcp`.
- Skills: `draft-post`, `publish-post`, `review-posts`.
