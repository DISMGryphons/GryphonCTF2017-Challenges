# FileShare

## Question Text
I created this service where you can leave files for other people to view! I have been getting good reviews.. <br>what do you think about it?

`nc pwn1.chal.gryphonctf.com 17342`

Created by paux

## Setup Guide
1. run `bash start.sh`

## Solution
1.	basically, you just have to exploit that the program can open files.. however, the file name has to be short and there must be a username of at least 3 characters long
2.	another thing is the error is sent directly to you, so you actually know where the py file is
3.	opening the py file using a key suchas,`WyJGUy5weSIsImhlbCJd`,will reveal existance of admin page..
4.	going into admin, by entering the secret key `QQTLBFVLZFCJHABTKQWYYTBLTLNENP` you will notice that you can choose option b and print flag, however, it requires a password
5.	checking the py file again will reveal thet the function check will return the added values of the ascii values of the string fed to it
6.	therefore, after entering `653` you get the flag

### Flag
`GCTF{in53cur3_fi13_tr4n5f3r}`