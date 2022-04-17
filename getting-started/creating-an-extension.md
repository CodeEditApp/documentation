---
description: Create a new extension project and become familiar with its structure.
---

# Creating an Extension

## System Requirements

Before creating an extension make sure the following requirements are met.

* You have [Node.js](https://nodejs.org/en/) 16.10 or higher installed.
* You have [Git](https://git-scm.com) installed.

## Starting a New Extension

CodeEdit makes it easy to create a new extension project using the **Extensions** menu. To get started choose **Extensions > New Extension…**, which will open a Save dialog prompting you to select a location for your project.

{% hint style="info" %}
**Extension Developer Account**

It is not necessary to have a CodeEdit developers account if you have no intention of offering the extension on the Extension Store. However, an account is required to publish an extension and make it publicly available. See [Publishing an Extension](publishing-an-extension.md) for more information.
{% endhint %}

## File and Folder Structure

```
.
├── assets/
│   └── icon.png
├── node_modules/
│   └── ... 
├── src/
│   └── main.js
├── .gitignore
├── CHANGELOG.md
├── manifest.json
└── README.md
```



## Manifest File

## Extension Entrypoint
