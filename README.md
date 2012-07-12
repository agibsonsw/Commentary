Commentary
==========

ST comments (renamed from PrintHtml)

I wanted to rename PrintHtml to Commentary but it seems 
complicated in GitHub. So I created this new repository.

Anyway, this allows the creation and management of comments 
within Sublime Text, and includes an option to output them 
in HTML format.

NB I WILL (EVENTUALLY) DELETE THE PRINTHTML REPO

For Sublime Text 2:
This enables the creation of comments that do not appear in-line in your code. The comments are attached to words in your code using an input-panel. The input-panel can remain open to allow you to navigate between comments, move them around and delete, or modify, them.

The comments can also be shown in a quick-panel; choosing a comment from this takes you to the commented-line. This can be viewed as a bookmarking-feature "with added commentary".

There is also a TextCommand to produce an HTML document from your code, which uses your themes font, colours, etc. Any commments that you've added will appear as pop-up tooltips on hovering over their attached word. An alternative theme can also be specified.

Another TextCommand - SaveWithComments - will save the comments, using the file-name with 'cmts' added to the end. They can subsequently be re-loaded for your document.

My key-bindings:

{ "keys": ["ctrl+alt+k"], "command": "commentary" },
{ "keys": ["ctrl+alt+q"], "command": "quick_comments" },
{ "keys": ["ctrl+alt+m"], "command": "print_html", "args": { "numbers": false } },
{ "keys": ["ctrl+alt+n"], "command": "print_html", "args": { "numbers": true } },
{ "keys": ["ctrl+s"], "command": "save_with_comments" }

Commentary is the main TextCommand that produces the comments' input-panel.
The 'numbers' arguments specifies whether or not to show the line-numbers in the HTML output.
You may prefer to use something other than Ctrl-S for the save-with-comments option.

The document Commmentary.rtf provides the fullest, and up-to-date, details.