DBI Git/GitHub protocols
========================

The [DallasDBI Organization](https://github.com/DallasDBI) is a free-tier account hosted on GitHub. This account will serve as a central hub for DBI staff members to collaborate and provide public transparency into their work. This document provides an outline of the Organization's structure and guidelines for staff members intending to use GitHub for their work. This is *not* intended to be a git or GitHub training document. Staff members in need of training should refer to the DBI GitHub Training repo.

Security and access controls
----------------------------

### Member privileges

In order to minimize potential privacy and security issues, each user within the DallasDBI Organization will be assigned one of two roles defining access permissions within the Organization.

1. **Member** - The default role. Members will have all of the following privileges:
    - Clone and pull public repositories
2. **Organization Owner** - Administrators. Owners will have all of the privileges granted to Members, and will additionally have the ability to:
    - Create public and private repositories
    - Push to public and private repositories
    - Change visibility of repositories (public vs. private)
    - Delete and transfer ownership of repositories
    - Grant Member access to specific repositories
 
### Repository Roles

For any given repository, Owners may assign Members to various predefined roles granting them additional permissions. These roles will generally be one of:

1. **Read** - Read and clone repositories. Open and comment on issues and Pull Requests.
2. **Write** - Same permissions as Read, plus the ability to write and push to repositories.
3. **Admin** - Same permissions as Write, plus additional functionality pertaining to GitHub features such as Pull Requests, Issues, etc.

Getting Started
---------------

### Joining the Organization

Once you have created an account, contact an Owner to receive an invitation to join the DallasDBI Organization

### Creating Repositories

Only Owners can create repositories. Members can request a new repository by contacting an Owner, at which point the Owner will create a ***private*** repository and grant appropriate roles to the requestor and other teammates as necessary.

### Changing Repository Visibility

All repositories will be private by default, meaning they will only be visible to the Owner and Members with an appropriate Repository Role. Members can request to change a repo's visibility by contacting an Owner.

Requests to change *private* repositories to *public* must be approved by the DBI Director. Requests to change *public* repositories to *private* should be considered urgent, e.g. in response to a security breach, and the Owner should make the change immediately.

### Deleting or Transferring Repositories

Only Owners can delete or transfer ownership of a repository. In general, these functions will likely never be used, as any potential security violations necessitating repo deletion can usually be resolved by making the the repo private.

Best Practices
--------------

### General guidelines

- *Do not* commit sensitive information or data to a repo.
- Try to only commit plaintext files such as scripts, code, and READMEs. Images and PDFs are also fine provided they do not contain sensitive info. Data files such as csvs should be scrubbed of identifying or private information before committing.
- Use GitHub's 2-factor authentication to secure your account.
- Unless you are exclusively using GitHub's web interface to work on a repo, use SSH when cloning, pushing, or pulling remotes. See GitHub's [Connect with SSH](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/about-ssh) help pages for details.

### .gitignore

A standard .gitignore file can be found in this repo, which excludes files that frequently contain sensitive data or are otherwise unsuitable for version control, such as csvs and Excel workbooks. It is recommended that you always include a .gitignore file with every repo you create, to ensure you do not publish secure information.

An alternative approach is to use a .gitignore like this:

    # .gitignore
    *
    
This will cause git to ignore *all* files within a repo. You will then need to use `git commit -f [YOURNEWFILE.EXT]`, or the equivalent command in your git GUI each time you want to track a new file. Changes to files that are already tracked by git can still be committed without using the `-f` option.

