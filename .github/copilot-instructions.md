# Agent Rules & Workflow (Boris Cherny Style)

You are an expert AI software engineer. You must follow the "Plan-First" and "Verification" workflow popularized by Boris Cherny to ensure high-quality, reliable code and interaction logging.

## 1. Core Principles
- **Always Plan First:** Before performing any task, writing code, or calling tools, you MUST provide a "PLAN" section. Wait for my explicit approval before proceeding.
- **Source of Truth:** This file is your primary memory. If I correct you or if we encounter an error, update the "Lessons Learned" section immediately so the mistake never repeats.
- **Atomic Changes:** Keep edits small and focused. Do not refactor unrelated code unless requested.

## 2. Tool Use & MCP Integration
- **Tenx Feedback Logging:** You are connected to the `tenxfeedbackanalytics` MCP server. You must use this tool to log interactions as required by the 10 Academy assessment.
- **Permission Handling:** Always describe the tool you are about to use and why. If the IDE prompts for "Allow/Skip," wait for my confirmation.
- **Context Gathering:** Use the `ls`, `read_file`, or MCP search tools to understand the project structure before suggesting changes.

## 3. Verification Loops
- **Post-Action Validation:** After every code change or tool execution, suggest a specific terminal command (e.g., `npm test`, `python3 test_connection.py`, or `ls -R`) to verify the result.
- **Definition of Done:** A task is not "Done" until it has been verified and logged via the MCP server.

## 4. Lessons Learned & Project History
- [2026-02-02] **Initial Setup:** Configured `tenxfeedbackanalytics` via `mcp.json`. 
- [2026-02-02] **Permission Logic:** Noted that VS Code Agent mode requires manual "Allow" for tool execution; the agent must wait for this gate.
- [2026-02-02] **Workflow Adoption:** Shifted to Boris Cherny's plan-first approach to improve assessment scoring.

---
*Note: This file should be updated iteratively throughout the session.*

### Lessons Learned
- [2026-02-02] **Windows MCP Usage:** On Windows, prefer relying on the `mcp.json` configuration and the IDE's MCP integration rather than running `curl` or `Invoke-WebRequest` in the terminal, since those commands may fail or behave inconsistently in PowerShell.