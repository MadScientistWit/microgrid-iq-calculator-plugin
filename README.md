# MicroGrid-IQ Calculator

This cross-platform plugin connects Codex/ChatGPT and Claude clients to the same public, stateless MicroGrid-IQ calculation server.

## Included calculators

- Energy use
- Single-phase and three-phase AC power
- Copper-conductor voltage drop
- Dwelling service-load planning estimate
- Flat-rate utility bill with optional demand charge
- Battery backup energy capacity
- Explicit cash-flow metrics

The remote MCP endpoint is `https://microgrid-iq.com/mcp`. It does not require an account and does not read MicroGrid-IQ customer projects or private data.

Every calculation returns units, assumptions, a method version, and limitations. Electrical and dwelling outputs are planning estimates, not code-compliance or professional-design determinations. Cash-flow outputs are arithmetic analysis, not tax, legal, accounting, or investment advice.

## Install

Claude Code and Cowork users can add the public marketplace and install the plugin:

```text
/plugin marketplace add MadScientistWit/microgrid-iq-calculator-plugin
/plugin install microgrid-iq-calculator@microgrid-iq
```

ChatGPT, Claude, and other MCP clients can connect directly to
`https://microgrid-iq.com/mcp` after the production endpoint is deployed.

For help, use the [MicroGrid-IQ support page](https://microgrid-iq.com/support).
