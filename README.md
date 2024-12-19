# Setting Up Your Python Code Base on a Mac
Author: Matt Hardy, 12/19/2024
## Table of Contents
- [Introduction](#introduction)
- [Downloading and Installing Anaconda](#downloading-and-installing-anaconda)
  - [Step 1: Download Anaconda](#step-1-download-anaconda)
  - [Step 2: Install Anaconda](#step-2-install-anaconda)
- [Configuring Your Anaconda Environment](#configuring-your-anaconda-environment)
  - [Step 1: Open Terminal](#step-1-open-terminal)
  - [Step 2: Initialize Conda](#step-2-initialize-conda)
  - [Step 3: Update Conda](#step-3-update-conda)
  - [Step 4: Create a Virtual Environment](#step-4-create-a-virtual-environment)
  - [Step 5: Activate the Environment](#step-5-activate-the-environment)
  - [Step 6: Verify Installation](#step-6-verify-installation)
- [Important Notes](#important-notes)

---

## Introduction
This guide will walk you through setting up your Python coding environment on a Mac. We will use Anaconda, a powerful tool for managing Python installations and virtual environments. Follow these steps carefully to ensure that your system is ready for your coursework.

**Important:** You will always use your Mac's integrated Terminal for these steps. Do not use the "Anaconda Navigator" graphical interface for any part of this process.

**Note:** Multi-line code blocks in this guide are intended to be run **one line at a time**. Copying and pasting the entire block at once may result in errors.

## Downloading and Installing Anaconda

### Step 1: Download Anaconda
1. Navigate to the [Anaconda Download Page](https://www.anaconda.com/download/success) and select the latest version of Anaconda for macOS.
2. Click the download button for **MacOS Installer** (64-Bit, Apple silicon, Graphical Installer, 704.7M) under the "Anaconda Installers" section.

### Step 2: Install Anaconda
1. Once the installer is downloaded, double-click on the file to run it.
2. Follow the installation wizard steps:
   - Accept the license agreement.
   - Leave the installation directory as default unless you have a specific need to change it.
3. Finish the installation by clicking the "Install" button. Once complete, click "Finish."

---

## Configuring Your Anaconda Environment

### Step 1: Open Terminal
1. Open the Spotlight Search by pressing `Cmd + Space`, type **Terminal**, and press `Enter`.

### Step 2: Initialize Conda
1. Run the following command to enable Conda in your Terminal:
   ```bash
   conda init zsh
   ```
   - If you're using an older version of macOS and running `bash` instead of `zsh`, replace `zsh` with `bash` in the command.
2. Close your Terminal and reopen it for the changes to take effect.

### Step 3: Update Conda
1. Run the following commands to ensure Conda and Anaconda are up-to-date:
   ```bash
   conda update conda
   conda update anaconda
   ```
   Run each line individually by pressing `Enter` after each command.
2. Press `y` when prompted to confirm updates.

### Step 4: Create a Virtual Environment
1. Create a new virtual environment named `dev` using Python 3.10:
   ```bash
   conda create -n dev python=3.10 anaconda -y
   ```
   Run this command as a single line.
   - This environment will include all necessary default packages, such as NumPy, Pandas, and Matplotlib.

### Step 5: Activate the Environment
1. Activate your new environment by entering:
   ```bash
   conda activate dev
   ```
2. Your prompt should now include `(dev)` at the beginning, indicating that the environment is active.

### Step 6: Verify Installation
1. Verify that the necessary packages are installed by running:
   ```bash
   conda list
   ```
   Run this command as a single line.
2. Confirm that the following packages are listed:
   - Numpy
   - Pandas
   - Matplotlib

---

## Important Notes
- Always activate the `dev` environment before running Python code by entering:
  ```bash
  conda activate dev
  ```
- If you need to exit the environment, use:
  ```bash
  conda deactivate
  ```
- Remember to keep Conda updated periodically to avoid compatibility issues.
- Use the **Terminal** exclusively for managing environments and running commands as described in this guide.

With this setup, you are now ready to begin your coursework. If you encounter any issues, reach out to your instructional staff for assistance.

