# TRP1: Research and Exploration Notes

## Explored Sources
1. **Boris Cherny's Workflow (Primary Reference):** Deep-dived into the "Plan-First" and "Verification Loop" logic.
2. **Model Context Protocol (MCP) Official Documentation:** Researched the architecture of the `mcp.json` structure to solve header issues.
3. **VS Code Copilot Extension GitHub Issues:** Researched why `Invoke-WebRequest` headers often fail in integrated terminals versus native shells.
4. **Community Best Practices:** Studied `.cursorrules` and `.github/copilot-instructions.md` patterns for "Agent Steering."

## Experiments Conducted
- **Test A (Default Agent):** Ran the agent with no rules. It attempted to solve tasks using Linux-style `curl` commands which failed in my Windows PowerShell environment.
- **Test B (Rule-Based Steering):** Implemented the Boris Cherny "Plan-First" rule. The agent stopped, proposed a plan, and allowed me to correct its terminal command before it failed.
- **Test C (MCP Integration):** Successfully verified the `tenxfeedbackanalytics` connection after discovering that manual header configuration in `mcp.json` is more stable for Windows 11 environments than CLI flags.

## Curated Resource List for AI Orchestration
- [Official MCP Documentation](https://modelcontextprotocol.io/)
- [Boris Cherny's Original Thread](https://x.com/bcherny)
- [GitHub Copilot Custom Instructions Guide](https://docs.github.com/en/copilot/using-github-copilot/customizing-copilot-responses)