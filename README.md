# Tailwind CSS @apply with Non-Existent Class

This repository demonstrates an uncommon error in Tailwind CSS related to the `@apply` directive.  When using `@apply` with a class that is either misspelled or doesn't exist in your Tailwind configuration, it doesn't throw a compilation error but silently fails to apply the style. This can be difficult to debug, as the styling will simply not appear.

## Bug Reproduction

The `bug.html` file shows the issue.  The class `text-wrong-class` is intentionally misspelled, leading to the expected styling not being applied.

## Solution

The `bugSolution.html` file provides a corrected version, demonstrating how to fix the problem by either correctly spelling the class name or ensuring it exists in your `tailwind.config.js` file.

## How to fix:

1. **Careful Class Naming:** Double-check the spelling and ensure all class names are accurate and consistent with your Tailwind configuration.
2. **Linters:** Use a linter (e.g., ESLint with a Tailwind plugin) to help identify potential typos and unused classes.
3. **Purge Unused Styles:** Configure Tailwind to purge unused CSS in production to prevent bloat and potential issues with undeclared classes.