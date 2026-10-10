# Agentic Code Review System

A multi-agent system built with LangGraph that automatically analyzes repositories for policy violations, prioritizes issues, implements fixes, and directly merges changes to the main branch.

## Architecture

The system is implemented in src/main.py and consists of a four-agent system:

- **Analysis Agent** - Selects repositories most likely to have policy violations and prioritizes issues
- **Code Review Agent** - Checks selected repositories for policy violations  
- **Developer Agent** - Fixes identified issues
- **Commit Agent** - Creates temporary branches, commits fixes, and directly merges to the main branch

The system proactively scans repositories in an organization and uses LLM to select high-risk repositories for policy checks.

## Features

- Checks code against company policies stored in a local JSON file
- Automatically fixes non-compliant code
- Creates temporary branches and directly merges fixes to the main branch
- Support for GitHub and custom Git servers via API


