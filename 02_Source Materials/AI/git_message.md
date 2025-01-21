**Language > Specialist**: Markdown > Commit Message Specialist  
**Includes**: Semantic prefixes, concise action descriptions  
**Requirements**: Focus on clarity, action-oriented messages, and a consistent style for commits  

## Plan
1. Propose a reusable, structured commit message template.
2. Suggest commonly used prefixes for different purposes (e.g., feature addition, bug fix).
3. Provide examples for clarity.

---

Here is a structured commit message template you can adopt for consistency across repositories:

### Commit Message Template
```
<type>: <summary>

[Optional] <Context or reason for the change>

[Optional] <Further details>
```

### Recommended Prefixes
1. **For Features**:
   - `Add:` For adding a new feature.
   - `Enhance:` For improving an existing feature.

   Example:
   ```
   Add: User authentication system

   Implemented login, logout, and signup features using Django's built-in authentication module.
   ```

2. **For Fixes**:
   - `Fix:` For bug fixes.
   - `Resolve:` For addressing specific issues or tasks.

   Example:
   ```
   Fix: Incorrect date parsing in reports

   Updated the `parse_date` function to handle edge cases for ISO 8601 formats.
   ```

3. **For Refactoring**:
   - `Refactor:` For code improvements without changing functionality.

   Example:
   ```
   Refactor: Simplify database query logic

   Merged redundant ORM queries into a single optimized query for better performance.
   ```

4. **For Documentation**:
   - `Docs:` For updating or creating documentation.

   Example:
   ```
   Docs: Update README with API usage instructions

   Added examples for integrating with third-party services.
   ```

5. **For Chores**:
   - `Chore:` For routine tasks like dependency updates, build setup, etc.

   Example:
   ```
   Chore: Upgrade to Python 3.12

   Updated requirements and tested compatibility with Python 3.12.
   ```

6. **For Tests**:
   - `Test:` For adding or improving tests.

   Example:
   ```
   Test: Add unit tests for the payment gateway integration
   ```

### Guidelines for the Summary
- Use the present tense (e.g., "Fix", "Add").
- Keep it under 50 characters for clarity.

Does this approach work for your needs, or would you like to customize it further?
