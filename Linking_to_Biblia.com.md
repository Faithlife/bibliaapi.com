---
title: Linking to Biblia.com
layout: default
---

Biblia.com supports a clean URL structure designed for ease of use.

*Note: Linking to a book does not guarantee that the person following that link has permission to view the book. Some books on Biblia.com require a license, and someone trying to view a book that they do not own a license for will not be granted access.*

* **Book IDs**: To link to a Bible or other book, you will need to know its ID. For most common Bible translations, the book ID is the same as the translation's common abbreviated title. A few examples: esv, niv, nlt, nkjv. You can find the ID by viewing the book's info by clicking the "i" toolbar button while viewing the book. The book's ID will be listed at the bottom under "Support info".

* **Bible references**: Any Biblia.com URL that accepts a Bible reference is capable of parsing a variety of reference formats. For example, "John 3.16", "John 3 16", "Jn 3.16", "Jn3 16", etc. will all take you to same place. Please note that the colon (:) character is not allowed in URLs. We recommend using a period instead when linking to Bible references: use "John 3.16" instead of "John 3:16".

## Linking to Bibles

Linking directly to a Bible reference will display the reference in a simple full-screen view, along with footnotes and cross-references for the passage.

#### Linking to a specific reference within a specific Bible

```
https://biblia.com/bible/{bookID}/{reference}

https://biblia.com/bible/niv/Jn3.16
```

You can also link to Bible references using the [ref.ly](http://ref.ly) short URL service.

```
http://ref.ly/{reference}

http://ref.ly/Jn3.16
```

#### Linking to a specific reference without specifying a Bible

If you don't specify a Bible, Biblia.com will choose one. If the person following the link has signed in to Biblia.com, they will see their highest-ranked Bible that contains the requested reference. If not, a default will be chosen. In most cases, this will be the ESV.

```
https://biblia.com/bible/{bookID}/{reference}

https://biblia.com/bible/niv/Jn3.16

http://ref.ly/{reference};{bookID}

http://ref.ly/Jn3.16;niv
```

## Linking to non-Bible books

You can use these URLs to link to Bibles as well. The difference here is that the book will be displayed alongside a second book in a 2-column view.

#### Linking to the default location in a book

If the person following the link is signed in to Biblia.com, the book will be opened to their last-read position in the book. If not, the beginning of the book will be opened.

```
https://biblia.com/books/{bookID}

https://biblia.com/books/eastons
```

#### Linking to a reference in a specific book

```
https://biblia.com/books/{bookID}/{reference}

https://biblia.com/books/summbblnt/2Jn
```

#### Linking to a word entry in a specific book

Biblia.com also supports linking to specific words in books like dictionaries.

```
https://biblia.com/books/{bookID}/word/{word}

https://biblia.com/books/eastons/word/Matthias
```

#### Linking to an unknown reference or word in a specific book

If you have a query and you don't know if it's a reference or a word entry, you can let Biblia.com decide. Biblia.com will try to interpret your input as either a reference or a word entry, and if it finds one, redirect you to the corresponding location.

```
https://biblia.com/books/{bookID}/resolve?input={input}

https://biblia.com/books/summbblnt/resolve?input=Page19
```
