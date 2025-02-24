---
id: "Activity: Create a conditional statement"
aliases: []
tags: []
---

Tags: [[google_cybersecurity]]

## Task 8

To complete Task 8, you'll use the variable `organization_hours` to check whether a user logged in during the designated time. The structure will involve a simple conditional that evaluates whether a `login_time` (representing the time of login) falls within the allowed hours.

Below is the completed code:

```python
# Assign `organization_hours` to a tuple that represents start and end hours of organization hours (in 24-hour format)
organization_hours = (9, 17)  # 9 AM to 5 PM

# Assign `login_time` to the hour (in 24-hour format) when the login attempt was made
login_time = 18  # Example: 6 PM

# If the login time is within organization hours, display an appropriate message
# Otherwise, display a message indicating the login attempt was outside organization hours

if organization_hours[0] <= login_time < organization_hours[1]:
    print("Login attempt made during organization hours.")
else:
    print("Login attempt made outside of organization hours.")
```

### Explanation

1. **`organization_hours` variable**:

   - This variable is a tuple `(start_hour, end_hour)` representing the range of allowed login hours.
   - Example: `(9, 17)` represents 9 AM to 5 PM.

2. **`login_time` variable**:

   - Stores the hour (in 24-hour format) when the user attempted to log in.

3. **Condition**:

   - The `if` condition checks if the `login_time` falls within the range defined by `organization_hours`.
   - Uses the `<=` and `<` operators for inclusivity at the start (`9 <= login_time`) and exclusivity at the end (`login_time < 17`).

4. **Output**:
   - If the condition evaluates to `True`, it prints: `"Login attempt made during organization hours."`
   - Otherwise, it prints: `"Login attempt made outside of organization hours."`

### Example Scenarios

- **Input**: `login_time = 10`
  **Output**: `"Login attempt made during organization hours."`

- **Input**: `login_time = 18`
  **Output**: `"Login attempt made outside of organization hours."`

Would you like me to provide a combined script that integrates this task with Tasks 6 and 7?
