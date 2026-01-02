+++
title = "PDFE"
description = "A cross-platform PDF editor with true content-level redaction. Most PDF redaction tools just draw black boxes over sensitive text—the data is still there, extractable by anyone who knows to look. PDFE actually removes the content from the PDF structure."
weight = 2
template = "project.html"

[extra]
category = "productivity"
status = "Active Development"
logo = "images/pdfe_logo.svg"
github = "https://github.com/marctjones/pdfe"
+++

## Overview

PDFE addresses a critical flaw in most PDF redaction tools: they don't actually redact. Drawing a black rectangle over text is not redaction—the text remains in the PDF structure, trivially extractable with basic tools. This has led to countless security incidents where "redacted" documents leaked sensitive information.

PDFE performs true content-level redaction by removing glyphs from the PDF content streams themselves.

## Features

- **Glyph-level text removal** from PDF content streams, not visual masking
- **Verified with external tools** (pdftotext, PdfPig)—redacted text cannot be extracted
- **CLI tool (pdfer)** for batch redaction, search, and verification
- **OCR support** for scanned documents via Tesseract
- **Built with .NET 8 and AvaloniaUI** for cross-platform support

## How It Works

PDFs store text as a series of glyph positioning commands within content streams. PDFE:

1. Parses the PDF structure to locate text content streams
2. Identifies the specific glyphs that render the target text
3. Removes those glyphs from the content stream
4. Optionally draws a visual indicator (black box) where text was removed
5. Rewrites the PDF with the modified content streams

The result is a PDF where the redacted text simply doesn't exist—not hidden, not obscured, but gone.

## Verification

Trust but verify. PDFE includes verification tools that confirm redaction worked:

```bash
pdfer verify document.pdf --redacted "secret text"
```

This uses multiple extraction methods to confirm the text is truly gone from the document.
