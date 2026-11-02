# Findings & Technical Observations

## 1. Google Stitch MCP Discovery
- The MCP server configuration is present in `~/.gemini/config/mcp_config.json` under name `"stitch"`.
- It uses the CLI package `@_davideast/stitch-mcp` with an active `STITCH_API_KEY`.
- Direct invocation via `npx -y @_davideast/stitch-mcp tool <tool_name> -f <payload_file> -o json` executes deterministically.
- Available tools:
  - `create_project`: Creates new project container.
  - `create_design_system`: Configures palette, typography, roundness, custom colors.
  - `generate_screen_from_text`: Synthesizes full UI screens from detailed text prompts.
  - `edit_screens`: Performs targeted prompt-based edits on existing screens.
  - `list_screens`, `get_screen`, `download_file`, `download_assets`.

## 2. Visual Reference Synthesis
- **Reference 1 (Hero)**:
  - Giant background serif typography (e.g., "DR. AARAV SHARMA" or "SHARMA") layered behind doctor portrait.
  - Clean floating navigation with warm ivory pill or glass style.
  - Prominent primary CTA ("Book Appointment") and secondary CTA ("Explore Expertise").
  - Small social proof / trust badges (e.g., "4.9 ★ Rating", "10+ Years Experience").
- **Reference 2 (Services)**:
  - 3-column x 2-row clean grid.
  - One highlighted card in deep contrast (Forest Green `#183D32`).
  - Subtle borders, refined icons, and clear "Learn More" links.
- **Reference 3 (Statistics)**:
  - 4 horizontal cards side-by-side.
  - One highlighted card (Forest green).
  - High typographic scale for numerals (`12+`, `5,000+`, `98%`).
- **Reference 4 (Contact)**:
  - Two-column split: Interactive/styled map + clinic office info cards on the left; clean enquiry form on the right.
- **Reference 5 (Testimonials)**:
  - Giant soft quote marks (`“`).
  - Carousel cards with 5-star ratings, structured patient quotes, name, and age/demographic placeholder.
  - Pagination dots + circular prev/next arrow buttons.
