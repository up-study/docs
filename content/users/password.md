# 1. Change Password
require `old_password`, `new_password`, `repeated_password`
# 2. Reset Password
require `email`, would be sent a message to this email with the link to set a new password, you need to fill `repeated_password` field as well
# 3. Password validators
 - at least 8 chars
 - not only numeric
 - should match to email/username/e.t.c
