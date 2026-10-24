# Privacy

This plugin is a thin wrapper: it ships configuration and skill text, and points Claude at the hosted Content Mill MCP server at `https://bsky-mcp.contentmill.dev/mcp`. The plugin itself runs no code and stores nothing on your machine.

## What the server handles when you use it

- Your Content Mill sign-in (email and password, or Google sign-in) to authorise the connection. The access token Claude receives is valid for this Bluesky server only and is not accepted anywhere else.
- The text, media and schedule of the posts and drafts you ask Claude to create, and the results of publishing them.
- The names and connection status of your connected Bluesky accounts.
- A record of each tool call made on your behalf: which tool, when, the arguments Claude sent (for example the post text, the accounts and the media links) and a short result, so you can see what an assistant did.

Posts are sent to Bluesky only after you approve a preview. Content Mill does not post anywhere else.

## Full policy

The authoritative description of what Content Mill collects, how long it keeps it and how to delete your account is the privacy policy: https://contentmill.dev/privacy

Contact: support@contentmill.dev
