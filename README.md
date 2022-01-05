DBI Git/GitHub protocols
========================

[DallasDBI](https://github.com/DallasDBI) is the official GitHub organization for the City of Dallas's Office of Data Analytics and Business Intelligence, or DBI for short. This Organization serves as a central hub for DBI staff members to collaborate with one another and to provide public transparency into their work. This repository houses documentation outlining the Organization's structure and governance, as well as guidelines for staff members intending to use GitHub for their work.

- If you are a DBI staff member, please contact an Owner for an invitation to join the DallasDBI Organization.
- If you are new to Git or GitHub, refer to the [DBI Git Tutorial](https://github.com/DallasDBI/DBI_Git_Tutorial) for a brief introduction.
- If you are a member of the general public, please feel free to browse or clone any of our public repositories. You may also be interested in the [Open Data Portal](https://www.dallasopendata.com/), the City of Dallas's official portal for various kinds of municipal data.

Overview
--------

### Member privileges

In order to minimize potential privacy and security issues, each user within DallasDBI will be assigned one of two roles:

1. **Member** - The default role. Members will have the following privileges:
    - Clone and pull all DallasDBI repositories, both public and private
2. **Organization Owner** - Administrators. Owners will have all of the privileges granted to Members, and will additionally have the ability to:
    - Create DallasDBI repositories
    - Write and push to DallasDBI repositories
    - Change visibility of repositories (public vs. private)
    - Delete and transfer ownership of repositories
    - Grant Member access to specific repositories
 
### Repository Roles

In addition to general Member privileges, DallasDBI Members may be granted additional permissions for specific repositories via Repository Roles. These roles will generally be one of:

1. **Read** - Read and clone repositories. Open and comment on issues and Pull Requests. This is the default role for all Members.
2. **Write** - Same permissions as Read, plus the ability to write and push to the repository.
3. **Admin** - Same permissions as Write, plus additional functionality pertaining to GitHub features such as Pull Requests, Issues, etc.

### Creating Repositories

Only Owners can create repositories. Members can request a new repository by contacting an Owner, who will create a ***private*** repository and grant appropriate roles to the requestor and other teammates as necessary.

### Changing Repository Visibility

All repositories will be set to private by default, meaning they will only be visible to DallasDBI members. Members can request to change a repo's visibility by contacting an Owner.

Requests to change *private* repositories to *public* must be approved by the DBI Director. 

Requests to change *public* repositories to *private* should be considered urgent, e.g. in response to a security breach, and the Owner should make the change immediately.

### Deleting or Transferring Repositories

Only Owners can delete or transfer ownership of a repository.

Best Practices
--------------

### General guidelines

- *Do not* commit sensitive information or data to a repo.
- Try to only commit plaintext files such as scripts, code, and READMEs. Images and PDFs are also fine provided they do not contain sensitive info. Data files such as csvs should be scrubbed of identifying or private information before committing.
- Consider using GitHub's [2-factor authentication](https://docs.github.com/en/authentication/securing-your-account-with-two-factor-authentication-2fa/about-two-factor-authentication) to secure your account.

### .gitignore

A standard .gitignore file can be found in this repo, which excludes files that frequently contain sensitive data or are otherwise unsuitable for version control, such as csvs and Tableau workbooks. It is recommended that you always include a .gitignore file with every repo you create, to ensure you do not publish secure information.

An alternative approach is to use a .gitignore like this:

    # .gitignore
    *
    
This will cause Git to ignore *all* files within a repo. You will then need to use `git commit -f [YOURNEWFILE.EXT]`, or the equivalent action in your Git GUI each time you want to track a new file. Changes to files that are already tracked by Git can still be committed without using the `-f` option.

### Commit messages

Commit messages should be concise and informative. A good rule of thumb is the [50/72 rule](https://www.midori-global.com/blog/2018/04/02/git-50-72-rule), whereby the first line of the commit message is a short, 50 character summary of changes, optionally followed by any number of 72-character lines providing additional context.

For more guidance on writing commit messages, refer to [How to Write a Git Commit Message](https://cbea.ms/git-commit/) and [Effective Git Commits in Data Science](https://ericmjl.github.io/essays-on-data-science/workflow/effective-commit-messages/).

