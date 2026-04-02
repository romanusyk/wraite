---
name: edit
description: Edit article paragraphs for readability, suggesting changes in structure or colour mode
disable-model-invocation: true
argument-hint: <mode: structure|colour>
allowed-tools: Read
---

# Article Editing Command

Read and follow the editor instructions:

!`cat editor.md`

## Your Task

The author has provided text to edit. The editing mode is: **$0**

If the mode is not "structure" or "colour", ask the author to specify one of these two modes.

## Text to Edit

$1
