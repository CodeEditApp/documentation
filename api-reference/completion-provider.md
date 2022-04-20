---
description: >-
  The completion provider interface defines how extensions should communicate
  code completion suggestions in CodeEdit.
---

# Completion Provider

## Registering a Completion Provider

```javascript
codeedit.extensions.registerCompletionProvider(myCompletionProvider)
```

## CompletionProvider Interface

```javascript
class CompletionProvider {
  provideCompletionItems(editor, context) {
    ...
    
    return completionItems;
  }
}
```

It is expected that every `CompletionProvider` class include a `provideCompletionItems` method, the role of which is to return an array of `CompletionItem` objects. This array of objects is used to determine relevant completion suggestions as the user types inside the editor.

In the case of the `CompletionProvider`, the `provideCompletionItems` method will be called each time the user types in the editor while the [activation event](../activation-events.md) conditions are met. CodeEdit will then determine the relevant suggestions.

The `provideCompletionItems` method expects an [editor](texteditor/textedit.md) and [context](context.md) as arguments. These objects provide the extension with information about the state when a completion is triggered, including the [scope](scope.md) of the current cursor position.

{% hint style="info" %}
Using the [context](context.md) object, additional completion criteria can be defined by limiting the results returned by the provideCompletionItems method based on the current context. For example, a completion suggestion that is a CSS class name, should only be returned when the current context is within a valid HTML class attribute.
{% endhint %}

## CompletionItem

### Constructor

`new CompletionItem(label: string, kind?:` [`CompletionItemKind`](completion-provider.md#undefined)`): CompletionItem`

Instantiates a new completion item object.

Completion items must have a label that is used as the default insert text as well as for sorting and filtering of completion suggestions.

### Properties

<details>

<summary>additionalTextEdits?: TextEdit[]</summary>

An array of additional text edits that should be applied when the completion is selected. _Edits must not overlap._

</details>

<details>

<summary>command?: Command</summary>

A command that should be executed after insertion of the selected completion.

</details>

<details>

<summary>commitCharacters?: string[]</summary>



</details>

<details>

<summary>detail?: string</summary>



</details>

<details>

<summary>documentation?: string | MarkdownString</summary>



</details>

<details>

<summary>filterText?: string</summary>



</details>

<details>

<summary>insertText?: string</summary>



</details>

<details>

<summary>keepWhitespace?: boolean</summary>



</details>

<details>

<summary>kind?: <a href="completion-provider.md#undefined">CompletionItemKind</a></summary>



</details>

<details>

<summary>label: string</summary>

The label of the completion item. It is also the default text that is inserted if the insertText property is not set.

</details>

<details>

<summary>range?: Range | {inserting: Range, replacing: Range}</summary>



</details>

<details>

<summary>sortText?: string</summary>



</details>

## CompletionItemKind
