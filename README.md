## OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT

![image](https://github.com/user-attachments/assets/09b41d7a-edd1-4eec-b3cd-0ade2a9fdec1)


cat < file2
## OUTPUT

![image](https://github.com/user-attachments/assets/31ed9fa8-3fa6-4d15-82a4-b02bfca61c17)


# Comparing Files
cmp file1 file2
## OUTPUT

 ![image](https://github.com/user-attachments/assets/0ebebf3d-906b-4775-a072-83cacb58007a)

comm file1 file2
 ## OUTPUT
 
![image](https://github.com/user-attachments/assets/76d75bba-551f-40c5-9fa7-811073a18cdb)

 
diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/9e854078-c5e5-4949-a89e-8a51f33e13b3)


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT
![image](https://github.com/user-attachments/assets/464d7c75-f6e5-4840-ac79-f6bc399dc200)




cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/24abbcbe-11c8-4e98-a91a-dea11c9815a7)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/4479400d-8d4a-4b77-be02-447c27b3121a)


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/4150869d-32b6-48de-bacc-77d5cfc1a21e)



grep hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/70587e31-0128-48d0-b829-0c35c550a9b9)




grep -v hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/86a11a6a-b5a5-4802-ba01-02afdb771168)


cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/507fa04d-8498-40bc-abb0-e0998c3a1687)




cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/30df34d6-cb01-4d80-9d8f-047699a3c69b)



grep -R ubuntu /etc
## OUTPUT

![image](https://github.com/user-attachments/assets/651509d7-e56c-443d-ac04-b187292117a6)


grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/929c23c8-9474-4048-adc5-aec780a2f924)


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/7e7496db-dc62-46eb-bf90-de84967641e6)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/9c3086b0-28d1-44a4-b68f-3a5a89c662c1)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


![image](https://github.com/user-attachments/assets/f369abca-1bf0-4f37-9a37-5f91d683c260)


egrep '(^hello)' newfile 
## OUTPUT


![image](https://github.com/user-attachments/assets/04ae36f8-3aa4-49f4-b82a-0b0acf76f895)


egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/1a58c5c5-a1d5-43fc-acea-5bfbcf775312)


egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/265296b4-61c8-466e-bce1-0f5acf54b0e0)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/d4f6df5d-926e-493c-8c78-1801d8dd3419)



egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/1aa65b76-c09a-4667-859a-07765fccf7a6)



egrep 'Linux.*world' newfile 
## OUTPUT


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/6c2a7422-1b40-47ef-9a9c-78f0c8a4f828)


egrep l{2} newfile
## OUTPUT

![image](https://github.com/user-attachments/assets/8bdac9a7-fc51-4f75-88f5-cfcada545a80)


egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/8ce57297-f5be-4550-9f91-a2c27599022d)


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/5af9aa19-8eca-4106-bca0-d7b4d4728222)



sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/4433674f-790f-4308-a9e6-97bfbe8f3fec)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/ccbc34d6-d00d-4d5b-9ee6-f429ee7a45ba)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/a2e20419-8f56-48a1-a51b-f7fcc7da5610)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/c3cdc0b3-05bb-4c21-845c-a8e2d4fccca6)


sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/7b267750-45bc-4d9e-80cb-919c7be16bc6)



sed -n -e '2,/Joe/p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/01316aa2-ddd1-42cf-893c-f60fd6d70bbd)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/46ab0c26-4ac0-4ccf-863c-2b92f2d7d871)



seq 10 
## OUTPUT
![image](https://github.com/user-attachments/assets/4d75697d-7347-4585-8bfa-d3f17746bd67)



seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/user-attachments/assets/8b5ae114-24b2-441a-97d0-75008c09573f)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/user-attachments/assets/7275d3a5-3665-40db-aee6-01bec481a4fb)



seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/7b98315a-5164-4de5-b8b6-d2d9bf747bd3)



seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/e82d1599-9277-4147-85a5-d4f069a60e1f)


seq 10 | sed '2,9c hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/15e9dbe8-5ea3-4e0b-8071-f60a5cffa27b)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/7f70aa72-a1f2-46fe-9c4c-194ada0848eb)



sed -n '2,4{s/$/*/;p}' file23


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
![image](https://github.com/user-attachments/assets/312bb2c5-50bc-40e5-ba7b-5f3aacff05c4)


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT

![image](https://github.com/user-attachments/assets/dfc6d579-2743-46b0-8b6d-a620d04cd3da)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 
![image](https://github.com/user-attachments/assets/93e1dbb5-54fb-49d9-9a59-5f49c1e1df42)

cat < urllist.txt
```

^d
 ```cat .
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
` ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
![image](https://github.com/user-attachments/assets/feaed513-cf3f-4c5b-9c7d-d7998b93bc9e)


cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image](https://github.com/user-attachments/assets/d30f89b9-e0eb-494e-8f96-34b530953bb0)



#Backup commands
tar -cvf backup.tar 
## OUTPUT
![image](https://github.com/user-attachments/assets/1232070c-1da1-4c1d-90dd-c58743e5d49c)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![image](https://github.com/user-attachments/assets/1f3f4913-6d2a-4c6b-a7b3-3688d85c5b9f)

tar -xvf backupdir/backup.tar
## OUTPUT

![Screenshot 2025-04-23 123657](https://github.com/user-attachments/assets/f27e75d9-b1bb-4ff8-a648-b1fe413f97c1)

gzip backup.tar

ls .gzls
## OUTPUT
 ![image](https://github.com/user-attachments/assets/563dafeb-2ba6-4524-940d-192f289e8004)
![image](https://github.com/user-attachments/assets/9bca3d75-b2bf-439b-8074-d441064b78d2)

gunzip backup.tar.gz
## OUTPUT
![image](https://github.com/user-attachments/assets/3bf05c9b-73d3-485b-a857-4bd59f616e74)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/cbc43b4b-2e4a-4586-9b6d-f0ff7d0a172b)
![image](https://github.com/user-attachments/assets/a681a854-f295-4fa6-be35-f696a84487ec)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![image](https://github.com/user-attachments/assets/355a3a24-554b-41fb-a5ef-77ee9fd4f4e0)


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
![image](https://github.com/user-attachments/assets/308ca26d-922c-4ba6-909e-08a652088709)

![image](https://github.com/user-attachments/assets/3549beac-ecb6-48c6-b60d-91285a285e5d)
 
ls file
## OUTPUT
![image](https://github.com/user-attachments/assets/53cb6f7f-81ea-478a-b707-a6ad66cc8892)

echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/91fa8c03-3251-4c8e-a666-5f0102222d02)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![image](https://github.com/user-attachments/assets/eafee7b1-1431-4252-9cd7-b879c0666554)

abcd
 
echo $?
 ## OUTPUT

![image](https://github.com/user-attachments/assets/0f744cb2-3598-48b6-a81e-b39fb1df2d1b)

 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
## OUTPUT
chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![image](https://github.com/user-attachments/assets/06b5b5eb-345c-4b44-85c2-5d53240533f4)


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/92dd8ad7-dbc5-4ee1-93dc-02e1504323fe)

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT

![image](https://github.com/user-attachments/assets/7bd0a1ad-f6f2-44eb-8785-7da2151f8b1f)



# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
## OUTPUT

![image](https://github.com/user-attachments/assets/135c1f8d-6a2e-4977-a73d-226705dd47b5)

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/a87f763e-0f29-491b-a263-d40b34cb8384)


# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT

![image](https://github.com/user-attachments/assets/0e7bffc1-f339-441e-8bc9-6be7792c6c0e)


# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/02eb2c24-5e9a-4b32-8224-d89a1eed9362)

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh
## OUTPUT 

 ![image](https://github.com/user-attachments/assets/881f86e3-2e0e-4eb2-9df3-eb2869b1676f)

cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh

 ![image](https://github.com/user-attachments/assets/a68fc75c-e164-4f71-85a0-62b5501ea0c3)

 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
![image](https://github.com/user-attachments/assets/da9adf58-b76b-4230-81a5-ae19eaeffa4c)

 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 ![image](https://github.com/user-attachments/assets/8170f796-b2be-4a6e-a85d-b744da80f215)

 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh

## OUTPUT
 ![image](https://github.com/user-attachments/assets/f7df1ee4-0708-429e-9f06-d116c1671203)

cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
## OUTPUT
 ![image](https://github.com/user-attachments/assets/b20c134f-6e8f-4572-b44c-08d48ae0f2d2)

cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 

## OUTPUT

 ![image](https://github.com/user-attachments/assets/6baa875f-b6ec-4fde-8d45-98776e928e8c)

cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
![image](https://github.com/user-attachments/assets/4c27ab6c-f906-411b-acb9-444ad6203a64)

cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT

![image](https://github.com/user-attachments/assets/4fbf6517-6790-4aa0-9082-f64b2eb0aa82)


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/59830f13-2894-4070-8ceb-49302856a0d3)

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/9ebe58c6-5618-48e2-ab86-f585fbd8bb78)

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT
![image](https://github.com/user-attachments/assets/2ec8ec08-3db7-4315-8701-25df606472b5)


$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 ![image](https://github.com/user-attachments/assets/b86813b8-f850-4e70-9906-73bfbf1897d5)

cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/29e77150-b028-4800-a114-c7721bb99488)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![image](https://github.com/user-attachments/assets/3236784c-88c9-4b8d-bf20-4f72371b4c64)



$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 
 ./funcex.sh 1 2
![image](https://github.com/user-attachments/assets/92e56c69-80be-4e67-a731-11d84d670cf2)

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
 ![image](https://github.com/user-attachments/assets/6829e622-0140-4a35-98eb-3d3d94647c27)

 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 ![image](https://github.com/user-attachments/assets/09fbdb61-929b-4237-b90f-ed2b8be9cae8)

cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
![image](https://github.com/user-attachments/assets/d3cad86c-1c79-4355-8aa9-61188cd6b5b9)
 
 
 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 ![image](https://github.com/user-attachments/assets/54e9282f-4c0a-4c10-b4ae-386734d7fe39)

cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
![image](https://github.com/user-attachments/assets/7445608c-f43e-416b-a7e2-1bf128170e2c)


# RESULT:
The Commands are executed successfully.
