# Symbols, Comments and Other .tmPreferences Metadata

**Index**

- Symbols
- Comments
- Environment variables
- Metadata

## Format

Unless otherwise noted, the format for all the files below is `.plist` with a `.tmPreferences` extension,
and the file names can be arbitrary.

## Symbols

---

TODO: We probably need a 'reference' topic too? Or make this a 'reference' only topic? It is only interesting for advanced users who want to develop their own plugins.

TODO: Add examples.

---

Sublime Text provides basic support for symbol navigation.

**Defining Symbols**

The symbol navigation framework in Sublime Text is text-based and uses regular expressions to define known symbols.

The regular expression engine used is Oniguruma. [link to syntax ref]

Additionally, symbol regexes can only target text with a *function* or a *class* scope. Any other text will be ignored.

Using Oniguruma's features, it is possible to apply transformations to the matched symbol text so their displayed value is more user-friendly.

**Navigating Symbols**

Once symbols are defined, you will be able to navigate them using standard key bindings: **F12** (go to definition), **Ctrl+R** (show symbols in file), and **Ctrl+Shift+R** (show symbols in project).

---

## Comments

**Defining Comment Data**

Sublime Text supports multiple types of comments: in-line, block and alternate (???).

Once comment data is available for a file type, you will be able to comment/uncomment code through standard key bindings (insert key bindings here).

Insert example here.

Naturally, comments can only be defined for programming or markup languages that have a notion of comments.

---

## Setting environment variables

CHECK: TM can do this; can ST too?