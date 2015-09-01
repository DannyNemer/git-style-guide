# Git Style Guide
The very early beginnings of a Git style guide.

1. Commit summaries should be imperative present tense.
1. Commit summaries should be limited to 50 characters.
1. Commit desciritions should be wrapped to 72 characters.
1. Commits descriptions should have a blank line between paragraphs and bullets.
1. Commits descriptions bullets hsould be properly indented.

  ```shell
  # Bad
  - text text text text text text text text text text text text text text
  text text text text text text text text text text text text text text
  text text text text text text text text text text text text text text

  # Good
  - text text text text text text text text text text text text text text
    text text text text text text text text text text text text text text
    text text text text text text text text text text text text text text
  ```

1. Use backticks for source variable, function, type names.

  ```shell
  # Bad
  Do not use Array in for loops

  # Good
  Do not use `Array` in `for` loops
  ```

1. Use single quotes for file names.

  ```shell
  # Bad
  Add "dantil.js"

  # Bad
  Add dantil.js

  # Good
  Add 'dantil.js'
  ```

1. Use single quotes for strings.

  ```shell
  # Bad
  Set name of `user` to "danny"

  # Good
  Set name of `user` to 'danny'
  ```

1. Use double quotes for strings representing input.

  ```shell
  Handle queries for "People who are not dead"
  ```