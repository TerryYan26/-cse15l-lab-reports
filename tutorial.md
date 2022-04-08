# Lab Report

## Installing VScode
  1. Go to google searching "VSCode" or [Click Here](https://code.visualstudio.com/).
  2. Select your platforms(Window , MacOs)
  ![image](https://user-images.githubusercontent.com/103209100/162337138-daccb456-a0b8-4fee-9f4e-355e48a21239.png)
  3. Download your platforms version and install it.
  4. When you done for the install. Your VsCode interface like that
  ![image](https://user-images.githubusercontent.com/103209100/162337349-4fd9422e-30b4-4856-b9dc-6ee493b3f346.png)
## Remotely Connecting
1. Go to install the OpenSSH. [Click Here](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse) to install OpenSSH
2. Getting your CSE15L account from:[Here](https://sdacs.ucsd.edu/~icc/index.php).
3. Then, Going to the VsCode and  open a terminal in VSCode (Ctrl + `, or use the Terminal → New
Terminal menu option). Your command will look like this, but with the **zz** replaced by the
letters in your course-specific account.
4. enter the command in your VScode : $ ssh cs15lsp22zz@ieng6.ucsd.edu
5. If you are first time to login, here is the message you will see :
   $ ssh cs15lsp22zz@ieng6.ucsd.edu
" The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established."
Are you sure you want to continue connecting (yes/no/[fingerprint])?
6. Type "yes" and enter.
7. Here is the message you will see:

![image](https://user-images.githubusercontent.com/103209100/162338896-a98c3454-ad03-4f1c-a6e5-04dd922807f5.png)

## Trying Some Commands
1. Here is some Commands for testing.
2. Pwd and ls
3. Pwd is a command that shows the current directory.
  Here is picture for enter command Pwd :![image](https://user-images.githubusercontent.com/103209100/162340622-b97f840c-7b98-4a67-a6e4-9d337ef958b9.png)
 
4. ls is a command that shows a directory listing.
  Here is a picture for enter a command ls:
  ![image](https://user-images.githubusercontent.com/103209100/162340573-e9c208fb-69f4-4e8c-91a1-6a43a4233eee.png)


## Moving Files with scp
1. When we want to move file form local computer to remote computer, we have to use command call "scp"
2. Make sure we are not login the remote compurter.(If we are in the remote computer, use command "exit". 
3. Then you will logout it and get the message: Connection to ieng6.ucsd.edu closed.
4. Enter you command in your VScode terminal : scp <file name> cs15lsp22<zz>@ieng6.ucsd.edu:~/
5. Then login your account: ssh cs15lsp22<zz>@ieng6.ucsd.edu and use ls 
6. You can see your uploading file.
   Here am I using WhereAMI.java be the example and you will see the result below:
  ![image](https://user-images.githubusercontent.com/103209100/162341494-100ce076-1d66-4971-b3f3-5d9cad45e8d4.png)

## Setting an SSH Key

## Optimizing Remote Running


