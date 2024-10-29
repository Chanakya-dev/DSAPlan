# Setting Up Branch Rules in Repository

To ensure proper code management and control over your main branch, follow these steps to create and enable branch rules.

## Steps to Create Branch Rules

1. **Navigate to Repository Settings:**
   - Go to your repository on GitHub.
   - Click on the `Settings` tab at the top right.

2. **Access Branch Rules:**
   - In the sidebar, find and click on `Branches`.
   - Under "Branch protection rules," click the `Add branch protection rule` button.

3. **Create a Branch Rule:**
   - In the **Branch name pattern** field, enter the branch name you want to apply the rule to.
     - If you want to apply the rule to the main branch, select `Default (main)` in the dropdown.
     - To target a specific branch, select `Include by pattern` and enter the branch name (e.g., `main` or `develop`).

4. **Bypass Permissions (Admin Only):**
   - Scroll down to the **Bypass permissions** section.
   - Enable the `Allow specified actors to bypass required pull requests` option.
   - In the dropdown, select `Organization Admin Role`. This ensures that only admins can push code directly to the branch without a pull request.

5. **Set Branch Protection Rules:**
   - In the **Branch protection rules**, enable the following options:
     - `Restrict deletions`: This prevents accidental deletion of the branch.
     - `Require a pull request before merging`: This ensures all code is reviewed before being merged.

6. **Additional Settings:**
   - Click on `Show additional settings` to reveal more options.
   - Under **Require approvals**, set the number of required approvals to `1`. This ensures that at least one team member reviews the code before merging.
   - Enable the `Block force pushes` option to prevent forced changes to the branch.

7. **Save Changes:**
   - After selecting your rules and settings, scroll down and click the `Create` or `Save changes` button to apply the branch rules.

---
