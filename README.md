# Git Style Guide
The beginnings of a Git style guide.

1. Phrase commit summaries in imperative present tense.

  ```perl
  # Bad
  Added test cases

  # Bad
  Adds test cases

  # Good
  Add test cases
  ```

1. Phrase commit descriptions in indicative present tense.

  ```perl
  # Bad
  cli: Refactor `forEach()`

  Defined `forEach()` as an `Array` method instead of a global function.

  # Bad
  cli: Refactor `forEach()`

  Define `forEach()` as an `Array` method instead of a global function.

  # Good
  cli: Refactor `forEach()`

  Defines `forEach()` as an `Array` method instead of a global function.
  ```

1. Limit commit summaries to 50 characters in length.
1. Wrap commit descriptions to 72 characters.
1. Properly indent bullets in commit descriptions.

  ```perl
  # Bad
  - Lorem ipsum dolor sit amet, morbi pede, et vulputate commodo, arcu
  gravida. Condimentum massa mauris viverra id egestas taciti, augue arcu
  quia vel ornare id enim, consectetuer velit odio parturient erat varius
  risus, ultricies tristique lacinia non vivamus, condimentum sit sem.

  # Good
  - Lorem ipsum dolor sit amet, morbi pede, et vulputate commodo, arcu
    gravida. Condimentum massa mauris viverra id egestas taciti, augue
    arcu quia vel ornare id enim, consectetuer velit odio parturient erat
    varius risus, ultricies tristique lacinia non vivamus, condimentum sit
    sem.
  ```

1. Separate paragraphs and list items with a blank line in commit descriptions.

  ```perl
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

  ```perl
  # Bad
  Do not use Array with for loops

  # Good
  Do not use `Array` with `for` loops
  ```

1. Use single quotes for file names.

  ```perl
  # Bad
  Add dantil.js

  # Bad
  Add "dantil.js"

  # Good
  Add 'dantil.js'
  ```

1. Use single quotes for strings.

  ```perl
  # Bad
  Set name of `user` to "danny"

  # Good
  Set name of `user` to 'danny'
  ```

1. When renaming or moving a file, use `git mv` instead of plain `mv`, and omit changes to the file contents because the whole file is marked new regardless. Use `--follow` with `git log` on the renamed file in the future. Use the following syntax for commit summaries when renaming or moving a file.

  ```perl
  Rename 'danny-util.js' → 'dantil.js'
  ```

1. When renaming a public variable or method that requires refactoring across several files, consolidating the refactoring in a single, solitary commit with the following syntax:

  ```perl
  Rename `dantil.printError()` → `dantil.logError()`
  ```

1. When referencing a method in a commit message, prepend its name with the class name.

  ```perl
  # Bad
  Refactor `logError()`

  # Good
  Refactor `dantil.logError()`

  # Good
  Remove use of `Array.prototype.slice()`
  ```

1. When referencing a function or method in a commit message, enclose in backticks and include parentheses (irrespective of arity).

  ```perl
  # Bad
  Refactor `dantil.logError`

  # Good
  Refactor `dantil.logError()`
  ```

1. When committing the addition of a function or method, phrase the commit summary as "Add <function_name>" and include a description of the function in the commit description. Use the full indicative-mood function description for the commit description.

  ```perl
  # Bad
  Add `dantil.logError()` to print errors

  # Good
  Add `dantil.logError()`

  Prints the provided values like `console.log()` prepended with
  red-colored "Error: ".
  ```