# Purpose
To push your local git repository to your remote Github repository, you have to prove to Github that you are the owner of your account.


# Setup Steps
* In your local machine:
  1. Generate a new SSH key
     ~~~sh
     $ cd ~
     $ ssh-keygen -t rsa -b 4096 -C "<YOUR_GITHUG_E-MAIL>"
     $ ll | grep id_rsa  # id_rsa, id_rsa.pub
     ~~~
     * Keep your private SSH key (id_rsa) secure on your local machine
     * Upload your public SSH key (id_rsa.pub) on your GitHub --> public SSH key is ok for other people to see this key

* In your Github:
  2. Uploading the created public SSH key
     Go to `Settings -> SSH and GPG keys -> New SSH key -> Add SSH key'
     * Paste the following contents in the `New SSH key` step
       * title: id_rsa.pub
       * key: paste the `id_rsa.pub` contents

* In your local machine:
  3. Adding your SSH key to the ssh-agent
     ~~~sh
     $ cd ~
     $ eval "$(ssh-agent -s)"
     $ open ~/.ssh/config
     ~~~
     * paste the following contents in the ~/.ssh/config
     ```
     Host *
       AddKeysToAgent yes
       UseKeychain yes
       IdentityFile ~/.ssh/id_rsa 
     ```
     ~~~sh
     $ ssh-add -K ~/.ssh/id_rsa
     $ ssh -T git@github.com     
     ~~~


# More Details:
* See [Generating a new SSH key and adding it to the ssh-agent](https://docs.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)

