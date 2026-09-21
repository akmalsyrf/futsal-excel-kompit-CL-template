# Futsal Excel Kompit CL Template

Node.js generator for the Kompit Futsal CL team roster Excel template.

## Features

- Sheet protection with limited editable ranges
  - **TEAM**: `D1:D4` only
  - **PA / PI**: `A3:Q16` only
- Indonesian province & cascading city dropdowns (via `FILTER` helper on `Wilayah`)
- Hardened roster validations (WhatsApp phone, jersey number, NIM, IPK, enrollment year, etc.)

## Requirements

- Node.js >= 18

## Usage

```bash
npm install
npm run generate
```

Output: `output/Template Futsal Kompit - CL.xlsx`

```bash
node generate.js --out /path/to/file.xlsx
node generate.js --password mysecret
```

Default sheet-unprotect password: `kompit`

## Project layout

| Path | Description |
|------|-------------|
| `generate.js` | Template generator (ExcelJS) |
| `data/indonesia-regions.json` | Province → city map |
| `output/` | Generated `.xlsx` (gitignored) |

## License

Private / internal Kompit use.
