# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This is a **documentation and technical specifications repository** for Paulina24 GmbH partner integrations. It contains JSON schemas, example data, and documentation for external partners integrating with the Paulina24 platform (a German elderly care provider matching platform).

**This repository contains NO executable code, build systems, or tests.** It is purely for documentation and data structure definitions.

## Repository Architecture

### Documentation Structure

The repository follows a modular documentation pattern:

- **Main README.md**: High-level overview, company info, and links to detailed documentation
- **outbound/**: Contains data structures for external partner consumption
  - **outbound/care-provider/**: Care provider profile specifications
    - **README.md**: Detailed profile documentation
    - **schema.json**: JSON Schema Draft 07 specification
    - **example.json**: Example profile data

### Key Principle: Schema as Source of Truth

The `schema.json` files are the **authoritative source** for data structures. When documenting enumerations or data types:
- **Do NOT list all enumeration values in markdown documentation**
- Instead, provide 2 example values and refer readers to the schema (e.g., "DRESSING, FEEDING, ...")
- This prevents documentation drift when schemas are updated

## Terminology

- **Always use "care provider"** (not "caregiver") when referring to the professionals who provide care
- Profile data is "privacy-filtered" for external consumption

## Schema Conventions

- **Standard**: JSON Schema Draft 07
- **Versioning**: Each profile includes `id` and `version` UUIDs for tracking
- **Structure**: All type definitions use `$defs` with descriptive names
- **Required fields**: Explicitly defined via `required` arrays
- **No additional properties**: `additionalProperties: false` enforced throughout

## Making Changes

When adding new data structures to `outbound/`:
1. Create a new subdirectory under `outbound/` for the data type
2. Include: `README.md`, `schema.json`, and `example.json`
3. Update the main README.md to link to the new subdirectory
4. Follow the existing pattern: examples instead of exhaustive enum listings
5. Ensure all schemas conform to JSON Schema Draft 07
