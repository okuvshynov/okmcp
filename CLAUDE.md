# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

- **Install dependencies**: `uv --directory /path/to/summarize run summarize.py`
- **Run tests**: `python summarize.py --test`
- **Register MCP server**: `claude mcp add summarize -s user -- uv "--directory" /path/to/summarize run summarize.py`

## Code Style Guidelines

- Use Python 3.12+ features
- Include type annotations for all functions and parameters
- Format docstrings with Args sections for parameters
- Handle errors with specific try/except blocks and meaningful error messages
- Use async/await patterns for network operations
- Follow PEP 8 naming conventions (snake_case for variables and functions)
- Use logging with appropriate levels (info, error) for operational feedback
- Structure code with clear function separation and logical organization
- Organize imports: standard library first, then third-party packages

## Project Structure

The codebase implements a local LLM-based summarization tool as an MCP server for Claude Code. The main component is `summarize.py` which handles file processing, token counting, and communication with a local LLM server.

## Documentation

Custom Claude commands are available in `summarize/commands/` directory.