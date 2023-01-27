# 1. Via Up-Study
Required fields: `email`, `username`, `password`, `repeated_password` <br>
message with the confirmation link would be sent to your email <br>
until you confirm the email the user is not active

# 2. Invite User via admin panel
The same as [1. Via Up-Study](#1-via-up-study), but user will get administration's permissions

# 3. Invite User via invitation link
The link would be created and bind to the user who invites.
Both of users (inviting and invited) should get some benefits
Link can be generated, deleted, regenerated
Link is unique and one per user profile

# 4. Send invitation via email
Inviting user via email you're doing the same thing as if you just [send the link](#3-invite-user-via-invitation-link), 
but by email with a designed invitation template
