# Tutorial: Sync GitHub with Visual Studio Code

This tutorial will guide you through the steps to synchronize your GitHub repository with Visual Studio Code (VS Code). By following this process, your local changes will seamlessly reflect on GitHub, ensuring your project is always up to date.

---

## **1. Install and Set Up Git**

1. **Download Git**: Install Git from [git-scm.com](https://git-scm.com/).
2. **Verify Installation**:
   ```bash
   git --version
   ```
3. **Set Your Git Identity**:
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "your_email@example.com"
   ```

---

## **2. Create a New Repository on GitHub**

1. Log in to [GitHub](https://github.com/).
2. Click on the **"New"** button to create a new repository.
3. Fill in the repository details:
   - Repository name.
   - Add a description (optional).
   - Set it to **Public** or **Private**.
4. (Optional) Initialize with a README file.
5. Click **"Create Repository"**.

---

## **3. Open Your Project in Visual Studio Code**

1. Launch VS Code.
2. Open your project folder:
   - **File > Open Folder** and select your project directory.

---

## **4. Initialize Git in Your Local Project**

1. Open the terminal in VS Code:
   - **View > Terminal** or press `Ctrl + \` (Windows/Linux) or `Cmd + \` (Mac).
2. Run the following commands:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   ```

---

## **5. Link Your Local Repository to GitHub**

1. Copy the repository URL from GitHub:
   - Go to your repository page and click the **"Code"** button, then copy the HTTPS URL.
2. Link your local repository to GitHub:
   ```bash
   git remote add origin <repository_url>
   ```
   Replace `<repository_url>` with the copied URL.
3. Push your changes to GitHub:
   ```bash
   git branch -M main
   git push -u origin main
   ```

---

## **6. Sync Changes Between VS Code and GitHub**

### **When Making Changes Locally**

1. Save your changes.
2. Stage and commit changes:
   ```bash
   git add .
   git commit -m "Your commit message"
   ```
3. Push changes to GitHub:
   ```bash
   git push
   ```

### **When Pulling Changes from GitHub**

1. To fetch updates from GitHub, run:
   ```bash
   git pull
   ```

---

## **7. Automate Git Commands in VS Code**

1. **Source Control Panel**:
   - Click the **Source Control** icon on the left sidebar.
   - Stage changes by clicking the `+` next to the modified files.
   - Commit changes by typing a message in the input box and clicking the **checkmark**.
2. **Push and Pull**:
   - Use the ellipsis menu (`...`) in the Source Control panel to select **Push** or **Pull**.

---

## **8. (Optional) Set Up SSH for Authentication**

1. Generate an SSH key:
   ```bash
   ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
   ```
2. Copy the public key:
   ```bash
   cat ~/.ssh/id_rsa.pub
   ```
3. Add the SSH key to GitHub:
   - Go to **GitHub > Settings > SSH and GPG Keys > New SSH Key**.
   - Paste the public key and save.
4. Test the SSH connection:
   ```bash
   ssh -T git@github.com
   ```

---

## **9. Verify and Troubleshoot**

- Check the status of your Git repository:
  ```bash
  git status
  ```
- Preview staged changes before committing:
  ```bash
  git diff --staged
  ```
- If you encounter issues, use the following to reset:
  ```bash
  git reset
  ```

---

By following this tutorial, you can ensure that your local VS Code project stays in sync with your GitHub repository. Let me know if you need any further assistance!
