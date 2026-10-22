# Corvus plugins

A plugin adds something to Corvus without waiting for a new release. These plugins need
**Corvus 0.5.2 or later**, and Math preview's list needs **0.5.3**: Corvus offers the update
itself, or download it from the [latest release](https://github.com/Subirac/corvus-releases/releases/latest).

| Plugin | Version | What it does |
| --- | --- | --- |
| [Tree lists](tree-1.0.1.zip) | 1.0.1 | Put a nested list in a `::: tree` container and it is drawn as a tree, its items joined by lines (├── └── │), in the HTML Preview and the PDF. |
| [Math preview](math-preview-1.2.0.zip) | 1.2.0 | While the caret is inside maths, a small window shows it as the Preview will draw it, and redraws it as you type. A Maths tab lists every piece of maths in the document; Select Next/Previous Maths steps through them; Wrap Selection in $ makes maths. |

## Installing one

1. Click the plugin's name above, then **Download raw file** (the ⬇ button) to save the `.zip`.
   Leave it zipped.
2. In Corvus choose **Settings ▸ General ▸ Plugins ▸ Install Plugin…** and pick the `.zip`.
   Corvus shows the plugin's name, version and author and asks before installing. It works at once.

**To update a plugin**, install the newer `.zip` the same way: Corvus asks to replace the version
you have.

To switch a plugin off, untick it in the same list; to remove it, click **Remove…**. Either takes
effect when Corvus next starts (the list offers **Relaunch Corvus**).

A plugin is a program that runs inside Corvus with Corvus's own access to your files, so Corvus
runs only plugins its developer **signed**, and refuses one whose files were changed after
signing. A document can never make Corvus run a plugin.

**Had Tree lists 1.0.0?** It was not signed, so Corvus 0.5.2 stops loading it (Settings says
why). Install 1.0.1 from the table above; it replaces 1.0.0 and works at once.

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

## Using Math preview

Put the caret inside maths — `$x + y$`, `$$\frac{a}{b}$$`, or an environment written bare such as
`\begin{align} … \end{align}` — and a small window shows the maths as the Preview will draw it.

- **Drag** it anywhere; it opens there from then on. **Double-click** it to put it back under the
  maths.
- **Escape** closes it until the caret leaves that maths. A mistake shows in red, with KaTeX's
  message underneath.
- **View ▸ Show Math Preview** switches it off and on. Give it a key in Settings ▸ Keyboard (under
  *Plugins*), or put its **Math** button on the toolbar with View ▸ Customize Toolbar.
- A **Maths** tab in the Navigation panel lists every piece of maths in the document, drawn, with
  its line number; click one to go to it. **Window ▸ Maths List** (⌥⌘5) shows and hides it.
- **Edit ▸ Find ▸ Select Next Maths** (⌘⇧Y) and **Select Previous Maths** (⌥⌘⇧Y) step through
  the maths and open the window on each.
- **Format ▸ Wrap Selection in $** turns the selection into maths.
- Every key can be changed in Settings ▸ Keyboard, under *Plugins*. The list and the Select
  commands need Corvus 0.5.3; in 0.5.2 the tab says so and the rest works.
