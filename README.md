[English](README.md) | [繁體中文](README.zh.md)

# PPTX Skill

A Claude Code skill for creating, reading, and editing PowerPoint presentations (.pptx files).

## Features

- **Read & Analyze**: Extract text with markitdown, generate visual thumbnail grids
- **Edit from Template**: Unpack/repack XML workflow for precise template-based editing
- **Create from Scratch**: Generate presentations using PptxGenJS with full design control
- **Visual QA**: Convert to images for automated slide inspection and verification
- **XML Validation**: Schema-based validation of Office Open XML structure

## Installation

```bash
# Copy to your skills directory
cp -r pptx/ ~/.claude/skills/pptx/
```

### Python Dependencies

```bash
pip install "markitdown[pptx]" Pillow
```

### Node.js Dependencies

```bash
npm install -g pptxgenjs
```

### System Dependencies (macOS)

```bash
brew install libreoffice poppler
```

## Usage

Simply ask Claude to work with a PowerPoint file:

- "Create a pitch deck about AI trends"
- "Read the content of presentation.pptx"
- "Edit the slides in my template"
- "Generate a 10-slide presentation from this outline"
- "Extract text from this deck"

## File Structure

```
pptx/
  SKILL.md              -- Main skill instructions
  references/
    editing.md          -- Template-based editing guide
    pptxgenjs.md        -- PptxGenJS creation guide
  scripts/              -- Python helper scripts
    add_slide.py        -- Add slides to presentations
    clean.py            -- Clean XML artifacts
    thumbnail.py        -- Generate slide thumbnails
    office/             -- Office XML utilities
      pack.py           -- Pack XML back to .pptx
      unpack.py         -- Unpack .pptx to XML
      validate.py       -- XML schema validation
      soffice.py        -- LibreOffice wrapper
      helpers/          -- XML processing helpers
      schemas/          -- Office Open XML schemas
      validators/       -- Format-specific validators
  assets/               -- (reserved for future assets)
```

## License

Proprietary. See LICENSE.txt for complete terms.

## Source

Adapted from [anthropics/skills](https://github.com/anthropics/skills/tree/main/skills/pptx).
