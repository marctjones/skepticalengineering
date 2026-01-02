+++
title = "PromptResponse"
description = "A cross-platform form application that abandons the page metaphor. Instead of wrestling with PDF quirks, Word's fragile form fields, or Excel protection schemes, PromptResponse uses a portable text-based format (.apr) built on JSON."
weight = 1
template = "project.html"

[extra]
category = "productivity"
status = "Active Development"
logo = "images/promptresponse_logo.svg"
github = "https://github.com/marctjones/promptresponse"
+++

## Overview

PromptResponse reimagines form-based data collection by abandoning the page metaphor entirely. Traditional form tools—PDF, Word, Excel—were designed for printed documents first, with digital interaction bolted on as an afterthought. The result is fragile forms that break across versions, accessibility nightmares, and data locked in proprietary formats.

PromptResponse starts from first principles: forms are structured data collection interfaces, not documents.

## Features

- **Pure JSON format** for easy database import, webhook submission, and programmatic processing
- **Responsive forms** that adapt to any screen without fixed layouts
- **WCAG 2.1 Level AA** accessibility by design
- **Safe to open untrusted files** (no code execution)
- **Built with .NET 8 and AvaloniaUI** for cross-platform support

## Technical Details

The `.apr` format is a JSON-based specification that describes form structure, validation rules, and conditional logic. Because it's plain text, forms can be:

- Version controlled with git
- Diffed and merged
- Generated programmatically
- Validated with JSON Schema
- Transformed with standard tools (jq, Python, etc.)

## Philosophy

The interesting part is making forms boring. No fancy features that break, no clever hacks that don't survive a software update. Just reliable, accessible data collection that works everywhere.
