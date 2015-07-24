General Style
=============

A general guide for programming in style.

Formatting
----------

* Avoid inline comments.
* Break long lines after 80 characters.
* Delete trailing whitespace. Your editor should be configured to do so automatically:
  * [Sublime Text](http://nategood.com/sublime-text-strip-whitespace-save)
  * [Vim](http://vim.wikia.com/wiki/Remove_unwanted_spaces)
  * [Atom](https://github.com/atom/whitespace)
* Don't include spaces after `(`, `[` or before `]`, `)`.
* Don't misspell.
* Don't vertically align tokens on consecutive lines.
* If you break up an argument list, keep the arguments on their own lines and
  closing parenthesis on its own line.
* If you break up a hash, keep the elements on their own lines and closing curly
  brace on its own line.
* Indent continued lines two spaces.
* Indent private methods equal to public methods.
* If you break up a chain of method invocations, keep each method invocation on
  its own line. Place the `.` at the end of each line, except the last.
  [Example][dot guideline example].
* Use 2 space indentation (no tabs).
* Use an empty line between methods.
* Use empty lines around multi-line blocks.
* Use spaces around operators, after commas, after colons and semicolons, around
  `{` and before `}`.
* Use [Unix-style line endings] (`\n`).
* Use [uppercase for SQL key words and lowercase for SQL identifiers].

[dot guideline example]: https://github.com/thoughtbot/guides/blob/master/style/samples/ruby.rb#L11
[uppercase for SQL key words and lowercase for SQL identifiers]: http://www.postgresql.org/docs/9.2/static/sql-syntax-lexical.html#SQL-SYNTAX-IDENTIFIERS
[Unix-style line endings]: http://unix.stackexchange.com/questions/23903/should-i-end-my-text-script-files-with-a-newline

File Names
----------

* Separate words using underscores, not dashes (`user_settings.coffee`, not `user-settings.coffee`)
* Avoid multiple filetypes (`user_settings.coffee`, not `user_settings.js.coffee`)

Naming
------

* Avoid abbreviations.
* Avoid object types in names (`user_array`, `email_method` `CalculatorClass`, `ReportModule`).
* Name the enumeration parameter the singular of the collection.
* Name variables, methods, and classes to reveal intent.
* Treat acronyms as words in names (`XmlHttpRequest` not `XMLHTTPRequest`),
  even if the acronym is the entire name (`class Html` not `class HTML`).
* Name variables holding a factory with `_factory` (`user_factory`).
* Name variables created by a factory after the factory (`user_factory`
  creates `user`).

Organization
------------

* Order methods so that caller methods are earlier in the file than the methods
  they call.
* Order methods so that methods are as close as possible to other methods they
  call.