# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a marketplace for Claude Code - a community-driven platform for sharing and discovering Claude Code extensions, skills, MCP servers, slash commands, and other resources.

Repository: https://github.com/arhx/claude-marketplace.git

## Development Environment

- Uses Vite for development with hot module reloading - **never run build commands** as Vite runs continuously
- Tailwind CSS 4.x - apply opacity using `/opacity` syntax (e.g., `bg-red-500/20` with 10-step increments or custom like `/[0.63]`)
- Prefer vanilla JS or Vue.js for dynamic pages - **avoid Alpine.js** unless absolutely necessary
- If using Alpine.js, always verify `x-data` is present when troubleshooting `@click` issues

## File Path Conventions

- Always use forward slashes `/` in paths when running commands (backslashes `\` cause issues on Windows)
- Never use `2>nul` in Bash commands

## Styling Guidelines

- Check `resources/css/*.css` for `@theme` color definitions before creating custom colors
- Avoid `text-[#...]` or `bg-[#...]` unless it's a one-off color not defined in theme
- New semantic color names can be added to the theme when appropriate

## File Operations

- Use `rm` command for deleting files
