![Screenshot from 2024-02-26 19-13-21](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/c1e559f9-2f67-43f2-95d6-fb9e68ae3677)# OS-Linux-commands-Shell-scripting
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
![Screenshot from 2024-02-26 17-57-58](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/9a7fa92c-8402-46b8-b656-239d06beb3b1)


cat < file2
## OUTPUT
![Screenshot from 2024-02-26 17-58-14](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/594de9b5-c8f5-48f1-bcd2-486e46f79341)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![Screenshot from 2024-02-26 20-30-46](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/7058f85c-bed5-4f31-ae17-89a9d443eab0)

comm file1 file2
 ## OUTPUT
![Screenshot from 2024-02-26 18-51-18](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/3631d93b-190d-436c-87de-f12d3f7fda25)

 
diff file1 file2
## OUTPUT
![Screenshot from 2024-02-26 18-51-30](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/3cf90e90-10f3-4612-84e4-f5f678b703b0)


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

![Screenshot from 2024-02-26 18-08-42](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/3bed0ade-b8a6-424c-9993-235c12ddb1aa)



cut -d "|" -f 1 file22
## OUTPUT
![Screenshot from 2024-02-26 18-08-59](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/1bc068c4-d930-49b5-8672-1a4a7275c9b3)



cut -d "|" -f 2 file22
## OUTPUT
![Screenshot from 2024-02-26 19-01-36](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/3acbad83-46c5-4b21-a0f1-91ee5d9ae290)


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
![Screenshot from 2024-02-26 19-03-33](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/642c3cdc-9371-4b95-b738-9870688a57b6)



grep hello newfile 
## OUTPUT

![Screenshot from 2024-02-26 19-03-47](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/200035fa-9c4b-4fba-a494-89cc0487bda7)



grep -v hello newfile 
## OUTPUT

![Screenshot from 2024-02-26 19-13-21](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/e59cc025-e6e0-42d0-8d1f-65b9f3b7fcc7)


cat newfile | grep -i "hello"
## OUTPUT
![Screenshot from 2024-02-26 20-36-27](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/4a0502a1-2a7e-4977-86bf-0cc6a92724c3)




cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot from 2024-02-26 20-36-41](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/524a0318-7feb-4d16-a643-ac85142d763b)



grep -R ubuntu /etc
## OUTPUT




![Screenshot from 2024-02-26 19-26-26](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/808f36df-96b8-48f0-b4ed-e8c3197c5501)

![Screenshot from 2024-02-26 19-27-14](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/1d2900b9-b66b-45d8-b193-d41678ff13f4)
grep -w -n world newfile   
## OUTPUT:
![Screenshot from 2024-02-26 20-38-38](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/70135a12-c7cb-49e4-b1ae-89bb979937de)


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
![Screenshot from 2024-02-26 20-39-31](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/5cf2986e-246b-4719-b2c0-86c70dc485b3)




egrep -w '(H|h)ello' newfile 
## OUTPUT

![Screenshot from 2024-02-26 20-39-49](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/3d17e4c2-ea93-48ec-adb9-482575dfcac1)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![Screenshot from 2024-02-26 20-42-55](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/d11ed441-bb45-4577-8a4f-3feb3ce9096a)



egrep '(^hello)' newfile 
## OUTPUT:
![Screenshot from 2024-02-26 20-43-27](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/7c197f3d-4c6f-4284-9614-fb4d182335bf)


egrep '(world$)' newfile 
## OUTPUT
![Screenshot from 2024-02-26 20-43-27](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/01f2d684-bed5-4516-84ff-16846742d3f9)



egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2024-02-26 20-43-39](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/479683e8-9a42-40d5-acac-0cdb10699cfc)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot from 2024-02-26 20-44-03](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/b524ef37-e602-4f9c-98b1-73ce507a2d12)



egrep '[1-9]' newfile 
## OUTPUT
![Screenshot from 2024-02-26 20-46-28](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/9da906a1-919b-486a-9266-654b00556201)



egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2024-02-26 20-46-42](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/1a791c92-4bc2-4df6-92c9-3d4195235e90)



egrep 'Linux.*World' newfile 
## OUTPUT:

![Screenshot from 2024-02-26 20-47-08](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/81e387a4-de16-47ab-a34d-25447d8888cb)


egrep l{2} newfile
## OUTPUT
++++++++++![Screenshot from 2024-02-28 14-03-39](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/4106f4bc-6e7d-4aea-9849-67aab37c998d)



egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot from 2024-02-26 20-47-22](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/b197b85f-a455-42e1-9fed-3ed94d7cf881)


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

![Screenshot from 2024-02-26 20-48-24](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/224d5b87-ac05-40df-9825-b1c50cb60c1d)


sed -n -e '$p' file23
## OUTPUT



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2024-02-26 20-47-32](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/b4c8923e-4655-42b0-8acc-c8573cae0710)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot from 2024-02-26 20-48-14](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/781e3b84-e5ec-4dd4-8716-10dddcb65371)



sed -n -e '1,5p' file23
## OUTPUT



sed -n -e '2,/Joe/p' file23
## OUTPUT




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT



seq 10 
## OUTPUT



seq 10 | sed -n '4,6p'
## OUTPUT



seq 10 | sed -n '2,~4p'
## OUTPUT



seq 3 | sed '2a hello'
## OUTPUT



seq 2 | sed '2i hello'
## OUTPUT


seq 10 | sed '2,9c hello'
## OUTPUT


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT



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



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


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

 
ls file1
## OUTPUT
![Screenshot from 2024-02-27 23-23-12](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/1278d500-a56d-45e3-aecd-21aa0d0a7043)

echo $?
## OUTPUT 

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
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
##OUTPUT
![Screenshot from 2024-02-28 09-12-40](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/b538cfc6-e024-4bee-949d-190d131db7fc)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![Screenshot from 2024-02-28 09-12-24](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/ccb158fa-a56c-4170-a3c9-a4e6c6fff5dc)



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
![Screenshot from 2024-02-28 09-12-13](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/c05c5251-324d-4a24-a51c-3ba03dba5b25)


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
![Screenshot from 2024-02-28 09-11-58](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/6f1248e1-3587-49b9-99fe-20a5928f8dcf)



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
##OUTPUT
![Screenshot from 2024-02-28 09-11-45](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/178b42c5-aa10-46a2-9a2f-db996e6cf958)

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
##OUTPUT

 ![Screenshot from 2024-02-28 09-11-34](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/9ba4c43b-43aa-45c3-a40a-693265de2fe5)



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
![Screenshot from 2024-02-28 09-11-20](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/65e249d5-ecb3-4972-b746-467dbf062008)


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
![Screenshot from 2024-02-28 09-10-38](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/82ba76bb-5810-4052-b9a3-ce25a374b8ad)

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
 ![Screenshot from 2024-02-28 09-10-24](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/041379c2-8da8-41e0-b658-d3e457cd950d)

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
 ![Screenshot from 2024-02-28 09-10-09](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/36e9db60-0134-4280-a2c1-a57335ec2f0e)

 
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
 
 ![Screenshot from 2024-02-28 09-09-54](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/d6d79a42-da5a-40dc-b553-08879fea431c)

 
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
 ![Screenshot from 2024-02-28 09-09-41](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/be63b10a-f544-4cf3-aab7-4e9d8f4be8e5)

 
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
 ![Screenshot from 2024-02-28 09-09-30](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/a0450c1e-c374-40ea-a823-629d21fcf956)

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
 ![Screenshot from 2024-02-28 09-09-20](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/018d6ba1-dbf3-4e81-9cef-1c9e5314a563)

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
![Screenshot from 2024-02-28 09-54-14](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/a144e84d-240e-40d3-bfc8-63140a90dbec)


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
## OUTPUT:
![Screenshot from 2024-02-28 09-08-52](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/08bac301-5132-433b-ab50-960eaae438cb)


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
![Screenshot from 2024-02-28 09-08-35](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/a72a580c-924b-4366-bd93-7a8355c994a9)


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
![Screenshot from 2024-02-28 09-08-24](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/8663bff6-26de-4004-be52-252ddc1aad86)

 
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

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh
![Screenshot from 2024-02-28 09-08-13](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/d517455a-0c77-4689-9d8a-98b2ebe90276)


 
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


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



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
![Screenshot from 2024-02-28 09-02-11](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/15850ec8-c851-4d51-8aca-1feee524f2ac)

 
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
 ![Screenshot from 2024-02-28 08-59-41](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/8c411bfa-f79e-4bbf-960f-36f65f97d429)

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
![Screenshot from 2024-02-28 08-59-41](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/ccd8553c-15d7-47fc-9912-b553ac08b50e)

 
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
 ![Screenshot from 2024-02-28 08-53-50](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/47670da0-402d-47c8-b258-95423685bf85)

 
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
 ![Screenshot from 2024-02-28 08-46-56](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/a8699dd8-820b-458f-bf84-82b6a3d3e356)

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
![Screenshot from 2024-02-28 08-44-48](https://github.com/Kishore23008675/OS-Linux-commands-Shell-script/assets/144979375/75423528-fe48-48b4-b1b5-fc31440f0d41)


# RESULT:
The Commands are executed successfully.
