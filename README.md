# 🚀 Getting Started with Frontend Digital Design

This guide helps you set up a Verilog development environment on any OS using **WSL**, **Git**, **Icarus Verilog**, **VSCode**, and the **veriloghdl** extension.

---

## 🛠 Prerequisites
Laptop with 4 GB+ RAM
2 GB+ of Storage.

## 🧰 Prerequiste Setup (Windows Only)

If you are using Windows, it is often easier to develop in a Linux based environment, lots of things from PATH management to the directory format are much simpler in a Unix-based system, saving you time and lettig you focus on what is actually important - creating your first designs!

**1.1** Install VsCode fron the link: [VSCode](https://code.visualstudio.com)

**1.2**  Open PowerShell as Administrator and run:
   ```powershell
   wsl --install
   ```

**1.2a**  Restart your computer if prompted.

**1.3a**  Launch Ubuntu from the Start Menu and create a username/password when prompted.

Inside the WSL terminal, 

```bash
code .
```

This will open VSCode with the WSL remote server, alloowing you to use the Linux
filesystem with ther Windows VSCode app.

From now on, 'Linux' instructions refer to commands entered on in either a Linux or WSL terminal and Mac instructions are for MacOS users.

---

## 🧰 Tool Installation (Linux)

*Linux Tutorial*

In a linux system, you can use the 'apt' package manager to install tools. 'sudo' means SUperuserDO and is like giving yourself admin rights on a Windows machinie.

Common comands
```bash
mkdir testdir
touch hello.txt
cd ./testdir
ls
cd ..
ls
```
Run these and try and figure out what is happening!

**2.1** Update apt and Install Git

```bash
sudo apt update
sudo apt install git
git --version
```

**2.1.1** Configure Git

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```
This tells Git who you are.

**2.1.2** Connect to Github

If you need to access GitHub from Windows Subsystem for Linux (WSL), we recommend using **SSH**.  
After you have generated an SSH key and added the public key to your GitHub account, Git operations will no longer prompt you for a password or any additional verification.

For detailed instructions on generating keys, connecting, and authenticating with GitHub over SSH, please refer to the [official documentation](https://docs.github.com/en/authentication/connecting-to-github-with-ssh).

**2.3** Install Icarus Verilog

```bash
sudo apt install iverilog
iverilog -v
```

## 🧰 Tool Installation (Mac)

**2.1** Install the Homebrew Package manager using this official guide: [Homebrew Installation](https://brew.sh/)

**2.2** Restart the shell.

**2.3** Test installation by running:
```bash 
brew --version
```

You should get a response that is not an error message.

**2.4** Install Git

```bash
brew install git
git --version
```
**2.4.1** Configure Git

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```
This tells Git who you are.

**2.4.2** Connect to GitHub

If you need to access GitHub from Windows Subsystem for **MacOS**, we recommend using **SSH**.  
After you have generated an SSH key and added the public key to your GitHub account, Git operations will no longer prompt you for a password or any additional verification.

For detailed instructions on generating keys, connecting, and authenticating with GitHub over SSH, please refer to the [official documentation](https://docs.github.com/en/authentication/connecting-to-github-with-ssh).

**2.5** Install Icarus Verilog

```bash
brew install iverilog
iverilog -v
```

## 🔧 Setting Up VSCode (All)

3.1 Navigate to the Extensions Panel
3.2 Install [VerilogHDL Extension](https://marketplace.visualstudio.com/items?itemName=mshr-h.VerilogHDL)

3.3 [Select iverilog in this field](vscode://settings/verilog.linting.linter)
   
3.4 in the terminal run
   ```bash
   whereis iverilog
   ```
3.5 copy the first directory that comes up (usually /usr/local/bin) into
[This field](vscode://settings/verilog.linting.path) - Make sure to not include the filename at the end of the path!

## You are now ready to to begin the Tutorial!

begin with the design section and then move on to verification.



