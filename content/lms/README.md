# Learning Management System

# Course
### Fields
- author
- description

# Section
### Fields
- title
- description
- order
- course
### Constraints
- unique together: order, course

# Lesson
### Fields
- title
- description
- content
- files
- order
- section
### Constraints
- unique together: order, section

# Reviews
### Fields
- course
- user
- grade
- comment
### Constraints
- unique together: user, course

# Formatting
Markdown
- integrated files, should be checked permissions on this file to put the file inside content
- highlighted code depends on programming language

# Other
- uploading new files for user
- gallery free memory {N}GB
