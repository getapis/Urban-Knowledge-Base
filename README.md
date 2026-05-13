# Urban Muay Thai Knowledge Base

Static knowledge base for Urban Muay Thai operations and SOPs.

## GitHub Pages Deployment

1. Commit the full project, including `index.html`, `assets/`, and `data/`.
2. In GitHub, open the repository settings.
3. Go to **Pages**.
4. Set the source to the branch you want to publish, usually `main`.
5. Set the folder to `/root`.
6. Save and wait for GitHub Pages to publish the site.

## Persistent Content

Content is stored in version-controlled JSON files:

- `data/categories.json`
- `data/articles.json`

The website reads from these files on load. Online article/category edits are blocked until **GitHub sync** is configured in the site. GitHub sync commits changes back into the JSON files through the GitHub API, so edits can be tracked in normal GitHub history.

## GitHub Sync Token

Create a fine-grained GitHub token with **Contents: Read and write** permission for this repository only. Enter it in the site's **GitHub sync** modal after unlocking the site.

Do not hard-code this token into the project.

## Security Note

The built-in password gate is client-side access control. It is useful for light privacy, but it is not a secure authentication system for sensitive information.
