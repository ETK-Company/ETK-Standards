# How to Contribute

## ETK Git Branch Standards:
There are two permanent branches `main`, and `test`, along side two non-permanent branches `feature/` and `fix/`.

### The `main` Branch:
- This is a protected branch, only selected people can merge onto the main branch.

### The `test` Branch:
- Where all finalized features get merged.

### The `feature/` Branch:
- This branch is created whenever working on a new feature.
- When creating this branch, you add the feature name to the end of the branch. e.g. `feature/examplefeat`

### The `fix/` Branch:
- This branch is created whenever resolving an issue in one of the test branches.
- When creating this branch, you add the issue name to the end of the branch. e.g. `fix/exampleissue`

## ETK git commit Standards:
Every commit should have a detailed description with a standard naming scheme (explained below).

### The `git` commit naming scheme:
Every commit name should start with one of these keywords, (all lower case).

- `create`, is used whenever implementing something new, like a calculator function.
- `add`, is used whenever adding something to an already existing feature, like adding multiplication to the calculator function.
- `fix`, whenever a commit has unusable code, like fixing a broken function.
- `re-struct`, used whenever already existing code is polished/re-organised without effecting its functionality, like making the calculator function more easily understandable.
- `remove`, used whenever deleting functionality.
- `doc`, used whenever changing documentation.

If a git commit requires more keywords to describe its operation, then the commit is probably to large, and should be shorten next time, but to do so you can string together multiple keywords. e.g. `re-struct add Re-organised function & Added multiplication`

If you commit half a feature, addition or fix, you can always add `unresolved` to the beginning. And you can keep updating commit, by doing `unresolved 2`, whilst keeping the same Name (description may vary). Once you've finished the commit, you can change the start to `resolved` (with the same name). e.g. `unresolved 3 create Multiplication function`

## ETK programming standards:

Rules to go off of when programming:

- There should be comments explaining every function and feature, while not over-explaining.
- If a problem has multiple ways of implementing it, the most readable solution should be programmed.
- Nesting should be lowered if possible, this improves code readability.
- Code should not be unnecessarily duplicated. Reusable functions should be created when appropriate.
- No private information (like keys), should be committed to the `FRONTEND/`.
