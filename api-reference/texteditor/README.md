---
description: Represents a text editor window.
---

# TextEditor

A TextEditor object refers to an open text editor in CodeEdit. It should not be confused with a TextDocument object, which is a property of the TextEditor.

## Class Methods

<details>

<summary>delete(range: Range): TextEdit</summary>



</details>

<details>

<summary>insert(position: Position, newText: string): TextEdit</summary>



</details>

<details>

<summary>replace(range: <a href="range.md">Range</a>, newText: string): TextEdit</summary>



</details>

## Constructor

```javascript
new TextEdit(range: Range, newText: string: TextEdit)
```

## Methods



## Properties

<details>

<summary>document: <a href="textdocument.md">TextDocument</a></summary>

The document associated with the text editor.

</details>

<details>

<summary>options: TextEditorOptions</summary>



</details>

<details>

<summary>selections: <a href="selection.md">Selection</a>[]</summary>



</details>

## Events

<details>

<summary>onDidSave(callback)</summary>



</details>
