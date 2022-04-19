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

The `provideCompletionItems` method expects an [editor](editor.md) and [context](context.md) as arguments. These objects provide the extension with information about the state when a completion is triggered, including the [scope](scope.md) of the current cursor position.

Using the [context](context.md) object, additional completion criteria can be defined by limiting the results returned by the provideCompletionItems method based on the current context. For example, a completion suggestion that is a CSS class name, should only be returned when the current context is within a valid HTML class attribute.

## CompletionItem Interface

