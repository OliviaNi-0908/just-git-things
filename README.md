# Discriptions
---
##### -  


# Setups
---
##### - Connect your local machine to your github through **SSH key**
1. Why? 
    > 1. To push your local git repository to your remote Github repository, you have to prove to Github that you are the owner of your account
2. How?
    **In your local machine:** Generating a new SSH key
    ```sh
        $ cd ~
        $ ssh-keygen -t rsa -b 4096 -C "<YOUR_GITHUG_E-MAIL>"
        $ ll | grep id_rsa  # id_rsa, id_rsa.pub 
    ``` 
    > 1. Keep your private SSH key (**id_rsa**) secure on your local machine, 
    > 2. Upload your public SSH key (**id_rsa.pub**) on your GitHub --> public SSH key is ok for other people to see this key

    **In your local machine:** Adding your SSH key to the ssh-agent
    ```sh
        $ cd ~
        $ eval "$(ssh-agent -s)"
        $ open ~/.ssh/config
            (vim)
                Host *
                  AddKeysToAgent yes
                  UseKeychain yes
                  IdentityFile ~/.ssh/id_rsa
            (:wq)
        $ ssh-add -K ~/.ssh/id_rsa
    ```     
    
    **In your Github:** Uploading the created public SSH key
    > 1. Settings
    > 2. SSH and GPG keys -> New SSH key -> Add SSH key
    > 3. New SSH key
        *- title: id_rsa.pub*
        *- key: paste the id_rsa.pub contents*
    > 4. Add SSH key
    

3. What more?
    >  See [Generating a new SSH key and adding it to the ssh-agent](https://docs.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
    > See [Git and GitHub for Beginners - Crash Course](https://www.youtube.com/watch?v=RGOj5yH7evk)

##### - Configure Mac's Terminal
1. Why? 
    > To configure the Terminal to display helpful information when in a directory that's under  version control
2. How?
3. What more?

