# Git Commands  
Before we get started, head to [git-scm.com](https://git-scm.com) and download Gitbash.  
Ensure you created your GitHub account with <name>@dsa.tshimologong.joburg and your username is <name>-tshimologong  
  
## 1 Linking our workstation to GitHub

  **Step 1 - Generating SSH keys** 
  Open Gitbash  
  ```shell
  ssh-keygen -t ed25519 -C "<name>@dsa.tshimologong.joburg"
  ```
  _! arguements explained_  
  `ssh-keygen` - This will generate a generic rsa encrypted keys type but want our connection to be secured with a different encryption.  
  `-t ed25519` - Here we specify the type of the encryption method. We use `ed25519` as it is recommended over `rsa`    
  `-C "email"` - This is a comment that we can logged from GitHub servers and will return the client that created the SSH keys  
  
  Follow the prompts and leave the SSH keys location at default and ensure you password protect your SSH keys.
  
  Now our keys are created and stored locally in users/_yourname_/.ssh/id_ed25519.pub. You can open this with notepad and copy the public key. Or alternativevely, you can:  
  To see your public key, enter 
  ```shell
  cat ~/.ssh/id_ed25519.pub
  ```

  
