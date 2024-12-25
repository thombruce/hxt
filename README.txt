 _       _   
| |_ _ _| |_ 
|   |_'_|  _|
|_|_|_,_|_|  

hxt is a set of formatting principles for `.txt` documents.

=== Headings ===

The default heading is three equals signs either side of a text string and separated by a space.

Second level headings are then denoted by the presence of two equals signs either side, and third level headings by one.

It should also be possible to support "higher" level headings (e.g. having four or more equals signs either side) where more than three heading levels are required.

A program wanting to parse a hxt-formatted text document should parse the headings and determine the number of levels required for presentation.

==== Heading 0 (Extended format) ====

=== Heading 1 (Default) ===

== Heading 2 ==

= Heading 3 =

=== Lists ===

== Bulleted Lists ==

- Bulleted item
- Bulleted item 2
- Bulleted item 3

== Numbered Lists ==

1. Numbered item
2. Numbered item 2
3. Numbered item 3

== Todo Lists ==

Todo lists will support the full spec of todo.txt in addition to my own extensions of the format. hxt is considered a superset of todo.txt and plaintext.

Buy groceries
Pick up dry cleaning
x Paint hallway

== Shopping Lists ==

Bananas     £0.20 x10
Eggs        £1.50 x2
x Milk      £1.75

=== Date Stamps ===

2024-12-23

=== Markup ===

== Emphasis ==

It is recommended NOT to use markup for emphasis (capitalization does the trick).

However, hxt aims to support simple *bold* and _italic_ text as well.

== Links ==

The 'h' in hxt doesn't stand for anything, but if it did it would be 'hyperlinks'.

The best way to include a link in a document is as plaintext: https://example.com/

hxt clients should also attempt to recognize relative links written in this way: ./example.txt

THE BELOW APPROACHES ARE NOT YET SUPPORTED!

Inspired by AsciiDoc, links may also contain title text:

- https://example.com/[Example]
- ./example.txt[Example]

These links with presentation metadata break in some readers, so I also aim to support an alternative inspired by Markdown:

- [Example](https://example.com/)
- [Example](./example.txt)
