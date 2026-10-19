# Ancora-Education-Ucertify-Lab53
# Managing User Accounts

> **Original Lab Source**
> 
> This lab was available through:
>
> [https://ancoraeducation.ucertify.com/app/?func=navigate_items&item_sequence=6]

## Objective of the Lab
In this lab, you will learn to manage user accounts. User account management is one of the many challenges of Linux system administrators. Some of the responsibilities of a system administrator are enabling/disabling user accounts, preserving the home directory, setting user permissions, assigning groups/shells to users, and managing passwords.

## Instructions
### STEP 1
From the left sidebar, open the Terminal icon. 
### STEP 2 
Execute the following command to display user account information (including the login shell and home directory) for the bin account:
```bash
grep bin /etc/passwd
```
### STEP 3 
Execute the following command to display user password information (including the encrypted password and password aging) for the bin account:
```bash
grep bin /etc/shadow
```
### STEP 4
Execute the following command to switch to the root account so the command from STEP 2 will be successful when executed:
```bash
su -
```
### STEP 5
Execute the following command to create a new user named jake and explicitly use options to create the home directory /home/jake for this user:
```bash
useradd -d /home/jake -m jake
```
### STEP 6
Execute the following commands to set a password for the jake user of your choice (Note: Execute one command at a time.): 
### Caution
Enter New password and Retype new password as ucertify whenever asked.
```bash
passwd jake
```
```bash
useradd -D
```
### STEP 7
Execute the following command to display the file that contains the password aging defaults:
```bash
less /etc/login.defs
```
### STEP 8
Enter q to exit.
### STEP 9
Execute the following command to delete the jake user and his home directory, using a single command:
```bash
userdel -r jake
```
# Disclaimer

This repository is for **educational and personal learning purposes only**.  

The original lab content belongs to **uCertify / Ancora Education** and remains their copyrighted material.  
This repository is not affiliated with, endorsed by, or sponsored by uCertify or Ancora Education.  

No copyright infringement is intended.  
Use of any tools or techniques mentioned here should only be performed in authorized, legal environments.
