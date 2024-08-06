# Set up SSH authentication for GitHub

The following should cover the basics. If you need further help, se link at the bottom of the page.

## Check for Existing Keys

   Before generating a new key pair, check if you already have an existing SSH key. Run the following command in your terminal:

`ls -al ~/.ssh`

Look for files named `id_rsa` (private key) and `id_rsa.pub` (public key). You might also have a keys named `id_ecdsa` or ``
id_ed25519` with their corresponding public keys. 

## Generate a New Key Pair

If you don't have existing keys or wish to generate a new pair, use the following command to generate one:

`ssh-keygen -t rsa -b 4096 -C "your_email@example.com"` 

Replace `"your_email@example.com"` with your GitHub-associated email. When prompted to "Enter a file in which to save the key," press Enter. This accepts the default file location.

## Upload Public Key to GitHub

Now you need to copy the public key to your clipboard: (replace the file path, if you have a keypair with different names)

On Mac, you can run `pbcopy < ~/.ssh/id_rsa.pub`.
On Windows, you can run `clip < ~/.ssh/id_rsa.pub`.

Alternatively, you can open the file in your favorite text editor or run `cat ~/.ssh/id_rsa.pub` to print it out to the terminal and copy it from there.

Now go to your GitHub account settings, navigate to "SSH and GPG keys," and click "New SSH key." Paste the copied key into the provided field and add a descriptive title.

## Test the Connection

To ensure the key is correctly configured, test the SSH connection to GitHub:

`ssh -T git@github.com`

If successful, you'll receive a message like "Hi username! You've successfully authenticated...". If it is the first time you connect to GitHub you might get a "Unknown host" warning, just type "yes" to continue.

## Clone Using SSH

To clone repositories using SSH, use the SSH URL provided on the GitHub repository page. For example:

`git clone git@github.com:username/repository.git`

Replace `username/repository` with the actual repository name.

For more detailed instructions or troubleshooting, refer to the [GitHub's SSH key setup guide](https://docs.github.com/en/authentication/connecting-to-github-with-ssh).
