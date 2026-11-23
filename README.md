# Contrast

Connect your data, query your warehouse, and build dashboards from Cursor or Claude Code. The plugin includes the Contrast MCP connection and a skill that guides your agent through source setup, SQL queries, and dashboards.

## Get started

Enable Contrast in your client. When prompted, sign in in your browser and select your workspace. Then ask your agent to show which data sources are connected and which tables are ready to query.

Try these prompts once your data is ready.

- Show revenue by month and tell me which table and definition you used.
- Build a dashboard for product usage and check that its charts run.

You'll need a Contrast workspace. Your workspace role determines which setup, source, and dashboard actions you can use. Initial sync time depends on your source and data volume.

## Try the plugin locally

- **Cursor.** Copy this folder to `~/.cursor/plugins/local/contrast`, reload Cursor, then check Customize for the Contrast skill and MCP server.
- **Claude Code.** Run `claude --plugin-dir .` from this folder, then open `/mcp` to connect `plugin:contrast-warehouse:contrast`.
- **Direct MCP setup.** Use the [Contrast MCP guide](https://docs.contrastdb.com/mcp) to connect without a plugin bundle.

## Connection and privacy

The plugin connects to `https://contrastdb.com/api/mcp` using browser OAuth. Tool calls send their inputs to Contrast and return authorized workspace data to your client. Connected tables can contain personal data. Source connection, ingestion, saved definitions, and dashboard actions can change workspace state. Warehouse SQL is read-only. The package includes the connection configuration, a Markdown skill, and the Contrast icon. Installation requires no scripts, local service, or API key.

Contrast stores imported data, saved definitions, and dashboards for the workspace. Removing a source stops future syncs. Previously imported data follows the workspace's retention and deletion settings. Diagnostic checks in the skill can also reach the first-party health endpoint at `https://api.embrasure.ai/health`.

[Documentation](https://docs.contrastdb.com/mcp) · [Privacy](https://contrastdb.com/privacy) · [Terms](https://contrastdb.com/terms) · [Support](https://contrastdb.com/support)

## License

The plugin configuration, skill, and documentation are MIT licensed. The Contrast service is subject to its terms. Brand names and logos are reserved for identifying Contrast.
