# Sitecommand Connector — releases

Signed release builds of **Sitecommand Connector**, the WordPress plugin that connects a site to the [Sitecommand](https://sitecomand.xyz) hub so an AI assistant (Claude, Cursor, any MCP client) can manage it safely.

## Download

- **Latest version:** [releases/latest](https://github.com/nomanjawad/siteconnector-releases/releases/latest) → `sitecommand-connector.zip`
- Every release lists its changes in the release notes.

## Install

1. In wp-admin go to **Plugins → Add New → Upload Plugin** and upload `sitecommand-connector.zip`.
2. Activate it, then open **Tools → Sitecommand** and press **Connect with Sitecommand**.
3. Approve the site in your Sitecommand dashboard. That is all: no keys to copy.

Requirements: WordPress 6.0+, PHP 7.4+.

## Updates

Connected sites update themselves from this repository. Each release carries a `manifest.json` signed with Ed25519; the plugin installs an update only when the signature is valid and the zip's SHA-256 matches the manifest, so a changed or swapped zip is refused.

## Security

The plugin accepts only HMAC-signed requests from the hub it was connected to (±5 minutes, no replays), blocks malware-shaped code, and can lock a site against installing or running code (Code Lock). Please report security issues privately to privacy@sitecomand.xyz rather than in a public issue.

## Source

The plugin is developed in a separate private repository; this repository only publishes the builds.

Author: [Noman E Jawad](https://nomanjawad.vercel.app) · License: GPLv2 or later
