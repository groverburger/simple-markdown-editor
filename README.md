# Groverburger Simple Markdown Editor

## Overview

This project is a lightweight, self-contained Markdown editor and viewer built as a single HTML file. It allows users to write Markdown content in an editable textarea, toggle to a rendered preview, and supports features like local storage persistence, LaTeX math rendering, and print-optimized styling.

The editor starts in editing mode and provides a simple interface for creating and viewing formatted Markdown documents without any external dependencies beyond CDN-loaded libraries.

## Features

- **Editing and Preview Toggle**: Switch between raw Markdown editing and rendered HTML view using Ctrl+M (cross-platform).
- **Local Storage**: Automatically saves and loads content from the browser's localStorage to persist work across sessions.
- **Dynamic Title**: Updates the browser tab title based on the first heading in the Markdown content.
- **LaTeX Support**: Renders mathematical expressions using MathJax, supporting both inline ($...$) and display ($$...$$) modes.
- **Print-Friendly**: Includes CSS styles optimized for printing, with header grouping to avoid breaks and full-width layout.
- **Markdown Parsing**: Uses Marked.js to convert Markdown to HTML, with post-processing to group headings and subsequent content for better structure.

## Usage

To use the editor, simply open `index.html` in any modern web browser—no installation or setup required.

1. The page loads in editing mode with sample Markdown content if no saved data exists.
2. Type or paste your Markdown in the textarea; changes save automatically to localStorage.
3. Press **Ctrl+M** to toggle to preview mode, where the content renders as formatted HTML.
4. In preview mode, use browser print (Ctrl+P) for a clean, paginated output with avoided breaks in elements like tables and code blocks.
5. Return to editing with Ctrl+M again; the banner in the top-right indicates the current mode.

Example initial content includes headings, lists, links, images, code blocks, blockquotes, tables, and math examples to demonstrate capabilities.

## Project Structure

```
groverburger-simple-markdown-editor/
└── index.html
```

The entire application is contained in this one file, combining HTML structure, CSS styles, and JavaScript logic for simplicity and portability.

## Technologies Used

- **Frontend**: Pure HTML5, CSS3, and vanilla JavaScript for core functionality.
- **Libraries**:
  - Marked.js (CDN): Handles Markdown to HTML conversion.
  - MathJax 3 (CDN): Enables LaTeX rendering in SVG format.
- **Storage**: Browser localStorage for persistence.
- **Styling**: Responsive design with flexbox, print media queries, and GitHub-inspired typography.

No build tools, servers, or additional dependencies are needed, making it ideal for quick prototyping or offline use.

## Keyboard Shortcuts

- **Ctrl+M**: Toggle between editing and viewing modes (works on Windows/Linux; Cmd+M may work on macOS but is set to Ctrl for consistency).

## Contributing

This is a minimal project, but contributions are welcome. Fork the repository, make changes to `index.html`, and submit a pull request with details on improvements like additional Markdown extensions or themes.

For issues, check the browser console for errors related to CDN loads or rendering.

## License

This project is open-source and available under the MIT License. See the LICENSE file for details.
