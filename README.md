# Stock Portfolio Suggestion Engine

## Team workflow

Use this team workflow every time:

```text
main (stable shared code)
  ↓ pull latest
your own branch
  ↓ code + test
commit changes
  ↓ push branch
Pull Request
  ↓ teammate review / resolve conflicts
merge into main
```

1. Before starting work, update your local copy:

   ```bash
   git switch main
   git pull origin main
   ```

2. Create a branch for one focused task:

   ```bash
   git switch -c feature/employee-management
   ```

   Examples: `feature/schedule-view`, `feature/shift-validation`, `fix/time-overlap`.

3. Make changes only related to that task. Test them before committing.

4. Check what changed:

   ```bash
   git status
   git diff
   ```

5. Save a clear checkpoint:

   ```bash
   git add .
   git commit -m "Add employee creation form"
   ```

6. Push your branch:

   ```bash
   git push -u origin feature/employee-management
   ```

7. On GitHub, open a Pull Request from your branch into `main`. Ask one teammate to review it before merging.

8. After the PR is merged, everyone updates their local `main` again before starting another task.

To avoid conflicts:

- One person owns a file or feature at a time. Announce it in your group chat first.
- Keep branches small and short-lived—finish and merge one feature before starting a large unrelated one.
- Do not work directly on `main`.
- Pull from `main` before creating a new branch.
- If someone merges while you are working, update your branch before opening the PR:

  ```bash
  git fetch origin
  git merge origin/main
  ```

If Git reports a conflict, do not guess: open the marked file, discuss which version should stay with the teammate who edited it, then resolve and commit the result.

