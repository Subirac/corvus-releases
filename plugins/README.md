# Corvus plugins

A plugin adds something to Corvus, usually a container of its own, without waiting for a new
release. Plugins need **Corvus 0.5.1 or later**: Corvus offers the update itself, or download it
from the [latest release](https://github.com/Subirac/corvus-releases/releases/latest).

| Plugin | Version | What it does |
| --- | --- | --- |
| [Tree lists](tree-1.0.0.zip) | 1.0.0 | Put a nested list in a `::: tree` container and it is drawn as a tree, its items joined by lines (├── └── │), in the HTML Preview and the PDF. |

## Installing one

1. Click the plugin's name above, then **Download raw file** (the ⬇ button) to save the `.zip`.
   Leave it zipped.
2. In Corvus choose **Settings ▸ General ▸ Plugins ▸ Install Plugin…** and pick the `.zip`.
   Corvus shows the plugin's name, version and author and asks before installing. It works at once.

To switch a plugin off, untick it in the same list; to remove it, click **Remove…**. Either takes
effect when Corvus next starts (the list offers **Relaunch Corvus**).

A plugin is a program that runs inside Corvus with Corvus's own access to your files — install
plugins only from people you trust. A document can never make Corvus run a plugin.

## Using Tree lists

```
::: tree **project/**
- `src/`
  - `main.ts`
- `docs/`
  1. Guide
  2. Reference
- `README.md`
:::
```

The words after `tree` are the title, and the top level hangs from it. Without a title the
top-level items are still joined by a line. Numbered lists keep their numbers, checklists keep
their boxes, and in the PDF a long tree breaks across pages between any two rows. A document that
uses `::: tree` still opens without the plugin and shows an ordinary list.
