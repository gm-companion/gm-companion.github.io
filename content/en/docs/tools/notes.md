---
title: Notes
description: Note keeping tool with Markdown syntax and PDF export.
---

![Screenshot of notes tool in editing mode](/images/notes-tool-01.webp)

![Screenshot of notes tool in reading mode](/images/notes-tool-02.webp)

## Books and Chapters

Books and chapters are actually folders inside your configured notes folder.  
The only difference is that books are the top level folders.

A book/chapter can contain more chapters and multiple note pages.

To add a new book, press the "New Notebook" button, set a name and press enter.
Chapters can be added by right-clicking books or chapters and selecting "New Chapter".

## Pages

Notes are textfiles stored inside chapters.  
A note must always belong to a chapter or a book.

Pages can be added by right-clicking books or chapters and selecting "New Page".
If you don't add a file extension, `.md` is used.

### Markdown

Markdown is a simple markup language. If you have never heard about it, have a look at [this guide](https://www.markdownguide.org/).

By clicking the eye/pen icon you can switch between editing and reading mode.

### PDF Export

Pages can also be exported as PDFs.

To do that, switch into reading mode and press the "PDF" button. The document will be placed next to the markdown file in the file system.

## Encryption

The "Encrypt Page" button encrypts the current note using the "rot13" method.  
This method is not a cryptographically safe encryption method as it only replaces every letter by the one at the current alphabetic index + 13, so that encrypting the encrypted note again restores the original content.

The idea behind this feature is to prevent others from accidentally reading your notes.

![Screenshot of notes tool in reading mode (encrypted)](/images/notes-tool-03.webp)