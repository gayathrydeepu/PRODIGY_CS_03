def check_password_strength(password):
  """Evaluates password strength based on multiple criteria.

  Args:
      password: The password to check.

  Returns:
      A tuple containing:
          - strength (int): Password strength score (0-4)
          - feedback (str): Description of password strength
  """
  strength = 0
  feedback = ""

  # Check password length
  if len(password) >= 12:
    strength += 1
    feedback += "Length is good (12+ characters).\n"
  elif len(password) >= 8:
    feedback += "Length is fair (8-11 characters).\n"
  else:
    feedback += "Password is too short. Use at least 8 characters.\n"

  # Check for uppercase letters
  if any(char.isupper() for char in password):
    strength += 1
    feedback += "Contains uppercase letters.\n"

  # Check for lowercase letters
  if any(char.islower() for char in password):
    strength += 1
    feedback += "Contains lowercase letters.\n"

  # Check for numbers
  if any(char.isdigit() for char in password):
    strength += 1
    feedback += "Contains numbers.\n"

  # Check for special characters
  if any(char in "!@#$%^&*()_+-=[]{};':|\,.<>/? " for char in password):
    strength += 1
    feedback += "Contains special characters.\n"

  # Assign feedback based on strength score
  if strength == 0:
    feedback += "This password is very weak. Please consider using a stronger one."
  elif strength == 1 or strength == 2:
    feedback += "This password is somewhat weak. Consider adding more complexity."
  elif strength == 3:
    feedback += "This password is moderately strong."
  else:
    feedback += "This password is strong."

  return strength, feedback

# Get user input
password = input("Enter your password: ")

# Check password strength
strength, feedback = check_password_strength(password)

# Print feedback
print(f"\nPassword Strength: {strength}/4")
print(feedback)
