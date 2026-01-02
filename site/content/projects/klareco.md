+++
title = "Klareco"
description = "An experimental conversational AI for Esperanto that prioritizes deterministic, explainable processing. The core idea: leverage Esperanto's regular grammar to replace neural components with programmatic logic, using learned parameters only for semantic reasoning."
weight = 5
template = "project.html"

[extra]
category = "research"
status = "Experimental"
logo = "images/klareco_logo.png"
github = "https://github.com/marctjones/klareco"
+++

## Overview

Modern large language models are impressive but opaque. They learn everything—including grammar—from data, making their behavior difficult to predict or explain. Klareco asks: what if we separated the learnable from the deterministic?

Esperanto, with its completely regular grammar (16 rules, no exceptions), is the perfect testbed. We can encode grammar directly in code and reserve machine learning for the genuinely hard part: meaning.

## Features

- **Esperanto's 16 grammar rules** encoded directly in the parser, not learned
- **Pipeline**: text → deterministic parser → AST → compositional embeddings → deterministic output
- **~333K learned parameters** handle semantics; grammar is fully programmatic
- **Thesis**: explicit grammar via ASTs lets a small core match larger models while remaining explainable

## Architecture

```
Input Text
    ↓
[Deterministic Tokenizer]
    ↓
[Rule-Based Parser] ← Esperanto's 16 rules
    ↓
Abstract Syntax Tree
    ↓
[Compositional Embeddings] ← Learned (~333K params)
    ↓
Semantic Representation
    ↓
[Deterministic Generator]
    ↓
Output Text
```

## Why Esperanto?

Natural languages are messy. English alone has:
- Irregular verbs (go/went, be/was/were)
- Context-dependent parsing (time flies like an arrow)
- Exceptions to every rule

Esperanto was designed to be regular:
- All verbs conjugate identically
- Word class is marked by ending (-o noun, -a adjective, -e adverb, -i verb infinitive)
- No irregular forms

This regularity means a hand-coded parser can handle 100% of Esperanto grammar—something impossible for natural languages.

## Research Questions

1. How much of language model capability comes from grammar vs. semantics?
2. Can explicit structure reduce the parameters needed for competent language use?
3. Does deterministic grammar improve explainability without sacrificing capability?

Klareco is an experimental platform for investigating these questions.
