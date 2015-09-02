# Git Style Guide
The very early beginnings of a Git style guide.

1. Commit summaries should be in imperative present tense.
1. Commit summaries should be limited to 50 characters.
1. Commit descriptions should be wrapped to 72 characters.
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
1. Use blank lines between paragraphs and bullets and commit descriptions.

  ```shell
  # Bad
  Lorem ipsum dolor sit amet, morbi pede, et vulputate commodo, arcu gravida:
  - Condimentum massa mauris viverra id egestas taciti, augue arcu quia vel
    ornare id enim, consectetuer velit odio parturient erat varius risus,
    ultricies tristique lacinia non vivamus, condimentum sit sem.
  - Diam at duis suspendisse ipsum, leo est vestibulum dui aliquam, enim wisi,
    varius arcu, quam morbi cursus quia lacinia per. Ac tellus sit integer et,
    tortor rutrum velit, molestie purus.

  # Good
  Lorem ipsum dolor sit amet, morbi pede, et vulputate commodo, arcu gravida:

  - Condimentum massa mauris viverra id egestas taciti, augue arcu quia vel
    ornare id enim, consectetuer velit odio parturient erat varius risus,
    ultricies tristique lacinia non vivamus, condimentum sit sem.

  - Diam at duis suspendisse ipsum, leo est vestibulum dui aliquam, enim wisi,
    varius arcu, quam morbi cursus quia lacinia per. Ac tellus sit integer et,
    tortor rutrum velit, molestie purus.
  ```

1. Use backticks for source variable, function, and type names.

  ```shell
  # Bad
  Do not use Array with for loops

  # Good
  Do not use `Array` with `for` loops
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

1. When renaming or moving a file, use `git mv`, not just `mv`, and ensure there are no other changes in the contents of the files as the whole file will be marked as new regardless. Use `--follow` when using `git log` or other commands on the renamed file in the future. Use the following syntax when renaming or moving a file.

  ```shell
  Rename 'danny-util.js' → 'dantil.js'
  ```

1. When renaming a public variable or function, requiring refactoring across several files, make that change a single commit. Use the following syntax:

  ```shell
  Rename `dantil.printError()` → `dantil.logError()`
  ```

1. When referencing a function in a commit message, prepend the function's name with the class name.
  ```shell
  # Bad
  Refactor `logError()`

  # Good
  Refactor `dantil.logError()`
  ```

1. When referencing a function in a commit message, use backticks and parenthesis (irrespective of the number of the function's parameters).

  ```shell
  # Bad
  Refactor `dantil.logError`

  # Good
  Refactor `dantil.logError()`
  ```

1. When adding a new function, state only "Add <function_name>" as the commit summary, but a description of the function in the commit description. Use the full indicative-mood function description for the commit description.

  ```shell
  # Bad
  Add `dantil.logError()` to print errors

  # Good
  Add `dantil.logError()`

  Prints the provided values like `console.log()` prepended with
  red-colored "Error: ".
  ```