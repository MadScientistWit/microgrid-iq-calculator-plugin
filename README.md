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

## Connect

The production endpoint must be deployed and return seven tools before clients
can connect.

### ChatGPT

1. Open **Settings → Security and login** and enable **Developer mode**.
2. Open the ChatGPT **Plugins** page and select **+**.
3. Name the connection `MicroGrid-IQ Calculator`.
4. Enter `https://microgrid-iq.com/mcp`.
5. Review the seven discovered tools, add the connection to a new chat, and try
   a starter prompt below.

### Claude

In Claude web or Desktop, open **Customize → Connectors → + → Add custom
connector**, name it `MicroGrid-IQ Calculator`, and enter
`https://microgrid-iq.com/mcp`. No OAuth credentials are required.

Claude Code users can connect directly:

```text
claude mcp add --transport http --scope user microgrid-iq-calculator https://microgrid-iq.com/mcp
claude mcp get microgrid-iq-calculator
```

Claude Code users can also add the public plugin marketplace:

```text
/plugin marketplace add MadScientistWit/microgrid-iq-calculator-plugin
/plugin install microgrid-iq-calculator@microgrid-iq
/reload-plugins
/mcp
```

In Cowork, open **Customize → Plugins → Add marketplace**, enter
`MadScientistWit/microgrid-iq-calculator-plugin`, and install
`MicroGrid-IQ Calculator`.

## Starter prompts

- `Calculate energy use for a 5 kW load running 8 hours.`
- `Estimate voltage drop for my copper circuit.`
- `Size a battery for 2 kW of critical load for 12 hours.`

For help, use the [MicroGrid-IQ support page](https://microgrid-iq.com/support).
