# Git Commands  
Before we get started, head to [git-scm.com](https://git-scm.com) and download Gitbash.  
Ensure you created your GitHub account with "_name_@dsa.tshimologong.joburg" and your username is "_name_-tshimologong"  
  
## 1 Linking our workstation to GitHub

  **Step 1 - Generating SSH keys** 
  Open Gitbash  
  ```shell
  ssh-keygen -t ed25519 -C "<name>@dsa.tshimologong.joburg"
  ```  
  ![ssh-keygen](https://user-images.githubusercontent.com/98871804/154627922-93b2c1be-f119-4b51-8c10-c83fe9e64bc3.png)  
  _! arguements explained_  
  `ssh-keygen` - This will generate a generic rsa encrypted keys type but want our connection to be secured with a different encryption.  
  `-t ed25519` - Here we specify the type of the encryption method. We use `ed25519` as it is recommended over `rsa`.    
  `-C "email"` - This is a comment, it keeps track of the client that created the SSH keys.  
  
  Follow the prompts and leave the SSH keys location at default and ensure you password protect your SSH keys. I am asked to overwrite my keys because I have created them before.  
  ![ssh prompt](https://user-images.githubusercontent.com/98871804/154628449-b646f1c2-9dca-4faf-bb34-99951dce60d0.png)

  Now our keys are created and stored locally in users/_yourname_/.ssh/id_ed25519.pub. You can open this with notepad and copy the public key.  
  
  Or alternativevely, you can:  
  
  To see your public key, enter  
  ```shell
  cat ~/.ssh/id_ed25519.pub

  ```  
  ![cat](https://user-images.githubusercontent.com/98871804/154633807-fb82a4c6-2aa8-4013-bdc2-2c510db3c811.png)  

  
  To copy your public key to your clipboard, enter  
  ```shell
  cat ~/.ssh/id_ed25519.pub | clip
  ```  
  ****
  
  **Step 2 - Adding SSH keys to GitHub**
  1. Go to GitHub  
  
  
  2. Click on your profile icon  
  ![profile](https://user-images.githubusercontent.com/98871804/154630136-76a4c09e-8978-40a9-9993-100bd095147a.png)   
  

  3. Click **Settings**  
  ![settings](https://user-images.githubusercontent.com/98871804/154629603-60dc67a8-f81d-4b7a-90d3-ab5035573cc4.png)  
  
  
  4. Click **SSH and GPG keys**  
  ![gpg](https://user-images.githubusercontent.com/98871804/154632486-a3fbae26-da8b-4ec4-9791-3a89e6ea9bc4.png)  
  
  
  5. Click on **New SSH Key**  
  ![New SSH](https://user-images.githubusercontent.com/98871804/154635157-17ccdadf-1103-41f8-9ded-03a607e64975.png)  
  

  6. Paste the keys generated from Gitbash and Add SSH key  
  ![add key](https://user-images.githubusercontent.com/98871804/154635629-6f8c46e1-2ac8-4b26-ab5c-932762142d7d.png)  

  
  **Step 3 - Test if your keys were added successfully**  
  To test if GitHub successfully added our keys we have to SSH into their port 22 to see if their servers recognise our SSH key  
  ```shell
  ssh -T git@github.com
  ```  
  If our keys were successfully added, we must get our username as a response  
  ![test](https://user-images.githubusercontent.com/98871804/154641101-dc1c0a31-a87f-4909-bf8b-0bd1e0e2881a.png)  
  
  _If you are adding your keys for the first time you will get a GitHub login window._  
  Git
