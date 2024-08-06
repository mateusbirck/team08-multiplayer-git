# Setting Up Authentication with Personal Access Tokens (PAT)

Use Personal Access Tokens for secure authentication when accessing GitHub repositories.

## Generate a Personal Access Token

- Go to your GitHub account settings, then navigate to "Developer settings" > "Personal access tokens." (or just go to <https://github.com/settings/tokens> directly)
- Click "Generate new token" and provide a meaningful note.
- Select the scopes (permissions) you need. IN this case, the topmost `repo` does the job.
- Select an *Expiration* time. For security, it's best to keep the token valid for as short a time as possible, and for this workshop, you can set it to expire in 1 day. You can always generate a new token later.
- Click "Generate token" and copy the generated token to a safe place.

## Store the Token Securely

   Keep your token confidential. Do not share it publicly or hard-code it in scripts. Use environment variables or a secure credentials manager.

## Authenticate with the Token

When using Git on the command line, you'll use your token (PAT) instead of your password for authentication.
Replace your password with the token when prompted. To avoid doing this for every push, you can set up a Git credential helper. There are multiple options for this, including the [built-in Git credential manager](https://git-scm.com/docs/gitcredentials) and [third-party credential managers](https://git-scm.com/book/en/v2/Git-Tools-Credential-Storage).

**The easiest solution for the purpose of this exercise, is to use the cache option of the built-in Git credential manager**: (leave out `--global` if you want to set this up for a single repository)

```bash
git config --global credential.helper cache
git config --global credential.helper 'cache --timeout=7200'
```

This just tells Git to remember your password for the 2 hours which is probably enough for this exercise.

## Clone Repositories

Clone repositories using the HTTPS URL provided on the GitHub repository page.

## Token Revocation and Management

- If a token is compromised or no longer needed, revoke it in your GitHub account settings.
- Regularly review and manage your tokens to ensure security.

For more details or troubleshooting, consult [GitHub's PAT authentication guide](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token).
