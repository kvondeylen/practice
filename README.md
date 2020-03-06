# practice
def greeting(name):
  print "Hello, " + name
  
def password_req(password):
  if len(password) <= 8 or len(password) >= 17:
    return "Passwords must be between 8 and 17 characters."
  return "Password updated successfully."
