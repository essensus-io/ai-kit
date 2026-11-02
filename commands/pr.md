Create or update a GitHub PR with a descriptive title using the GitHub CLI. First inspect the branch, working tree, diff, existing PR, and relevant project checks. If a PR already exists for the current branch, update its title and description; otherwise create one.

Do not stage, commit, push, create a branch, or modify unrelated working-tree changes unless the user explicitly asks. State checks actually run and leave unverified checklist items unchecked.

Use the commit-message conventions when proposing a title. Keep the PR body template below; fill the short Summary and Preview sections, and preserve the checklist wording.

Use this title style: `feat(auth): implement user verification screen`

### Template:

```md
## Summary:

## Preview:

<placeholder for screencast>

## Dev checklist:

- [ ] I have performed a self-review of my code
- [ ] I have manually tested this feature to ensure I am not breaking a critical piece of the platform
```

### Example:

Title: Implemented Create Pulse - Share cost flow, added screens and adjusted GraphQL responses

Description:

```md
### Summary:

- Added a new "Activity History" section to the user profile page.
- Implemented a paginated list of user activities with date and description.
- Added a "Load More" button for users with extensive activity history.

## Preview:

https://github.com/user-attachments/assets/3a98a4a6-b820-4286-92ab-ce41f3bf297c

## Dev checklist:

- [ ] I have performed a self-review of my code
- [x] I have manually tested this feature to ensure I am not breaking a critical piece of the platform
```
