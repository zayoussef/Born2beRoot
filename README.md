#ENGLISH VERSION-Finished Ig 😀


# Born2beroot-Tutorial 💻

### Before starting...

```
This is a complete guide step by step for the Born2Broot project at 42 school.
You should not take everything here for granted, and do your own research.
Thank you in advance for using this guide.
```

#Index

1. [Download virtual machine ISO 💿](#1--download-the-virtual-machine-iso-)
2. [Virtual machine installation 🛠](#2--installing-the-virtual-machine-)
3. [Debian installation 🌀](#3--installing-debian-)
4. [Virtual machine setup ⚙️](#4--virtual-machine-setup-%EF%B8%8F)

4.1 [Installing sudo & configuration of users and groups 👤](#41---installing-sudo--configuration-of-user-and-groups-)

4.2 [Installing & configuring SSH 📶](#42---installing--configuring-ssh-)

4.3 [Installing & configuring UFW 🔥🧱](#43-installing--configuring-ufw-)

4.4 [Setting up the sudo policies 🔒](#44-setting-up-the-sudo-policies-)

4.5 [Setting up the strong password policy 🔑](#45-setting-up-a-strong-password-policy-)

4.6 [Connecting via SSH 🗣](#46-connecting-via-ssh-)

5. [Script 🚨](#5--script-)

5.1 [End result of the script 🆗](#513-end-result-of-the-script)

6. [Crontab ⏰](#6--crontab-)
7. [Signature.txt 📝](#7--signaturetxt-)
8. [Bonus ⭐](#8--bonus-%EF%B8%8F)

8.1 [Manual partition](#81--manual-partition)

8.2 [Wordpress & services configuration 🌐](#82---wordpress--services-configuration-)

9. [Correction sheet ✅](#9--correction-sheet-)

9.1 [Evaluation answers 💯](#91-evaluation-answers-)

## 1-_Download the virtual machine ISO_ 💿

[CLICK HERE](https://www.debian.org/download.en.html) for the URL of the debian ISO. This is a direct link to debian.org/download.

## 2-_Installing the virtual machine_ 🛠

A virtualization software is required to perform the installation. In this tutorial we will use [Virtual Box](https://www.virtualbox.org/). If you already have installed this software and you have the Debian ISO we can proceed.

1 ◦ We need to open VirtualBox and click ```New```

<img width="836" alt="Screen Shot 2022-07-13 at 18 02 05" src="https://user-images.githubusercontent.com/66915274/178779265-38eade6e-2789-4597-89e9-5beca2d3921a.png">

2 ◦ We must choose a name for the machine and the folder which will locate it. **IMPORTANT** Store the machine created inside the sgoinfre folder located in your campus server; this is important because we will run out of memory space in our session and the installation will fail. (Ask your staff if you can't find it)

<img width="928" alt="Screen Shot 2022-10-23 at 2 57 11 PM" src="https://user-images.githubusercontent.com/66915274/197393458-dda8da5f-2362-4d36-b740-0951ebf03d3c.png">

3 ◦ Select the total RAM memory which we will reserve for the machine.

<img width="685" alt="Screen Shot 2022-07-13 at 13 06 05" src="https://user-images.githubusercontent.com/66915274/178781098-8aa07fbc-e1d2-4bee-8021-ddf052880364.png">

4 ◦ Select the second option so we can create a virtual disk now.

<img width="826" alt="Screen Shot 2022-07-13 at 18 13 24" src="https://user-images.githubusercontent.com/66915274/178781390-289236e0-1732-4dd8-8d3d-34eb0a229a18.png">

5 ◦ Choose the first option ```VDI``` since we downloaded an ISO.

<img width="829" alt="Screen Shot 2022-07-13 at 18 16 35" src="https://user-images.githubusercontent.com/66915274/178781999-a42c3c6c-bc1e-4ad5-8bc5-b4b3f811c3f2.png">

6 ◦ Select the first option ```Dynamically allocated``` so it will allocate the memory of the physical machine as it feels necessary while using the virtual machine until we reach the available limit.

<img width="833" alt="Screen Shot 2022-07-13 at 18 19 33" src="https://user-images.githubusercontent.com/66915274/178782529-fb309739-3169-4e20-b3e1-23d17a122a18.png">

7 ◦ One we established the recommended ```12 GB``` we must click on ```Create```. If we are doing the bonus we might set ```30 GB```.

<img width="835" alt="Screen Shot 2022-07-13 at 18 25 20" src="https://user-images.githubusercontent.com/66915274/178783666-4fa624a3-9c38-4c45-b6a8-d476c2864200.png">

8 ◦ It might seem that we have already finished the installation , but there's still some steps to do. Click on ```Settings```.

<img width="831" alt="Screen Shot 2022-07-13 at 18 30 46" src="https://user-images.githubusercontent.com/66915274/178784822-38228e96-ca37-4cc0-b3ca-551829e4c8c8.png">

9 ◦ Now click on ```Storage``` , again click on the 💿 that we find on the right and click on ```Choose a disk file```.

<img width="962" alt="Screen Shot 2022-07-13 at 18 33 28" src="https://user-images.githubusercontent.com/66915274/178785148-2904cf4f-93c0-4866-a5d6-778390bddeb7.png">

10 ◦ Select the ISO that we just downloaded and click ```Open```, then click on ```Ok```.

<img width="790" alt="Screen Shot 2022-07-13 at 18 38 39" src="https://user-images.githubusercontent.com/66915274/178786115-24f93fde-bc01-4e60-bf8d-20d7a5ae83be.png">

11. ◦ Once all these steps have been completed we can ```Start``` our new virtual machine.

<img width="833" alt="Screen Shot 2022-07-13 at 18 44 55" src="https://user-images.githubusercontent.com/66915274/178787317-aab80b53-8244-4ede-9c75-11fcf4efdd1c.png">

## 3-Installing Debian 🌀

➤ **You there, wait**❗️ Your eyesight is important 👀❗️ Making the window bigger will help:

<img width="666" alt="Screen Shot 2022-07-13 at 18 51 41" src="https://user-images.githubusercontent.com/66915274/178788620-61064b58-0c0c-4f48-815e-60b4a8eaecae.png">

Use the ```command``` key so the machine captures your mouse and vice versa.

### Now we proceed 🛠

1 ◦ We will choose the version without graphic interface ```Install``` size the subject says so. Any time we want to confirm something ```Enter key``` must be pressed, and the ```Arrow keys``` must be used any time to move around.

<img width="632" alt="Screen Shot 2022-07-13 at 18 58 48" src="https://user-images.githubusercontent.com/66915274/178789643-e987c6d0-5b6f-4b98-ad4a-5c092a352183.png">

2 ◦ Now language must be chosen for the machine that will be present during the installation and the default setting. Select ```English```.

<img width="794" alt="Screen Shot 2022-07-13 at 190041" src="https://user-images.githubusercontent.com/66915274/178789949-4fe83ac8-23b8-4f82-a034-a6d5e81d4f17.png">

3 ◦ It's time to select the country. If yours not on the present list go to ```Other```.

<img width="791" alt="Screen Shot 2022-07-13 at 19 07 50" src="https://user-images.githubusercontent.com/66915274/178791067-44230a4c-e647-46cb-9d6f-bc441bf0227b.png">

4 ◦ Time to select continent. In our case we will select ```Europe``` 🇪🇺.

<img width="797" alt="Screen Shot 2022-07-13 at 19 09 58" src="https://user-images.githubusercontent.com/66915274/178791387-78171f90-2834-42ab-aedb-9cf900d0ecd5.png">

5 ◦ Now select the country. In our case we will select ```Spain``` 🇪🇸.

<img width="793" alt="Screen Shot 2022-07-13 at 19 12 01" src="https://user-images.githubusercontent.com/66915274/178791824-7a34813c-eae9-4b5c-9873-cea158229e07.png">

6 ◦ Choose ```United States```.

<img width="792" alt="Screen Shot 2022-07-13 at 19 13 43" src="https://user-images.githubusercontent.com/66915274/178792054-4e72dfdd-8175-48f9-a06d-f2696fa752e3.png">

7 ◦ This time it's turn for selecting a keymap. Our keyboard follows the ANSI standard so ```American English```. If you don't know what keyboard standard is yours we highly recommend you to ask your staff.

<img width="793" alt="Screen Shot 2022-07-13 at 19 02 21" src="https://user-images.githubusercontent.com/66915274/178790230-d2571d4f-a546-4b43-bd44-c6a591d92d72.png">

8 ◦ Now we must set a ```Host Name``` of the machine, which must be your login followed by a 42.

<img width="792" alt="Screen Shot 2022-07-13 at 19 17 23" src="https://user-images.githubusercontent.com/66915274/178792607-1cc585eb-ae32-4b2c-97fd-4fcf5bad4262.png">

9 ◦ This section will be left blank since the subject doesn't require it.

<img width="792" alt="Screen Shot 2022-07-13 at 19 20 29" src="https://user-images.githubusercontent.com/66915274/178793113-b0934aac-fac4-4844-8412-aca124038fd0.png">

10 ◦ We have to set a password for the root user. **IMPORTANT** Save this password since we need to use the root user. If you want to check the password is correct, try going to *Show Pawssword in Clear* and then press the ```Space bar```.

<img width="794" alt="Screen Shot 2022-07-13 at 19 21 29" src="https://user-images.githubusercontent.com/66915274/178793296-c2c3b6c5-9744-4ba8-ac32-8e3c21c44f9b.png">

11 ◦ Repeat the process as you need to confirm the password we just set.

<img width="796" alt="Screen Shot 2022-07-13 at 19 24 53" src="https://user-images.githubusercontent.com/66915274/178793903-2ea7c623-7175-4c27-98bf-85c8c1b359db.png">

12 ◦ Set up the user name. As is in the subject, we need a new user that isn't the root user, and the name for that user have to be your student login.

<img width="794" alt="Screen Shot 2022-07-13 at 19 26 20" src="https://user-images.githubusercontent.com/66915274/178794178-901f7951-a978-458d-a925-4586026784f7.png">

Repeat you user name.

![image](https://user-images.githubusercontent.com/66915274/182679675-4d3805a9-34c9-4ba3-9488-1a7fe30f2519.png)


13 ◦ And now we have to set our new user password. Just as before, repeat the process; save this password too because it will be used later.

<img width="790" alt="Screen Shot 2022-07-13 at 19 30 08" src="https://user-images.githubusercontent.com/66915274/178794862-94de8c7a-282e-4a83-9903-d3b8439122ea.png">

14 ◦ Select your time zone.

<img width="796" alt="Screen Shot 2022-07-13 at 19 31 41" src="https://user-images.githubusercontent.com/66915274/178795105-956854e1-deff-4851-8eba-26cdefb1e06f.png">

15 ◦ Select ```Guied-use entire disk and set up encrypted LVM```. ⚠️❗️ **If you want to do the bonus select ```Manual``` and then [click here](#8--bonus-%EF%B8%8F)** ❗️⚠️

<img width="796" alt="Screen Shot 2022-07-13 at 19 33 13" src="https://user-images.githubusercontent.com/66915274/178795367-b82018de-edc8-47d3-8cd6-b90c5e3be2fa.png">


16 ◦ We select the disk in which we want to do the partitioning (There should only be one disk).

<img width="789" alt="Screen Shot 2022-07-13 at 19 40 03" src="https://user-images.githubusercontent.com/66915274/178796481-29ef7ebc-0518-40f0-9429-3f43316b35d3.png">

17 ◦ Once we have chosen the disk, we will have to do the partitioning as requested. To do it properly we must select the third option ```Separate /home, /var, and /tmp partitions```.

<img width="777" alt="Screen Shot 2022-07-13 at 19 41 16" src="https://user-images.githubusercontent.com/66915274/178796683-13f3ce53-9032-40c4-9957-c715856ff448.png">

18 ◦ We choose the ```Yes``` option so that the changes are written to the disk and we can configure the logical volume manager (LVM).

<img width="777" alt="Screen Shot 2022-07-13 at 19 44 30" src="https://user-images.githubusercontent.com/66915274/178797258-8c34bc31-16a7-4aef-8406-cecc21fdf028.png">

19 ◦ We give Cancel since the deletion of data on the disk is not necessary.

<img width="782" alt="Screen Shot 2022-07-13 at 19 46 45" src="https://user-images.githubusercontent.com/66915274/178797666-78cdf892-1a83-4c68-8f85-0d5440cd4854.png">

20 ◦ Again we will have to put a password, this time it will be the encryption phrase. As I have previously mentioned, you must repeat the process and you must write it down since it will be important in the future.

<img width="777" alt="Screen Shot 2022-07-13 at 19 51 17" src="https://user-images.githubusercontent.com/66915274/178798491-4c9b4a0c-d698-47c7-9579-10b16aa47275.png">

21 ◦ In this step we must enter the amount of volume that we will use for the guided partition. We must enter ```max``` or the maximum size number available in my case is ```12.4 GB```.

<img width="794" alt="Screen Shot 2022-07-13 at 19 55 02" src="https://user-images.githubusercontent.com/66915274/178799165-c6b05fd2-86ad-45b7-a026-9ee169eda5d5.png">

22 ◦ To finalize the partition and write the changes on the disk we will give the option ```Finish partitioning and write changes to disk```.

<img width="795" alt="Screen Shot 2022-07-13 at 19 59 15" src="https://user-images.githubusercontent.com/66915274/178800001-a0762a14-3d55-47e6-98c2-1198c7ee7d87.png">

23 ◦ We select the ```Yes``` option to continue and confirm that we do not want to make any more changes to the disk.

<img width="795" alt="Screen Shot 2022-07-13 at 20 00 58" src="https://user-images.githubusercontent.com/66915274/178800331-4e9daf83-fe4e-47c0-9737-d1a89a10b3a8.png">

24 ◦ We select the ```No``` option since we don't need additional packages.

<img width="770" alt="Screen Shot 2022-07-13 at 20 05 42" src="https://user-images.githubusercontent.com/66915274/178801099-2dda24f5-0d46-4184-8c44-a8fe0bf46527.png">

25th We choose our country.

<img width="756" alt="Screen Shot 2022-07-13 at 20 14 23" src="https://user-images.githubusercontent.com/66915274/178802653-d9e8504a-b60b-4441-8ee3-8d48ca4a6bf0.png">

26 ◦ We choose ```deb.debian.org``` since taking into account our region is where we will have a better connection.

<img width="792" alt="Screen Shot 2022-07-13 at 20 15 00" src="https://user-images.githubusercontent.com/66915274/178802772-4f67cd99-60d5-4439-8502-317e81e07d70.png">

27 ◦ We will leave this option empty and we will give it directly to ```Continue```.

<img width="797" alt="Screen Shot 2022-07-13 at 20 17 24" src="https://user-images.githubusercontent.com/66915274/178803208-2969acae-3fa7-423e-8a3c-bb7c76eff824.png">

28 ◦ We select the ```No``` option since we don't want developers to see our statistics even if they are anonymous.

<img width="796" alt="Screen Shot 2022-07-13 at 20 21 54" src="https://user-images.githubusercontent.com/66915274/178803926-a4efbc70-f3e2-4e6c-9809-9152478d8237.png">

29 ◦ We will remove all the software options (with the space bar) and we will give ```Continue```.

<img width="797" alt="Screen Shot 2022-07-13 at 20 24 17" src="https://user-images.githubusercontent.com/66915274/178804377-e775b89e-93d4-482f-a4d0-0ef126f47719.png">

30 ◦ We will select ```Yes``` to install [GRUB boot](https://en.wikipedia.org/wiki/GNU_GRUB) on the hard drive.

<img width="792" alt="Screen Shot 2022-07-13 at 20 26 24" src="https://user-images.githubusercontent.com/66915274/178804771-ba16e0b7-9f06-4c5b-9451-0bfd65efd2bb.png">

31 ◦ We will choose the device for the bootloader installation ```/dev/sda (ata_VBOX_HARDDISK)```.

<img width="792" alt="Screen Shot 2022-07-13 at 20 35 46" src="https://user-images.githubusercontent.com/66915274/178806441-f1bf3159-4e09-4c9a-9102-b3261c9000d8.png">

32 ◦ We will give ```Continue``` to finish the installation.

<img width="794" alt="Screen Shot 2022-07-13 at 20 39 30" src="https://user-images.githubusercontent.com/66915274/178807102-e2a9722e-791f-48a0-ae35-b05b36a37ed2.png">

## 4-Virtual machine setup ⚙️

➤ The first thing we need to do is select ```Debian GNU/Linux```.

➤ We must enter the encryption password that we used previously. In my case it is ```Hello42bcn```.

<img width="714" alt="Screen Shot 2022-07-13 at 20 47 26" src="https://user-images.githubusercontent.com/66915274/178808699-f1024129-5f90-41d0-a9a8-4806f5bc114b.png">

➤ We must enter the username and password that we have created. In my case the user is ```gemartin``` and the password is ```Hola42spain```.

<img width="798" alt="Screen Shot 2022-07-13 at 20 48 38" src="https://user-images.githubusercontent.com/66915274/178808994-664025ac-36df-4332-8e44-505ecd2ca305.png">

### We already have everything ready to start configuring our Debian virtual machine❗️

### 4.1-Installing sudo & configuration of user and groups 👤

1 ◦ For the installation of sudo we must first be in the root user, for this we will put ```Su``` in the terminal and enter the password, in my case it is ```Hello42bcn```. Once we have accessed the root user, we must enter the command ```apt install sudo``` to install the necessary packages.

<img width="796" alt="Screen Shot 2022-07-14 at 1 36 46" src="https://user-images.githubusercontent.com/66915274/178855273-fc76689c-224b-4368-b7b1-5d1954427aff.png">

2 ◦ We must restart the machine for the changes to take effect. To do this we will use the ```sudo reboot``` command and wait for it to restart.

<img width="514" alt="Screen Shot 2022-07-14 at 2 02 24" src="https://user-images.githubusercontent.com/66915274/178857108-a51988e1-084c-498c-86c6-98ab5a3b1305.png">

3 ◦ Once restarted we must re-enter the encryption and user passwords. To verify that we have installed ```sudo``` correctly we will enter the root user again and we will put the command ```sudo-V```, this command in addition to showing us the version of sudo will also show the arguments passed to configure when sudo was created and the plugins that can display more detailed information. (Optional) ➤ Since the output of the command is very long if we want to see it completely we must redirect the output to a file ```sudo-V > file.txt``` and then edit the ```nano file . txt```. Or put ```| more``` after the command.

<img width="799" alt="Screen Shot 2022-07-14 at 2 09 59" src="https://user-images.githubusercontent.com/66915274/178857742-96356272-abd6-44c4-a3e6-5e8b9f471146.png">

4 ◦ Continuing in the root user we will create a user with our login with the command ```sudo adduser login``` as we have already created the user in the installation it should appear that the user already exists.

<img width="509" alt="Screen Shot 2022-07-14 at 2 15 11" src="https://user-images.githubusercontent.com/66915274/178858240-95ce2a2b-004a-4bcb-981a-7990c1cc4fdd.png">

5 ◦ Now we need to create a new group called ```user42```. To create it we must do ```sudo addgroup user42```.

<img width="367" alt="Screen Shot 2022-10-26 at 6 30 52 PM" src="https://user-images.githubusercontent.com/66915274/198082677-d393243e-363a-4d1f-95d8-a6695336a47a.png">

🧠 <b>What is GID?❓</b> It is the group identifier, it is an abbreviation of Group 🆔.

🤔 <b>Has the group been successfully created? </b> The truth is that since there has been no error message, we can still check if it has been created with the command ```getent group group_name``` or we can also do ```cat /etc/ group ``` and we will be able to see all the groups and the users that are inside them.

6 ◦ With the command ```sudo adduser user group``` we will include the user in the group. We must include the user in the ```sudo``` and ```user42``` groups.

<img width="422" alt="Screen Shot 2022-10-26 at 6 32 30 PM" src="https://user-images.githubusercontent.com/66915274/198083019-c5a442bb-c625-45ce-84e1-bcbca3a7dba5.png">

<img width="404" alt="Screen Shot 2022-10-26 at 6 34 09 PM" src="https://user-images.githubusercontent.com/66915274/198083377-bd4162c6-317b-474f-8bc4-e542be4dcfde.png">

7 ◦ Once we have entered them to check that everything has been done correctly we can execute the command ```getent group name_group``` or we can also edit the /etc/group file ```nano /etc/group`` ` and in the groups ```sudo``` and ```login42``` our user should appear.

<img width="328" alt="Screen Shot 2022-10-26 at 6 35 50 PM" src="https://user-images.githubusercontent.com/66915274/198083739-ad16e388-69c3-41d1-a061-e55dd66b0d14.png">

<img width="151" alt="Screen Shot 2022-10-26 at 6 36 18 PM" src="https://user-images.githubusercontent.com/66915274/198083854-0fba5296-a49f-44cc-8427-59a692e69288.png">

<img width="353" alt="Screen Shot 2022-10-26 at 6 39 22 PM" src="https://user-images.githubusercontent.com/66915274/198084464-f73352ee-ed21-478b-a44d-d86eb6d8a1cd.png">

<img width="183" alt="Screen Shot 2022-10-26 at 6 38 25 PM" src="https://user-images.githubusercontent.com/66915274/198084311-45a50162-ff89-4e7d-a3c5-45e7048520a4.png">

### 4.2-Installing & configuring SSH 📶

🧠 <b> What is SSH?❓</b> It is the name of a protocol and the program that implements it, whose main function is remote access to a server through a secure channel in which all information is encrypted.

1 ◦ The first thing we will do is do ```sudo apt update``` to update the repositories that we defined in the /etc/apt/sources.list file

<img width="774" alt="Screen Shot 2022-07-14 at 3 09 44" src="https://user-images.githubusercontent.com/66915274/178864173-aa5a08cf-8562-4484-a60a-3e1c7a533a28.png">

2 ◦ Then we will install the main connectivity tool for remote login with the SSH protocol, this tool is OpenSSH. To install it we must enter the command ```sudo apt install openssh-server```. In the confirmation message we put ```Y```, then we will wait for the installation to finish.

<img width="772" alt="Screen Shot 2022-07-14 at 3 14 52" src="https://user-images.githubusercontent.com/66915274/178865991-cdb90f12-ebd8-4583-bcbb-70f47c86abe6.png">

To verify that it has been installed correctly, we will do ```sudo service ssh status``` and it should appear active.

<img width="702" alt="Screen Shot 2022-07-14 at 3 53 59" src="https://user-images.githubusercontent.com/66915274/178876938-7fd74214-15df-4759-bf8d-52b53a8f4251.png">

3 ◦ Once the installation is finished, some files have been created that we must configure. For this we will use [Nano](https://es.wikipedia.org/wiki/GNU_Nano) or if you prefer another text editor. The first file we will edit will be ```/etc/ssh/sshd_config```. If you are not from the root user you will not have write permissions, for this we will do ```su``` and put the password to enter the root user or if you do not want to enter the root user we put sudo at the beginning of the command ``` sudo nano /etc/ssh/sshd_config```.

<img width="497" alt="Screen Shot 2022-07-14 at 3 24 21" src="https://user-images.githubusercontent.com/66915274/178867150-273c75c1-c935-45f0-a551-1a115d3f6f6a.png">

4 ◦ The ```#``` at the beginning of a line means that it is commented, the lines that we are going to modify must be uncommented. Once we are editing the file we must modify the following lines:

➤ #Port 22-> Port 4242

<img width="807" alt="Screen Shot 2022-07-14 at 3 31 04" src="https://user-images.githubusercontent.com/66915274/178867929-0f8be11e-d0ca-4445-af05-a693d01411bd.png">

➤ #PermitRootLogin prohibit-password-> PermitRootLogin no

<img width="798" alt="Screen Shot 2022-07-14 at 3 34 13" src="https://user-images.githubusercontent.com/66915274/178868266-fc6d6684-8196-4021-b884-a047a443a3ec.png">

Once we have modified those lines we must save the changes made to the file and stop editing it.

5 ◦ Now we need to edit the ```/etc/ssh/ssh_config``` file.

<img width="501" alt="Screen Shot 2022-07-14 at 3 48 56" src="https://user-images.githubusercontent.com/66915274/178872582-8277e687-8ab7-4087-bd17-a71e5e86d5e6.png">

We will edit the following line:

➤ #Port22-> Port4242

<img width="795" alt="Screen Shot 2022-07-14 at 3 50 29" src="https://user-images.githubusercontent.com/66915274/178875013-1969c13f-9e43-4f2a-a037-f384a8e87a78.png">

6 ◦ Finally we must restart the ssh service so that the modifications we have just made are updated. To do this we must write the command ```sudo service ssh restart``` and once reset we will look at the current status with ```sudo service ssh status``` and to confirm that the changes have been made in the server listener you must Port 4242 will appear.

<img width="713" alt="Screen Shot 2022-07-14 at 3 56 56" src="https://user-images.githubusercontent.com/66915274/178880333-0e2ad7fd-674b-4b4f-b92a-25acbc36c8a5.png">


### 4.3 Installing & configuring UFW 🔥🧱

🧠 <b>What is [UFW](https://es.wikipedia.org/wiki/Uncomplicated_Firewall)❓</b> It is a [firewall](https://es.wikipedia.org/wiki/Cortafuegos_(inform %C3%A1tica)) which uses the command line to configure [iptables](https://en.wikipedia.org/wiki/Iptables) using a small number of simple commands.

1 ◦ The first thing we must do is install UFW, for this we will use the command ```sudo apt install ufw``` then we will write a ```y``` to confirm that we want to install it and wait for it to finish.

<img width="771" alt="Screen Shot 2022-07-14 at 19 28 55" src="https://user-images.githubusercontent.com/66915274/179045920-4a9aec64-b1d7-4785-89a1-4a299aae21a3.png">

<img width="802" alt="Screen Shot 2022-07-14 at 19 29 25" src="https://user-images.githubusercontent.com/66915274/179045994-19cdf6e0-be61-454b-9adc-ba1f9c2dfd84.png">

2 ◦ Once installed we must enable it, for this we must put the following command ```sudo ufw enable``` and immediately afterwards it should indicate that the firewall is active.

<img width="498" alt="Screen Shot 2022-07-14 at 19 32 57" src="https://user-images.githubusercontent.com/66915274/179046565-307c042b-243e-4224-bcb2-d02859332352.png">

3 ◦ Now what we must do is that our firewall allows the connections that are carried out through port 4242. We will do it with the following command ```sudo ufw allow 4242```.

<img width="514" alt="Screen Shot 2022-07-14 at 19 34 12" src="https://user-images.githubusercontent.com/66915274/179046765-5277ec55-b8e4-4d4f-a617-a2a8758b80a8.png">

4 ◦ Finally we will check that everything is correctly configured by looking at the status of our firewall, where connections through port 4242 should already appear as allowed. To see the status we will use the ```sudo ufw status``` command.

<img width="575" alt="Screen Shot 2022-07-14 at 19 38 37" src="https://user-images.githubusercontent.com/66915274/179047574-8073045c-6e78-4b6f-8487-cb0f490a2cd0.png">

### 4.4 Setting up the sudo policies 🔒

1 ◦ We will create a file in the path /etc/sudoers.d/ to my file. I have decided to call it sudo_config since the password configuration will be stored in that file. The exact command to create the file is ```touch /etc/sudoers.d/sudo_config```.

<img width="511" alt="Screen Shot 2022-07-14 at 220040" src="https://user-images.githubusercontent.com/66915274/179072822-2f86bd8b-216e-45e4-a15b-8fe3a49149ff.png">

2 ◦ We must create the sudo directory in the /var/log path because each command that we execute with sudo , both the input and the output must be stored in that directory. To create it we will use the command ```mkdir /var/log/sudo```.

<img width="502" alt="Screen Shot 2022-07-14 at 21 56 53" src="https://user-images.githubusercontent.com/66915274/179072210-ad99e50d-fa57-494b-999d-3a80dd0f7849.png">

3 ◦ We must edit the file created in step 1. As I mentioned before, you can use the editor that you like the most, but I will use nano. Command to edit the file: ```nano /etc/sudoers.d/sudo_config```.

<img width="502" alt="Screen Shot 2022-07-14 at 22 04 10" src="https://user-images.githubusercontent.com/66915274/179073389-5b2a9c16-811c-4133-87c6-479e770c880b.png">

4 ◦ Once we are editing the file, we must enter the following commands to meet all the requirements requested by the subject.

```
Defaults passwd_tries=3
Defaults badpass_message="Custom error message"
Defaults logfile="/var/log/sudo/sudo_config"
Defaults log_input, log_output
Defaults iolog_dir="/var/log/sudo"
Defaults requiretty
Defaults secure_path="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/snap/bin"
```

➤ How the file should look.

<img width="1202" alt="Screen Shot 2022-07-16 at 2 03 45" src="https://user-images.githubusercontent.com/66915274/179326003-1fd67295-4be2-47bd-98fc-d5821f5f1c4d.png">

🤔 <b>What does each command do❓ </b>

<img width="802" alt="Screen Shot 2022-07-16 at 2 04 56" src="https://user-images.githubusercontent.com/66915274/179326915-b374f679-fa2e-4e02-8b38-cdb53c6354a6.png">

### 4.5 Setting up a strong password policy 🔑

1 ◦ The first step will be to edit the login.defs file.

<img width="493" alt="Screen Shot 2022-07-16 at 2 54 06" src="https://user-images.githubusercontent.com/66915274/179327943-67432d4a-7042-44ea-96f4-5975556ce4dc.png">

2 ◦ Once we are editing the file we will modify the following parameters:

➤ PASS_MAX_DAYS 99999-> PASS_MAX_DAYS 30

➤ PASS_MIN_DAYS 0-> PASS_MIN_DAYS 2


<img width="802" alt="Screen Shot 2022-07-16 at 3 05 49" src="https://user-images.githubusercontent.com/66915274/179328449-32a40f67-a18d-4f29-993b-94d013cd7670.png">

PASS_MAX_DAYS: It is the expiration time of the password. The number corresponds to days.

PASS_MIN_DAYS: The minimum number of days allowed before changing a password.

PASS_WARN_AGE: The user will receive a warning message indicating that the specified days are missing for their password to expire.

3 ◦ In order to continue with the configuration we must install the following packages with this command ```sudo apt install libpam-pwquality``` , then we will type ```Y``` to confirm the installation and wait for it to finish.

<img width="770" alt="Screen Shot 2022-07-16 at 3 13 52" src="https://user-images.githubusercontent.com/66915274/179328708-c5054703-bdb0-4cca-82a8-6ab25ce42b40.png">

4 ◦ The next thing we have to do is edit a file again and modify some lines. We'll do ```nano /etc/pam.d/common-password```.

<img width="500" alt="Screen Shot 2022-07-16 at 3 27 02" src="https://user-images.githubusercontent.com/66915274/179329260-0e18bd27-a522-4c7c-86bf-21823eee0f8b.png">

5 ◦ After retry=3 we must add the following commands:

```
minlen=10
ucredit=-1
dcredit=-1
maxrepeat=3
reject_username
difok=7
enforce_for_root
```
➤ This is how the line should be ↙️

<img width="1127" alt="Screen Shot 2022-07-16 at 3 34 33" src="https://user-images.githubusercontent.com/66915274/179329511-0619183a-8ccc-456b-8f27-3962fc542cc3.png">

➤ This is how it should look in the file ↙️

<img width="800" alt="Screen Shot 2022-07-16 at 3 38 08" src="https://user-images.githubusercontent.com/66915274/179329787-1b718843-9272-43e4-8d92-8d83933cc938.png">

🤔 <b>What does each command do❓</b>

minlen=10 ➤ The minimum number of characters the password must contain.

ucredit=-1 ➤ Must contain at least one ```Caps``` character. We put the-since it must contain at least one character, if we put + we refer to a maximum of those characters.

dcredit=-1 ➤ It must contain at least one digit.

maxrepeat=3 ➤ You cannot have the same character more than 3 times in a row.

reject_username ➤ Cannot contain the username.

difok=7 ➤ Must have at least 7 characters that are not part of the old password.

enforce_for_root ➤ We will enforce this policy for the root user.

### 4.6 Connecting via SSH 🗣

1 ◦ To connect via SSH we must close the machine, open VirtualBox and give configuration.

<img width="832" alt="Screen Shot 2022-07-18 at 10 15 13" src="https://user-images.githubusercontent.com/66915274/179470948-d9a863ef-f1a3-41fb-a103-25378064e747.png">

2 ◦ Once in configuration we must click on the ```Network``` section, we will click on ```Advanced``` so that it shows us more options and we will click on ```Port Forwarding```.

<img width="684" alt="Screen Shot 2022-07-18 at 10 18 32" src="https://user-images.githubusercontent.com/66915274/179471690-cfbdbf4b-ab93-4b12-9504-2482712652a3.png">

3 ◦ We will click on the next emoticon to add a forwarding rule.

<img width="585" alt="Screen Shot 2022-07-18 at 10 21 24" src="https://user-images.githubusercontent.com/66915274/179471855-913a684d-c7b0-43e2-9e01-d2c954fe75a4.png">

4 ◦ Finally we will add the port ```4242``` to the host and the guest. The IP's are not necessary. We will click on the accept button so that the changes are applied.

<img width="588" alt="Screen Shot 2022-07-18 at 10 22 29" src="https://user-images.githubusercontent.com/66915274/179472105-5942b3ec-5c29-4d49-a00e-67f9cde289e8.png">

➤ In order to connect to the virtual machine from the real one, we must open a terminal on the real machine and write ```ssh gemartin@localhost-p 4242```, it will ask us for the user password and once we enter it, we will get the login in green and that means we will be connected.

<img width="517" alt="Screen Shot 2022-10-27 at 12 40 23 AM" src="https://user-images.githubusercontent.com/66915274/198174777-28f7793b-273b-43ce-b1c2-4a890353cb8c.png">

<img width="566" alt="Screen Shot 2022-10-27 at 12 40 04 AM" src="https://user-images.githubusercontent.com/66915274/198174814-c1873c62-41dd-4c1d-ad2d-f268b2da0e4c.png">

## 5-Script 🚨

This is a very important part of the project. You must pay attention to everything, it is very important not to copy and paste the file directly without knowing what each thing does. In the evaluation you must explain each command if the evaluator asks for it.

🧠 <b>What is a script❓</b> It is a sequence of commands saved in a file that when executed will do the function of each command.

### 5.1 Architecture

In order to see the architecture of the OS and its kernel version we will use the command ```uname-a``` ( "-a" == "--all" ) which will basically print all the information except if the type of processor is unknown or the hardware platform.

<img width="715" alt="Screen Shot 2022-10-27 at 4 50 06 PM" src="https://user-images.githubusercontent.com/66915274/198322524-8c2d305f-bfe8-4e4a-bf31-6a883af71ad3.png">

### 5.2 Core Physics

In order to display the number of physical cores we will use the /proc/cpuinfo file which provides information about the processor: its type, brand, model, performance, etc. We will use the command ```grep "physical id" /proc/cpuinfo | wc-l``` with the grep command we will search inside the "physical id" file and with wc-l we will count the lines of the grep result. We do this because the way to quantify nuclei is not very common. If there is one processor it will mark 0 and if it has more than one processor it will display all processor information separately by counting the processors using zero notation. In this way we will simply count the lines that there are since it is more comfortable to quantify it that way.

<img width="596" alt="Screen Shot 2022-10-27 at 4 50 49 PM" src="https://user-images.githubusercontent.com/66915274/198322799-4bf2131e-7fba-4c9e-8d1b-bb9cc1b89e76.png">


### 5.3 Virtual cores

To be able to show the number of virtual cores is very similar to the previous one. We will use the /proc/cpuinfo file again, but in this case we will use the command ```grep processor /proc/cpuinfo | wc-l```. The use is practically the same as the previous one, only that instead of counting the lines of "physical id" we will do it of processor. We do it this way for the same reason as before, the way to quantize marks 0 if there is a processor.

<img width="586" alt="Screen Shot 2022-10-27 at 4 55 48 PM" src="https://user-images.githubusercontent.com/66915274/198324254-3d0f247d-b767-4e02-9e69-11b4e0586280.png">


### 5.4 RAM memory

To show the ram memory we will use the ```free``` command to instantly see information about the ram, the part used, free, reserved for other resources, etc. For more information about the command we will put free--help. We will use free--mega since that unit of measure appears in the subject.

<img width="672" alt="Screen Shot 2022-08-02 at 2 46 10" src="https://user-images.githubusercontent.com/66915274/182268241-86b743bb-653d-4fef-acda-e7bfa59e38d7.png">

Once we have executed this command we must filter our search since we do not need all the information it provides us, the first thing we must show is the memory used, for this we will use the ```awk``` command that what this command does It is to process data based on text files, that is, we can use the data that interests us from X file. Finally what we will do is compare if the first word of a row is equal to "Mem:" we will print the third word of that row that will be the memory used. The whole command together would be ```free--mega | awk '$1 == "Mem:" {print $3}'```. In the script, we will assign the return value of this command to a variable that we will concatenate with other variables so that everything remains the same as specified by the subject.

<img width="621" alt="Screen Shot 2022-08-02 at 2 55 21" src="https://user-images.githubusercontent.com/66915274/182269019-d5bb3107-f091-491f-a4ab-27edd357aec8.png">

To obtain the total memory, the command is practically the same as the previous one, the only thing we have to change is that instead of printing the third word of the row we want the second ```free--mega | awk '$1 == "Mem:" {print $2}'```.

<img width="605" alt="Screen Shot 2022-08-02 at 30002" src="https://user-images.githubusercontent.com/66915274/182269450-318816e1-fc71-48b0-a860-278cc6050e05.png">

Finally we must calculate the % of memory used. The new command is similar to the previous ones, the only modification that we will make in the printing part. As the operation to get the percentage is not exact, it can give us many decimals and only 2 appear in the subject, so we will do the same, that's why we use ```%.2f``` so that only 2 decimals are shown. Another thing you may not know is that in printf to display a ```%``` you have to put ```%%```. The entire ```free--mega | awk '$1 == "Mem:" {printf("(%.2f%%)\n", $3/$2*100)}'```.

<img width="798" alt="Screen Shot 2022-08-02 at 3 51 01" src="https://user-images.githubusercontent.com/66915274/182274627-195476b2-1e17-4a4c-8d5c-2056e4e2bbb6.png">

### 5.5 Disk memory

In order to see the disk memory occupied and available we will use the command ```df``` which means "disk filesystem" , it is used to obtain a complete summary of the disk space usage. As in the sibject indicates the used memory is shown in MB so then we will use the-m flag. Then we will do a grep so that it only shows us the lines that contain "/dev/" and then we will do another grep with the-v flag to exclude the lines that contain "/boot". Finally, we will use the awk command and add the value of the third word of each line so that once all the lines have been added, print the final result of the sum. The entire command is as follows: ```df-m | grep "/dev/" | grep-v "/boot" | awk '{memory_use += $3} END {print memory_use}'```.

<img width="805" alt="Screen Shot 2022-08-03 at 2 26 15" src="https://user-images.githubusercontent.com/66915274/182498837-4f883b25-e316-4c74-8f6b-a5e8b5d13289.png">

To obtain the total space we will use a very similar command. The only differences will be that the values ​​that we will add will be $2 instead of $3 and the other difference is that in the subject the total size appears in Gb so as the result of the sum gives us the number in Mb we must transform it to Gb , for To do this we must divide the number by 1024 and remove the decimals.

<img width="801" alt="Screen Shot 2022-08-03 at 2 40 55" src="https://user-images.githubusercontent.com/66915274/182500104-0aaa1a6b-cf05-4a82-9c9a-8e163f1c1e98.png">

Finally we must show a percentage of the used memory. To do this, again, we will use a command very similar to the previous two. The only thing that we will change is that we will combine the two previous commands to have two variables, one that represents the memory used and the other the total. Once this is done, we will do an operation to get the percentage of ```use/total*100``` and we will print the result of this operation as it appears in the subject , between parentheses and with the % symbol at the end. The final command is this: ```df-m | grep "/dev/" | grep-v "/boot" | awk '{use += $3} {total += $2} END {printf("(%d%%)\n"), use/total*100}'```.

<img width="798" alt="Screen Shot 2022-08-03 at 2 49 33" src="https://user-images.githubusercontent.com/66915274/182500836-dd4b068e-b6ce-4dc6-b832-f90acecfb71c.png">


### 5.6 CPU usage.

In order to see the percentage of CPU usage we will use the ```vmstat``` command, this shows system statistics, allowing us to obtain a general detail of the processes, memory usage, CPU activity, system status, etc. We could put no option but in my case I will put an interval of seconds from 1 to 4. We will also use the ```tail-1``` command, which will allow us to only produce the output of the last line , then of the 4 generated only the last one will be printed. Finally, we will only print word 15, which is the use of available memory. The entire command is as follows: ```vmstat 1 4 | tail-1 | awk '{print %15}'```. The result of this command is only a part of the final result since there is still some operation to be done in the script to make it look good. What we would have to do is subtract from 100 the amount that our command has returned to us, we will print the result of that operation with a decimal and a % at the end and the operation would already be done.

<img width="580" alt="Screen Shot 2022-08-03 at 0 33 39" src="https://user-images.githubusercontent.com/66915274/182484896-def71bf0-b7eb-49d8-b83b-a019d15f62f1.png">

### 5.7 Last reboot

To see the date and time of our last reboot we will use the ```who``` command with the ```-b``` flag since with this flag it will show us on the screen the time of the last system boot. As it has happened to us before, it shows us more information than we want, so we will filter and only show what interests us, for this we will use the awk command and compare if the first word of a line is "system" the third will be printed on the screen word of that line, a space and the fourth word. The entire command would be as follows: ```who-b | awk '$1 == "system" {print $3 " " $4}'```.

<img width="661" alt="Screen Shot 2022-08-02 at 12 24 58" src="https://user-images.githubusercontent.com/66915274/182352895-d985e675-5afc-445a-bcd3-68189702fe70.png">

### 5.8 LVM check

To check if LVM is active or not, we will use the lsblk command, it shows us information on all block devices (hard drives, SSDs, memories, etc.) Among all the information it provides, we can see lvm in the type of manager. For this command we will do an if since we will either print Yes or No. Basically the condition we are looking for will be to count the number of lines in which "lvm" appears and if there are more than 0 we will print Yes, if there is 0 it will print No. All the command would be: ```if [ $(lsblk | grep "lvm" | wc-l)-gt 0 ]; then echo yes; else echo not; fi```.

<img width="801" alt="Screen Shot 2022-08-02 at 22 38 43" src="https://user-images.githubusercontent.com/66915274/182468904-3789e22f-dbde-4874-b153-0d86497c55e2.png">

### 5.9 TCPconnections

To see the number of established TCP connections. We will use the ```ss``` command instead of the deprecated netstat. We will filter with the ```-ta``` flag so that only TCP connections are shown. Finally we will do a grep to see the ones that are established since there is also only listening and we will close with wc-l so that it counts the number of lines. The command looks like this: ```ss-ta | grep ESTAB | wc-l```.

<img width="479" alt="Screen Shot 2022-08-03 at 0 53 36" src="https://user-images.githubusercontent.com/66915274/182487028-746244f8-2cda-4dc7-a14c-b2e5a7e0dc51.png">

### 5.10 Number of users

We will make use of the ```users``` command that will show us the name of the users that exist, knowing this, we will put wc-w so that it counts the number of words that are in the output of the command. The entire command looks like this ```users | wc-w```.

<img width="380" alt="Screen Shot 2022-08-02 at 12 33 29" src="https://user-images.githubusercontent.com/66915274/182354436-282547cf-22c8-4b03-9484-6801c0466de7.png">


### 5.11 IP address & MAC

To obtain the host address we will use the ```hostname-I``` command and to obtain the MAC we will use the ```ip link``` command which is used to display or modify network interfaces. As more than one interface appears, IP's etc. We will use the grep command to find what we want and thus be able to print on the screen only what we are asked for. To do this we will put ```ip link | grep "link/ether" | awk '{print $2}'``` and this way we will only print the MAC.

<img width="639" alt="Screen Shot 2022-08-02 at 14 53 14" src="https://user-images.githubusercontent.com/66915274/182379380-8e3b803d-d001-42ae-8aea-467e8c9f3ea9.png">

### 5.12 Number of sudo usage

In order to obtain the number of commands that are executed with sudo, we will use the jornalctl command, which is a tool that is responsible for collecting and managing system logs. Then we will put ```_COMM=sudo``` in order to filter the entries by specifying their path. In our we put ```_COMM``` since it refers to an executable script. Once we have filtered the search and only the sudo logs appear, we still have to filter a little more since when you start or close the root session it also appears in the log, so to finish filtering we will put a ```grep COMMAND``` and so only the command lines will appear. Finally we will put ```wc-l``` so that the lines are listed. The entire command is as follows: ```journalctl _COMM=sudo | grep COMMAND | wc-l)```. To verify that it works correctly we can run the command in the terminal, put a command that includes sudo and run the command again and it should
increase the number of sudo executions.

<img width="632" alt="Screen Shot 2022-08-02 at 23 50 39" src="https://user-images.githubusercontent.com/66915274/182479668-949b8eee-81f6-4593-83f4-99053d199f1b.png">

### 5.13 End result of the script

⚠️ Remember not to copy and paste if you don't know how each command works ⚠️

```
#!/bin/bash

# FILE
arch=$(uname-a)

# CPU PHYSICAL
cpuf=$(grep "physical id" /proc/cpuinfo | wc-l)

# VIRTUAL-CPU
cpuv=$(grep "processor" /proc/cpuinfo | wc-l)

# RAM
ram_total=$(free--mega | awk '$1 == "Mem:" {print $2}')
ram_use=$(free--mega | awk '$1 == "Mem:" {print $3}')
ram_percent=$(free--mega | awk '$1 == "Mem:" {printf("%.2f"), $3/$2*100}')

# DISK
disk_total=$(df-m | grep "/dev/" | grep-v "/boot" | awk '{disk_t += $2} END {printf ("%.1fGb\n"), disk_t/1024}')
disk_use=$(df-m | grep "/dev/" | grep-v "/boot" | awk '{disk_u += $3} END {print disk_u}')
disk_percent=$(df-m | grep "/dev/" | grep-v "/boot" | awk '{disk_u += $3} {disk_t+= $2} END {printf("%d"), disk_u/disk_t* 100}')

# CPU LOAD
cpul=$(vmstat 1 2 | tail-1 | awk '{printf $15}')
cpu_op=$(expr 100-$cpul)
cpu_end=$(printf "%.1f" $cpu_op)

# LAST BOOT
lb=$(who-b | awk '$1 == "system" {print $3 " " $4}')

# LVM USE
lvmu=$(if [ $(lsblk | grep "lvm" | wc-l)-gt 0 ]; then echo yes; else echo no; fi)

# TCP CONNECTIONS
tcpc=$(ss-ta | grep ESTAB | wc-l)

# USER LOG
ulog=$(users | wc-w)

# NETWORK
ip=$(hostname-I)
mac=$(ip link | grep "link/ether" | awk '{print $2}')

# SUDO
cmnd=$(journalctl _COMM=sudo | grep COMMAND | wc-l)

wall "	Architecture: $arch
	CPU physical: $cpuf
	vCPU: $cpuv
	Memory Usage: $ram_use/${ram_total}MB ($ram_percent%)
	Disk Usage: $disk_use/${disk_total} ($disk_percent%)
	CPU load: $cpu_fin%
	Last boot: $lb
	LVM use: $lvmu
	Connections TCP: $tcpc ESTABLISHED
	User log: $ulog
	Network: IP $ip ($mac)
	Sudo: $cmnd cmd"
```
Script seen from nano ↙️

<img width="911" alt="Screen Shot 2022-08-03 at 3 47 31" src="https://user-images.githubusercontent.com/66915274/182506484-f5a095b8-4751-461e-a114-f8e36b4cfa9a.png">

Result after executing the script ↙️

<img width="796" alt="Screen Shot 2022-08-03 at 3 46 15" src="https://user-images.githubusercontent.com/66915274/182506357-f5466a97-380b-4b6d-9b79-89e01a31498a.png">

## 6-Crontab ⏰

🧠 <b>What is crontab? </b>It is a background process manager. The indicated processes will be executed at the time you specify in the crontab file.

To have crontab correctly configured we must edit the crontab file with the following command ```sudo crontab-u root-e```.

In the file we must add the following command so that the script is executed every 10 minutes ```*/10 * * * * sh /path of the script```.

<img width="798" alt="Screen Shot 2022-08-03 at 4 40 18" src="https://user-images.githubusercontent.com/66915274/182512395-eaebabc2-5866-4ae3-966c-1a80818cde07.png">

Operation of each crontab parameter:

m ➤ Corresponds to the minute in which the script is going to be executed, the value ranges from 0 to 59.

h ➤ The exact time, the 24-hour format is used, the values ​​range from 0 to 23, with 0 being 12:00 midnight.
sun ➤ refers to the day of the month, for example you can specify 15 if you want to run every 15th.

dow ➤ Means the day of the week, it can be numeric (0 to 7, where 0 and 7 are Sunday) or the first 3 letters of the day in English: mon, tue, wed, thu, fri, sat, sun.

user ➤ Defines the user that is going to execute the command, it can be root, or another different user as long as it has permissions to execute the script.

command ➤ Refers to the command or the absolute path of the script to execute.

## 7-Signature.txt 📝

To obtain the signature, the first thing we must do is turn off the virtual machine since once you turn it on or modify something, the signature will change.

<img width="834" alt="Screen Shot 2022-08-03 at 4 47 32" src="https://user-images.githubusercontent.com/66915274/182513283-1cfc319f-982d-47cf-a596-8475d4c96616.png">

The next step will be to locate ourselves in the path where we have the .vdi of our virtual machine.

<img width="465" alt="Screen Shot 2022-08-03 at 4 57 37 AM" src="https://user-images.githubusercontent.com/66915274/182514499-f0ad5ba7-c0c2-493e-b0ae-9b79c970816e.png">

Finally we will do ```shasum hostname.vdi``` and this will give us the signature. The result of this signature is what we will have to add to our signature.txt file to later upload the file to the intra repository. It is very important not to open the machine again since the signature will be modified. For the corrections, remember to clone the machine so that you can turn it on without fear of the signature changing.

🧠 <b> What is shasum ❓ </b> It is a command that allows to identify the integrity of a file through the checksum of the SHA-1 hash of a file.

<img width="416" alt="Screen Shot 2022-08-03 at 4 58 48 AM" src="https://user-images.githubusercontent.com/66915274/182514627-f11026d0-de0d-447d-a2e4-31a3c1af0f35.png">

## 8-Bonuses ⭐️

### 8.1-Manual partition

1 ◦ At the time of choosing the disk partitioning we will select manual. In this way we can edit the partitions one by one.

<img width="789" alt="Screen Shot 2022-10-23 at 4 30 48 PM" src="https://user-images.githubusercontent.com/66915274/197397840-b6ae9d65-a6aa-4a5d-a03f-856d9ce81644.png">

2 ◦ In this section it shows us a general description of our partitions and mounting points. We currently have no partitions made. To create a new partition table we must choose the device where we want to create them. In our case we will choose the only one available.

<img width="793" alt="Screen Shot 2022-10-23 at 4 35 39 PM" src="https://user-images.githubusercontent.com/66915274/197398114-44abc561-d34d-47c9-b512-581b4ec6fddb.png">

3 ◦ We accept the confirmation message. Basically it tells us that if there are already partitions on the device they will be deleted and that if we are sure to create a new empty partition table.

<img width="770" alt="Screen Shot 2022-10-23 at 4 36 08 PM" src="https://user-images.githubusercontent.com/66915274/197398137-b9fe1f96-5907-462e-8a50-44b71ae2aefe.png">

4 ◦ Once we have completed the previous step we can see how our empty partition table appears. Now we must configure it, for this we must select it.

<img width="786" alt="Screen Shot 2022-10-23 at 4 36 35 PM" src="https://user-images.githubusercontent.com/66915274/197398172-b05fa7aa-e5b4-40cb-afd4-03a1404d7885.png">

5 ◦ We will create a new partition.

<img width="512" alt="Screen Shot 2022-10-23 at 4 36 54 PM" src="https://user-images.githubusercontent.com/66915274/197398199-70570553-de1b-49a9-8c44-da9a1e4b5c1e.png">

We'll start by creating this:

![image](https://user-images.githubusercontent.com/66915274/197427077-48636236-4012-4edf-b0e4-319db502e685.png)

6 ◦ As the subject indicates, the size of the partition must be 500 megabytes.

<img width="777" alt="Screen Shot 2022-10-23 at 4 37 27 PM" src="https://user-images.githubusercontent.com/66915274/197398241-604b2bb2-7303-412a-b382-40bfbf443ed0.png">

7 ◦ We choose the type of the partition. We choose primary since it will be the partition where the Operating System will be installed.

<img width="457" alt="Screen Shot 2022-10-23 at 4 37 38 PM" src="https://user-images.githubusercontent.com/66915274/197398253-2c0f8205-3d3f-4ab7-94a3-70c37ee014d9.png">

Brief description of all types of partitions:

◦ <b>Primary:</b> The only partition on which an OS can be installed. There can only be 4 primary partitions per hard drive or 3 primary and one extended.

◦ <b>Secondary/Extended:</b> It was designed to break the limitation of 4 primary partitions on a single physical disk. Only one such partition can exist per disk, and it is only used to contain logical partitions.

◦ <b>Logical:</b> Occupies a portion of the extended/primary partition or all of it, which has been formatted with a specific type of file system (in our case we will use ext4) and has been assigned a drive, so the operating system recognizes the logical partitions or their file system. There can be a maximum of 23 logical partitions in an extended partition, however the linux OS we currently work with reduces it to 15, more than enough to carry out this project.

8 ◦ We will select beginning since we want the new partition to be created at the beginning of the available space.

<img width="787" alt="Screen Shot 2022-10-23 at 4 37 52 PM" src="https://user-images.githubusercontent.com/66915274/197398265-c63d7b32-55b7-45ad-86b3-166e44cfd598.png">

9 ◦ The following Screen Shot shows us the details of the partition. We will modify the mount point to the one specified by the subject.

<img width="781" alt="Screen Shot 2022-10-23 at 4 38 27 PM" src="https://user-images.githubusercontent.com/66915274/197398293-2487ded0-2584-48c4-a5ea-1f2464ec39f9.png">

10 ◦ We choose boot as the mount point of our partition.

<img width="577" alt="Screen Shot 2022-10-23 at 4 38 49 PM" src="https://user-images.githubusercontent.com/66915274/197398322-51b9854b-ab32-4d81-8126-3ef3913858a6.png">

11 ◦ We finished configuring the current partition.

<img width="787" alt="Screen Shot 2022-10-23 at 4 39 07 PM" src="https://user-images.githubusercontent.com/66915274/197398336-72b17153-73dc-48a5-b7d3-839877e8983b.png">

12 ◦ Once we have completed the previous step, the partition should appear. Now we must create a logical partition with all the available space on the disk, that does not have a mount point and that is encrypted. To do this we select the free space where we want to create it.

<img width="781" alt="Screen Shot 2022-10-23 at 4 39 37 PM" src="https://user-images.githubusercontent.com/66915274/197398367-ee8a1f5d-3941-4a86-a775-90f29b1c955e.png">

![image](https://user-images.githubusercontent.com/66915274/197431553-718358bb-6570-41dd-b114-09acc347999d.png)

13 ◦ We create a new partition.

<img width="462" alt="Screen Shot 2022-10-23 at 4 39 58 PM" src="https://user-images.githubusercontent.com/66915274/197398396-843c7fb3-b945-4305-a960-02aa9d4ca940.png">

14 ◦ We select the maximum size.

<img width="779" alt="Screen Shot 2022-10-23 at 4 40 26 PM" src="https://user-images.githubusercontent.com/66915274/197398425-63205376-839f-4986-a8d0-981cdaa380e4.png">

15 ◦ We select the type of partition, in this case logical.

<img width="466" alt="Screen Shot 2022-10-23 at 4 40 53 PM" src="https://user-images.githubusercontent.com/66915274/197398448-49c99180-9a3d-4dd4-a9ce-d680bfdefa1c.png">

16 ◦ We will modify the mount point.

<img width="788" alt="Screen Shot 2022-10-23 at 4 41 44 PM" src="https://user-images.githubusercontent.com/66915274/197398500-188cc4fb-4eb5-4a56-893b-58838877c056.png">

17 ◦ We will choose the option of not mounting it.

<img width="590" alt="Screen Shot 2022-10-23 at 4 42 11 PM" src="https://user-images.githubusercontent.com/66915274/197398518-f6fb7588-8c53-40a9-9ceb-238d6a62d942.png">

18 ◦ We finish configuring the current partition.

<img width="788" alt="Screen Shot 2022-10-23 at 4 42 41 PM" src="https://user-images.githubusercontent.com/66915274/197398541-922f2c4d-ed5a-4d92-8083-ccf57aec3dee.png">

19 ◦ We will configure encrypted volumes. In order to encrypt our partition.

<img width="786" alt="Screen Shot 2022-10-23 at 4 43 08 PM" src="https://user-images.githubusercontent.com/66915274/197398562-2369fa90-7db9-4ba3-abed-7ac15ede8b81.png">

20 ◦ We accept the confirmation message.

<img width="777" alt="Screen Shot 2022-10-23 at 4 43 27 PM" src="https://user-images.githubusercontent.com/66915274/197398573-9720e351-04f4-49f0-a3dc-fe0ce1ada296.png">

21 ◦ We create the encrypted volumes.

<img width="596" alt="Screen Shot 2022-10-23 at 4 43 46 PM" src="https://user-images.githubusercontent.com/66915274/197398595-b36ab8da-86c6-483a-99fd-079293a92570.png">

22 ◦ We select in which partition we want to perform the encryption.

<img width="568" alt="Screen Shot 2022-10-23 at 4 44 06 PM" src="https://user-images.githubusercontent.com/66915274/197398615-7c9f8e45-7885-4f39-84eb-e3a056eeb2c7.png">

23 ◦ We finish configuring the current partition.

<img width="787" alt="Screen Shot 2022-10-23 at 4 44 35 PM" src="https://user-images.githubusercontent.com/66915274/197398649-06749ec8-903d-4b1a-af2a-c2dad77bcaec.png">

24 ◦ We finish since we do not want to create more encrypted volumes.

<img width="589" alt="Screen Shot 2022-10-23 at 4 44 49 PM" src="https://user-images.githubusercontent.com/66915274/197398663-0bd74c65-b3fd-430c-b3e6-4f1e0c76ae8d.png">

25 ◦ We accept the confirmation message. He tells us that everything inside the partition will be encrypted and that it shouldn't take long to finish.

<img width="783" alt="Screen Shot 2022-10-23 at 4 45 06 PM" src="https://user-images.githubusercontent.com/66915274/197398670-91db3e3e-b271-4e1b-ad8a-28ceb06e0897.png">

26 ◦ We do not care if it takes a long time or a short time, we click cancel since there is nothing to encrypt since the partition is empty.

<img width="789" alt="Screen Shot 2022-10-23 at 4 45 27 PM" src="https://user-images.githubusercontent.com/66915274/197398685-6603ef31-d499-46da-949f-ade8e2a05bf9.png">

27 ◦ Again we will have to put a password, this time it will be the encryption phrase. As I have previously mentioned, you must repeat the process and you must write it down since it will be important in the future.

<img width="779" alt="Screen Shot 2022-10-23 at 4 48 38 PM" src="https://user-images.githubusercontent.com/66915274/197398855-0c93f419-897e-4eee-9499-18321d8e8dfd.png">

28 ◦ We repeat the encryption phrase.

<img width="722" alt="Screen Shot 2022-10-23 at 4 49 01 PM" src="https://user-images.githubusercontent.com/66915274/197398875-3fa85638-7105-42bf-bbc2-e189fbbc1918.png">

29 ◦ We will configure the logical volume manager.

<img width="785" alt="Screen Shot 2022-10-23 at 4 50 17 PM" src="https://user-images.githubusercontent.com/66915274/197398933-85e0025e-0a4d-41f0-8fd0-5f0c8ee32e9b.png">

30 ◦ We will accept the confirmation message since we agree that the changes are saved on the disk.

<img width="786" alt="Screen Shot 2022-10-23 at 4 50 42 PM" src="https://user-images.githubusercontent.com/66915274/197398945-d79ea2a7-a13e-4e6a-9e9c-40bdcd2dd502.png">

31 ◦ We will create a new volume group. Volume groups group partitions.

<img width="454" alt="Screen Shot 2022-10-23 at 4 52 04 PM" src="https://user-images.githubusercontent.com/66915274/197399021-29b21274-37c1-4fd9-8526-962969d1cce3.png">

32 ◦ We will enter the name we want to give it. ```LVMGroup``` as indicated by the subject.

<img width="695" alt="Screen Shot 2022-10-23 at 4 52 58 PM" src="https://user-images.githubusercontent.com/66915274/197399065-1ac8d80d-9e18-4b4a-a60f-11496e7de26d.png">

33 ◦ We will select the partition where we want to create the group.

<img width="590" alt="Screen Shot 2022-10-23 at 4 53 22 PM" src="https://user-images.githubusercontent.com/66915274/197399089-5ea5f48e-176c-4278-8b14-a13b7f5ee45c.png">

34 ◦ Now we must create all the logical partitions. By having to repeat the same actions several times, there are captures that will not be documented.

![image](https://user-images.githubusercontent.com/66915274/197439138-889d6368-1875-402b-a094-bd146bb7cb8a.png)


<img width="457" alt="Screen Shot 2022-10-23 at 4 53 50 PM" src="https://user-images.githubusercontent.com/66915274/197399108-fb566eb4-664f-4509-8948-ab4ed04407b5.png">

35 ◦ We will start by choosing the group where we want them to be created. We select the only one available (the one we just created).

<img width="760" alt="Screen Shot 2022-10-23 at 4 54 02 PM" src="https://user-images.githubusercontent.com/66915274/197399115-e7d3b313-763c-421c-a71d-850d318432e7.png">

36 ◦ The order of the creation of the logical units will be the same as that indicated by the subject, so we will start with root and end with var-log. Then we will select the name of the logical volume.

<img width="662" alt="Screen Shot 2022-10-23 at 4 55 42 PM" src="https://user-images.githubusercontent.com/66915274/197399188-6ae8c83b-057d-498f-b112-9116079b0808.png">

37 ◦ Size, as indicated by the subject, will be 10g.

<img width="782" alt="Screen Shot 2022-10-23 at 4 56 21 PM" src="https://user-images.githubusercontent.com/66915274/197399216-c65f43ca-fb8e-4d05-9212-24ad2ee87b39.png">

38 ◦ We repeat the process for ```swap```. We will only change the name and size.

<img width="443" alt="Screen Shot 2022-10-23 at 4 56 49 PM" src="https://user-images.githubusercontent.com/66915274/197399239-c26598cb-e7bb-474c-aece-90f043e1990f.png">

<img width="751" alt="Screen Shot 2022-10-23 at 4 57 26 PM" src="https://user-images.githubusercontent.com/66915274/197399278-c5cd5a9c-2ab1-42b9-8871-b58e9b33b4b6.png">

<img width="667" alt="Screen Shot 2022-10-23 at 4 57 41 PM" src="https://user-images.githubusercontent.com/66915274/197399288-7ecf6adf-aaf5-46bf-959f-2159d19b7bbf.png">

<img width="782" alt="Screen Shot 2022-10-23 at 4 58 11 PM" src="https://user-images.githubusercontent.com/66915274/197399310-fc6c397e-8257-4e06-8fba-ad35431c9b96.png">

39 ◦ We repeat the process for ```home```. We will only change the name and size.

<img width="476" alt="Screen Shot 2022-10-23 at 4 58 57 PM" src="https://user-images.githubusercontent.com/66915274/197399347-a815d58b-686e-4d9d-bb5c-34a7b54476ab.png">

<img width="756" alt="Screen Shot 2022-10-23 at 4 59 07 PM" src="https://user-images.githubusercontent.com/66915274/197399355-28617029-c28c-4ca4-b56b-646e066cded6.png">

<img width="672" alt="Screen Shot 2022-10-23 at 5 01 13 PM" src="https://user-images.githubusercontent.com/66915274/197399433-1e9c7110-9240-4982-9835-b026ed73171f.png">

<img width="770" alt="Screen Shot 2022-10-23 at 5 04 34 PM" src="https://user-images.githubusercontent.com/66915274/197399610-247a7a35-0141-4c14-884e-7ecd07caa96d.png">

40 ◦ We repeat the process for ```var```. We will only change the name and size.

<img width="482" alt="Screen Shot 2022-10-23 at 5 05 10 PM" src="https://user-images.githubusercontent.com/66915274/197399644-58da651c-f4ad-4d1e-b128-de87c92cc292.png">

<img width="700" alt="Screen Shot 2022-10-23 at 5 05 30 PM" src="https://user-images.githubusercontent.com/66915274/197399662-32ab0a06-c14d-4a0e-ac80-cb0d12fc24eb.png">

<img width="774" alt="Screen Shot 2022-10-23 at 5 06 03 PM" src="https://user-images.githubusercontent.com/66915274/197399693-b49c2ffe-b21a-43c5-bd3f-160bc544b072.png">

41 ◦ We repeat the process for ```srv```. We will only change the name.

<img width="446" alt="Screen Shot 2022-10-23 at 5 06 14 PM" src="https://user-images.githubusercontent.com/66915274/197399702-6d531de3-690d-458d-9a3b-bf6ceedd7cda.png">

<img width="754" alt="Screen Shot 2022-10-23 at 5 06 39 PM" src="https://user-images.githubusercontent.com/66915274/197399724-0fdd75ad-e978-4468-8509-a62cdc4a3faf.png">

<img width="671" alt="Screen Shot 2022-10-23 at 5 06 57 PM" src="https://user-images.githubusercontent.com/66915274/197399744-b82b1dcd-09c7-44cc-a2ab-b6079abcbb5a.png">

<img width="771" alt="Screen Shot 2022-10-23 at 5 07 13 PM" src="https://user-images.githubusercontent.com/66915274/197399757-94732b16-585e-4f7d-a20f-f7ef0814b4e7.png">

42 ◦ We repeat the process for ```tmp```. We will only change the name.

<img width="481" alt="Screen Shot 2022-10-23 at 5 07 34 PM" src="https://user-images.githubusercontent.com/66915274/197399777-9d871f2a-856d-4b4d-ad18-1195001b0fdf.png">

<img width="732" alt="Screen Shot 2022-10-23 at 5 07 46 PM" src="https://user-images.githubusercontent.com/66915274/197399792-0794ace5-c236-4f68-b023-bb471753eba2.png">

<img width="659" alt="Screen Shot 2022-10-23 at 5 07 55 PM" src="https://user-images.githubusercontent.com/66915274/197399798-84a31102-6953-468b-85d4-0a248e98cb17.png">

<img width="768" alt="Screen Shot 2022-10-23 at 5 08 19 PM" src="https://user-images.githubusercontent.com/66915274/197399827-5dfc8571-e82c-4a28-aae7-dc716fb6e77b.png">

43 ◦ Finally we repeat the process for ```var-log```. We will only change the name and size.

<img width="448" alt="Screen Shot 2022-10-23 at 5 08 34 PM" src="https://user-images.githubusercontent.com/66915274/197399838-2cd49171-45dd-469a-887c-3ce99d84b7cd.png">

<img width="762" alt="Screen Shot 2022-10-23 at 5 08 40 PM" src="https://user-images.githubusercontent.com/66915274/197399841-04b75112-4d21-456c-bf50-8335839764e0.png">

<img width="658" alt="Screen Shot 2022-10-23 at 5 08 59 PM" src="https://user-images.githubusercontent.com/66915274/197399859-d706de2e-bb20-4a04-96db-4dd57b3778be.png">

<img width="779" alt="Screen Shot 2022-10-23 at 5 09 28 PM" src="https://user-images.githubusercontent.com/66915274/197399886-a1e9ee69-78a4-4071-af99-2192d535c6cd.png">


44 ◦ Once we have completed all the previous steps we will finish the configuration of the logical volume manager.

<img width="438" alt="Screen Shot 2022-10-23 at 5 09 51 PM" src="https://user-images.githubusercontent.com/66915274/197399904-c584fcdf-eb38-486f-af12-7374f1e04465.png">

45 ◦ Now we can see how in the section where all our partitions and free space are shown, all the logical partitions that we have just created already appear. Well, we must configure all of them to select the file system we want and the mount point indicated by the subject. Again we will go in order and select the first one that appears, which is ```home```.

<img width="783" alt="Screen Shot 2022-10-23 at 5 10 36 PM" src="https://user-images.githubusercontent.com/66915274/197399944-bccbe599-b80a-4abe-ac6c-d770447ea727.png">

46 ◦ It shows us the configuration of the partition. We must choose a file system since it currently does not have one.

<img width="782" alt="Screen Shot 2022-10-23 at 5 10 55 PM" src="https://user-images.githubusercontent.com/66915274/197399976-9b871bda-9425-4dbe-b8c9-25c8c6d6c811.png">

47 ◦ We choose the Ext4 file system, it is the most used file system in Linux distributions.

<img width="412" alt="Screen Shot 2022-10-23 at 5 11 18 PM" src="https://user-images.githubusercontent.com/66915274/197400000-2e855fc9-10b1-4f3e-9c58-85b6ff02a4fb.png">

48 ◦ Now we must select the mount point.

<img width="782" alt="Screen Shot 2022-10-23 at 5 11 44 ​​PM" src="https://user-images.githubusercontent.com/66915274/197400023-387a70aa-b491-43c0-91d2-cb378da9fc75.png">

49 ◦ We select ```home``` as indicated by the subject.

<img width="515" alt="Screen Shot 2022-10-23 at 5 11 54 PM" src="https://user-images.githubusercontent.com/66915274/197400040-e79cad4f-368b-4cee-9ec0-942f38b2f785.png">

50 ◦ Once we have selected it, we will finish the partition configuration.

<img width="785" alt="Screen Shot 2022-10-23 at 5 12 10 PM" src="https://user-images.githubusercontent.com/66915274/197400059-ab96f2c4-cd92-47cb-a9ee-61257537ee6a.png">

51 ◦ Again these steps can get very repetitive so I won't comment too much. We repeat everything the same (except the mount point) for ```root```.

<img width="782" alt="Screen Shot 2022-10-23 at 5 13 36 PM" src="https://user-images.githubusercontent.com/66915274/197400135-c08444fe-e39d-45fa-a3b6-3c73db2a4935.png">

<img width="782" alt="Screen Shot 2022-10-23 at 5 13 53 PM" src="https://user-images.githubusercontent.com/66915274/197400146-41ce0b0c-142c-46b4-a3c5-918676a3a852.png">

<img width="421" alt="Screen Shot 2022-10-23 at 5 14 08 PM" src="https://user-images.githubusercontent.com/66915274/197400155-92759327-5671-41f4-8104-dd1de4bc88cb.png">

<img width="775" alt="Screen Shot 2022-10-23 at 5 14 22 PM" src="https://user-images.githubusercontent.com/66915274/197400171-6fd04783-e833-4afd-a753-4b943133a4ab.png">

<img width="525" alt="Screen Shot 2022-10-23 at 5 14 39 PM" src="https://user-images.githubusercontent.com/66915274/197400182-780e1917-3f77-4986-b0e8-b50a90d75403.png">

<img width="790" alt="Screen Shot 2022-10-23 at 5 14 52 PM" src="https://user-images.githubusercontent.com/66915274/197400186-88da831a-c672-4ec0-a64c-0ad2808bb6c5.png">

52 ◦ We repeat the process for ```srv``` and change the mount point.

<img width="778" alt="Screen Shot 2022-10-23 at 5 15 05 PM" src="https://user-images.githubusercontent.com/66915274/197400198-599b4aa3-a511-45d1-86b0-dd42da4c380f.png">

<img width="778" alt="Screen Shot 2022-10-23 at 5 15 31 PM" src="https://user-images.githubusercontent.com/66915274/197400218-e6b26eb7-7933-426f-a7cd-a791400ebdab.png">

<img width="428" alt="Screen Shot 2022-10-23 at 5 15 37 PM" src="https://user-images.githubusercontent.com/66915274/197400222-95107b34-8d28-4d4d-a74b-7de6c6a46d33.png">

<img width="787" alt="Screen Shot 2022-10-23 at 5 15 44 PM" src="https://user-images.githubusercontent.com/66915274/197400227-20c13dc0-52cd-4c70-bf4e-531979c54a3e.png">

<img width="530" alt="Screen Shot 2022-10-23 at 5 15 52 PM" src="https://user-images.githubusercontent.com/66915274/197400238-3b403294-74d1-4e63-aca7-7d83447ed5b8.png">

<img width="790" alt="Screen Shot 2022-10-23 at 5 16 04 PM" src="https://user-images.githubusercontent.com/66915274/197400249-035f6b9d-3716-4565-9776-aa0af49b3fd7.png">

53 ◦ For ```swap``` we will make an exception since the file system will be different. We select ```swap```.

<img width="780" alt="Screen Shot 2022-10-23 at 5 16 32 PM" src="https://user-images.githubusercontent.com/66915274/197400272-112b44ef-4996-438a-90b8-6620cdd7d2ff.png">

54 ◦ When selecting the file system, we leave it in ```swap area```.

<img width="785" alt="Screen Shot 2022-10-23 at 5 16 41 PM" src="https://user-images.githubusercontent.com/66915274/197400281-e12ee636-8696-4bee-9198-862b7d6be199.png">

55 ◦ Once the previous step is done, we will finish the partition configuration.

<img width="370" alt="Screen Shot 2022-10-23 at 5 16 59 PM" src="https://user-images.githubusercontent.com/66915274/197400297-8eed129d-0ec0-49a8-8b2a-dd0d04055f75.png">

<img width="787" alt="Screen Shot 2022-10-23 at 5 17 09 PM" src="https://user-images.githubusercontent.com/66915274/197400309-74e83209-4b2a-4e27-9a67-44373c1db362.png">

56 ◦ Now we will do the same as before but now we will do it with ```tmp``` and changing the mount point.

<img width="777" alt="Screen Shot 2022-10-23 at 5 17 41 PM" src="https://user-images.githubusercontent.com/66915274/197400341-608516f6-0f5a-4cdd-83d8-c8fbd1635624.png">

<img width="778" alt="Screen Shot 2022-10-23 at 5 17 49 PM" src="https://user-images.githubusercontent.com/66915274/197400346-e9647c7a-a9a2-4a0f-b439-a912247fb3f9.png">

<img width="372" alt="Screen Shot 2022-10-23 at 5 18 01 PM" src="https://user-images.githubusercontent.com/66915274/197400360-1816d06a-252e-4d41-b1a2-fc547961f353.png">

<img width="781" alt="Screen Shot 2022-10-23 at 5 18 08 PM" src="https://user-images.githubusercontent.com/66915274/197400370-0474b71f-c1c3-445f-ba02-088dc1c64ce3.png">

<img width="496" alt="Screen Shot 2022-10-23 at 5 18 24 PM" src="https://user-images.githubusercontent.com/66915274/197400386-f66494c5-97b9-4bb9-8c75-5856d69d26cc.png">

<img width="783" alt="Screen Shot 2022-10-23 at 5 18 40 PM" src="https://user-images.githubusercontent.com/66915274/197400405-4a368bfb-f862-4bbd-a33e-b87c3038d232.png">

57 ◦ We repeat the process again for ```var``` changing the mount point.

<img width="773" alt="Screen Shot 2022-10-23 at 5 19 13 PM" src="https://user-images.githubusercontent.com/66915274/197400447-85bcad13-8083-4aec-acb2-fa467e5d4e33.png">

<img width="790" alt="Screen Shot 2022-10-23 at 5 19 21 PM" src="https://user-images.githubusercontent.com/66915274/197400452-aed22368-4889-4c04-bf60-5a06fb93944e.png">

<img width="386" alt="Screen Shot 2022-10-23 at 5 19 28 PM" src="https://user-images.githubusercontent.com/66915274/197400459-b6f59948-e804-414a-b41d-21d2f495fccc.png">

<img width="780" alt="Screen Shot 2022-10-23 at 5 19 36 PM" src="https://user-images.githubusercontent.com/66915274/197400462-788d29e5-7798-418a-8725-3cb8dd2849bd.png">

<img width="515" alt="Screen Shot 2022-10-23 at 5 19 51 PM" src="https://user-images.githubusercontent.com/66915274/197400473-4508d9d6-481d-4f3a-9630-6c1eba7c5cc0.png">

<img width="779" alt="Screen Shot 2022-10-23 at 5 20 00 PM" src="https://user-images.githubusercontent.com/66915274/197400482-1f8c147f-66d8-438b-866f-3e9eff75ef5e.png">

58 ◦ Finally we repeat the process again for ```var-log``` in this we will have to manually enter the mount point.

<img width="772" alt="Screen Shot 2022-10-23 at 5 20 23 PM" src="https://user-images.githubusercontent.com/66915274/197400513-53b3f899-47f5-4cdb-ab4b-205b1d1bce31.png">

![image](https://user-images.githubusercontent.com/66915274/197602511-fa34155b-3244-4b0c-8054-2778edecfb16.png)

![image](https://user-images.githubusercontent.com/66915274/197602585-03b540af-5d7a-4364-b90a-559bac0cb2a2.png)

![image](https://user-images.githubusercontent.com/66915274/197602630-cc749189-9ac9-48bc-a595-dc33282840ec.png)

![image](https://user-images.githubusercontent.com/66915274/197602673-5c18be85-1b0f-430b-b507-66711b807115.png)

![image](https://user-images.githubusercontent.com/66915274/197602699-fddadd2d-c54d-4313-8165-a93db1249b26.png)

![image](https://user-images.githubusercontent.com/66915274/197602741-431bd866-1558-4735-bb34-ab57dc5745b7.png)

59 ◦ Once we have completed all the previous steps, we are almost finished, we must click on finalize the partitioning and thus save all the changes on the disk.

![image](https://user-images.githubusercontent.com/66915274/197602907-4a3ba459-1a5d-468e-81dc-5206403cf034.png)

60 ◦ We accept the message and the changes will be saved. Make sure that all partitions are the same as in the screenshot.

![image](https://user-images.githubusercontent.com/66915274/197602944-13ca67b2-bcc5-476c-84dc-aadc5e1d3baf.png)

61 ◦ We select the ```No``` option since we do not need additional packages.

<img width="770" alt="Screen Shot 2022-07-13 at 20 05 42" src="https://user-images.githubusercontent.com/66915274/178801099-2dda24f5-0d46-4184-8c44-a8fe0bf46527.png">

62 ◦ We choose our Country.

<img width="756" alt="Screen Shot 2022-07-13 at 20 14 23" src="https://user-images.githubusercontent.com/66915274/178802653-d9e8504a-b60b-4441-8ee3-8d48ca4a6bf0.png">

63 ◦ We choose ```deb.debian.org``` since taking into account our region is where we will have a better connection.

<img width="792" alt="Screen Shot 2022-07-13 at 20 15 00" src="https://user-images.githubusercontent.com/66915274/178802772-4f67cd99-60d5-4439-8502-317e81e07d70.png">

64 ◦ We will leave this option empty and click ```Continue``` directly.

<img width="797" alt="Screen Shot 2022-07-13 at 20 17 24" src="https://user-images.githubusercontent.com/66915274/178803208-2969acae-3fa7-423e-8a3c-bb7c76eff824.png">

65 ◦ We select the ```No``` option since we don't want developers to see our statistics even if they are anonymous.

<img width="796" alt="Screen Shot 2022-07-13 at 20 21 54" src="https://user-images.githubusercontent.com/66915274/178803926-a4efbc70-f3e2-4e6c-9809-9152478d8237.png">

66 ◦ We will remove all the software options (with the space bar) and we will give ```Continue```.

<img width="797" alt="Screen Shot 2022-07-13 at 20 24 17" src="https://user-images.githubusercontent.com/66915274/178804377-e775b89e-93d4-482f-a4d0-0ef126f47719.png">

67 ◦ We will select ```Yes``` to install [GRUB boot](https://en.wikipedia.org/wiki/GNU_GRUB) on the hard drive.

<img width="792" alt="Screen Shot 2022-07-13 at 20 26 24" src="https://user-images.githubusercontent.com/66915274/178804771-ba16e0b7-9f06-4c5b-9451-0bfd65efd2bb.png">

68 ◦ We will choose the device for the bootloader installation ```/dev/sda (ata_VBOX_HARDDISK)```.

<img width="792" alt="Screen Shot 2022-07-13 at 20 35 46" src="https://user-images.githubusercontent.com/66915274/178806441-f1bf3159-4e09-4c9a-9102-b3261c9000d8.png">

69 ◦ We will click ```Continue``` to finish the installation.

<img width="794" alt="Screen Shot 2022-07-13 at 20 39 30" src="https://user-images.githubusercontent.com/66915274/178807102-e2a9722e-791f-48a0-ae35-b05b36a37ed2.png">

70 ◦ Once we have finished installing debian, we must configure our virtual machine.

[Click here to go to the virtual machine configuration ⚙️](#4-virtual-machine-configuration-%EF%B8%8F)

### 8.2-Wordpress & services configuration 🌐
### WordPress and services coming soon... 🔜🛠

### Lighttpd

🧠 <b>What is Lighttpd❓</b>

1 ◦ Installation of lighttpd packages.

<img width="791" alt="Screen Shot 2022-10-27 at 4 09 24 AM" src="https://user-images.githubusercontent.com/66915274/198174389-428c30e0-c437-4bc1-b8df-40dd2fb0c0ce.png">

2 ◦ We allow connections through port 80 with the command ```sudo ufw allow 80```.

<img width="306" alt="Screen Shot 2022-10-27 at 4 15 24 AM" src="https://user-images.githubusercontent.com/66915274/198175046-8ea3f052-32f1-4107-a9a1-c9271d6c9ce6.png">

3 ◦ We check that we have really allowed. Port 80 and allow should appear.

<img width="460" alt="Screen Shot 2022-10-27 at 4 15 45 AM" src="https://user-images.githubusercontent.com/66915274/198175075-da6833f1-2360-4e08-b708-99f920b8215c.png">

### Mariadb

🧠 <b>What is MariaDB❓</b>


<img width="797" alt="Screen Shot 2022-10-27 at 4 17 09 AM" src="https://user-images.githubusercontent.com/66915274/198175218-65dec75f-5727-425c-97d0-2baa2b8cd457.png">

<img width="629" alt="Screen Shot 2022-10-27 at 4 19 25 AM" src="https://user-images.githubusercontent.com/66915274/198175511-d826b699-770e-4142-b464-cd6a91211d6a.png">

<img width="704" alt="Screen Shot 2022-10-27 at 1 00 20 AM" src="https://user-images.githubusercontent.com/66915274/198175719-b22bd572-ab50-4590-9298-5f5a69f98862.png">

<img width="551" alt="Screen Shot 2022-10-27 at 1 00 40 AM" src="https://user-images.githubusercontent.com/66915274/198175732-eff97e65-d8ef-4b44-8930-62d58d910598.png">

### phpmyadmin

🧠 <b>What is Phpmyadmin❓</b>

<img width="733" alt="Screen Shot 2022-10-27 at 4 22 33 AM" src="https://user-images.githubusercontent.com/66915274/198175891-74168b70-13e1-41a6-a46d-74fe03077a2e.png">

<img width="641" alt="Screen Shot 2022-10-27 at 1 13 56 AM" src="https://user-images.githubusercontent.com/66915274/198175978-8744b575-c23e-4563-80de-1f733df9341d.png">

<img width="578" alt="Screen Shot 2022-10-27 at 4 26 55 AM" src="https://user-images.githubusercontent.com/66915274/198176405-f6bf2457-1174-4571-a495-d96ba80f5b83.png">




<br>
<br>
<br>

#
# This tutorial has taken a lot of work, if you think it has been useful I would really appreciate starred 🌟 so that it can be shared and help more students 👨🏻‍🎓❤️
<br>
<br>
<br>


## 9-Correction sheet ✅

### Don't be surprised by anything❗️ Keep scrolling to see everything that appears in the correction. All the following screenshots have been taken from the pasqualerossi guide 🇦🇺🤝🇪🇸 ➤ [Repository](https://github.com/pasqualerossi/Born2BeRoot-Guide)

![image](https://user-images.githubusercontent.com/66915274/182514998-71de2c26-c072-4769-b16b-7706b96bcbe5.png)

![image](https://user-images.githubusercontent.com/66915274/182515024-5725b2f1-e687-4dea-a9a2-ef2e7fec7b78.png)

![image](https://user-images.githubusercontent.com/66915274/182515037-6e267905-ae52-4d21-9959-54b4fd7c3db7.png)

![image](https://user-images.githubusercontent.com/66915274/182515074-dfcf5f81-1c14-484d-a0e0-4e57acac7802.png)

![image](https://user-images.githubusercontent.com/66915274/182515110-f766c351-24fd-44ef-a747-e706fd50382c.png)

## 9.1 Evaluation answers 💯

### ▪️ What is a virtual machine❓

It is software that simulates a computer system and can run programs as if it were a real computer. It allows creating multiple simulated environments or dedicated resources from a single physical hardware system.

### ▪️ Why did you choose Debian❓

This is something personal for each one, my opinion: The subject itself explains that it is easier to do it in Debian and if you are looking for documentation/tutorials there are many and they have all been done in Debian.

### ▪️ Basic differences between CentOS and Debian

![182516961-c3e4da77-2db8-4737-a68f-27b033908705 (1) (1)](https://user-images.githubusercontent.com/66915274/182517306-edb92eac-cba4-444a-83f8-9692bac69231.png)

### ▪️ What is the purpose of virtual machines❓

Its goal is to provide a hardware platform and operating system independent runtime environment that hides the details of the underlying platform and allows a program to always run the same way on any platform.

### ▪️ Differences between apt and aptitude ↙️

Aptitude is an improved version of apt. APT is a lower level package manager and aptitude is a high level package manager. Another big difference is the functionality offered by both tools. Aptitude offers better functionality compared to apt-get. Both are capable of providing the necessary means to perform package management. However, if you are looking for a more feature-rich approach, it should be Aptitude.

### ▪️ What is APPArmor❓

It is a Linux kernel security module that allows the system administrator to restrict the capabilities of a program.
