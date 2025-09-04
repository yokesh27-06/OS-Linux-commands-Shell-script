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
![image](https://github.com/user-attachments/assets/1bb3120c-1238-4920-a7ea-2ec3150d32b4)

cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/af32b9fb-66a8-4474-b17b-d75b9b7926d4)


# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/fe022908-c0d6-4750-a3af-08e4f0928dcb)

comm file1 file2
 ## OUTPUT
![image](https://github.com/user-attachments/assets/4e232ce9-64ca-4bde-9d12-5f98108d8346)

diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/16204101-b55b-4a1c-835f-9bb417dfac40)

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
![image](https://github.com/user-attachments/assets/00c489fe-0939-43f2-b5cf-f571c047250d)

cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/eef254a6-6aa9-4363-986d-af6a4e32503b)

cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/b78a2f7e-6686-4576-a855-78896122233d)

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
![image](https://github.com/user-attachments/assets/2572e17d-61ce-47f1-b253-d351109263a8)

grep hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/1ee46c9f-b7df-4ecf-913c-0aea790402f6)

grep -v hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/6a8b672b-5c17-41d6-840d-ad8af4cb25e7)

cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/d7ff3b27-3730-4c8e-b763-fed7469c7cc2)

cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/31eda373-42d7-403e-93b8-3942a6f8823a)

grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/user-attachments/assets/8dde9438-13f6-4e9c-9ab6-1cd908c51940)

grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/9c65ea2b-f5ad-4a02-88fd-03ed6741c893)

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
![image](https://github.com/user-attachments/assets/c39fda35-314c-4fd4-a263-9803cc1aaaf3)

egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/eed0c643-a36c-44ea-a416-38dcf24bfd94)

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/2407a2da-bc0d-4dd0-8551-76e5a0ea5e05)

egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/44050480-107a-4e3f-8ade-bc1ac9627d95)

egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/93889252-1369-46d2-b8d9-e0e3fd509f7b)

egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/f7e818eb-8ce4-4f31-af9e-3749c6a32b5e)

egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/ad4c2dde-1e04-4590-8929-0b97142b2864)

egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/de1e8d0a-93fd-4d58-9be3-12cc208f55b8)

egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/7a6fdf4f-3c6b-4b40-b396-42e1802f79dc)

egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/8bd1e9ba-19d7-4fff-9ad9-e2bd30746e97)

egrep l{2} newfile
## OUTPUT
![image](https://github.com/user-attachments/assets/40fa2653-6700-4f6a-8f8b-719e562b415f)

egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/1d2b3a5e-6409-474f-8be0-b21192414c1f)

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
![image](https://github.com/user-attachments/assets/14ceb3c8-6905-4c47-a233-72552615d761)

sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/7084c57b-3cbc-4397-a455-4962d6372bfe)

sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/6cf2d482-f1e5-4271-bd04-352fd9c85d62)

sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/cce0ae77-a28f-4322-b316-c54d3eeea180)

sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/2598f70d-bee9-4e49-8bdc-e97761ce74a5)

sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/d70d7409-ec60-4000-ac14-8c6079528a09)

sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/0ed148ba-7d73-46fc-ad9a-c2d87300c415)

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/5432ce87-44fd-42cc-9e5d-7cdfc31739b2)

seq 10 
## OUTPUT
![image](https://github.com/user-attachments/assets/fea8e390-8ae0-4a90-a28e-8d2b2c2c4c76)

seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/user-attachments/assets/5fae905a-ba24-4765-8c93-def41c9264b4)

seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/user-attachments/assets/44312c45-a1f5-4c19-a82c-79e3f0d6d171)

seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/76cd1775-4b5d-485c-a622-3de51dad01b4)

seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/9c38dd7b-fef7-4d2e-8791-caef77ced470)

seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/39431da3-26f8-47ee-98eb-1e818f80398e)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/28da254d-8c2f-4fb9-bb7c-e678a52d4b8f)

sed -n '2,4{s/$/*/;p}' file23
![image](https://github.com/user-attachments/assets/c1640cd5-0eda-4c6b-9eb7-cc4c06a9868e)

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
![image](https://github.com/user-attachments/assets/5db50e6c-391d-4ba8-a38f-93846e4eba4c)

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
![image](https://github.com/user-attachments/assets/de81f100-b407-4b5d-a3c4-e564b3d9b3b2)

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/user-attachments/assets/8ba44fdd-6db2-4a8a-8768-397d16d1fb43)

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
![image](https://github.com/user-attachments/assets/b0f4cf88-27be-4ead-80f7-08225513dd8a)
 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/user-attachments/assets/9b25a0f1-e752-4909-8598-82e5eb880ad4)

#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/user-attachments/assets/7f0aa5d5-785d-4c8e-949c-d1d879c66bef)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/8c56c8fb-bd94-4513-8599-0566c847d152)

tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/92c2b763-f1b8-4ded-90f3-0c1e51d63527)

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
![image](https://github.com/user-attachments/assets/0932e73f-7810-4c97-bd78-241311cf159f)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/user-attachments/assets/7f41c8dc-54c2-46c4-8da7-c5ab566be484)

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
![image](https://github.com/user-attachments/assets/e937d554-8cd1-4050-a573-3eeff4519d77)

ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/2d3b80e3-d9a2-426f-a255-2fcf8b44b9c1)

echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/80397abf-0009-41c7-9d67-c84ec7bae2ae)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![image](https://github.com/user-attachments/assets/e33fdeb7-12a1-46c6-b04a-c008a5119e00)

abcd
 
echo $?
 ## OUTPUT
![image](https://github.com/user-attachments/assets/87d0f7ad-127f-481a-a2c6-95972550bfef)
 
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

chmod 755 strcomp.sh
./strcomp.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/81fd545e-7fcf-42a1-bf9e-6985a6a971d2)

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
![image](https://github.com/user-attachments/assets/91a5283a-ca9d-4bea-8e7e-608d90716214)

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
![image](https://github.com/user-attachments/assets/bcdae15b-82d6-4040-8e87-289b1139f3c6)

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
![image](https://github.com/user-attachments/assets/a17bf600-aa8f-48eb-8e2c-01b27a7a2599)

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
![image](https://github.com/user-attachments/assets/3bcbb9f8-ca91-41f3-9c29-f7a9986f88e0)

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
![image](https://github.com/user-attachments/assets/cddfced1-6aa4-4b6b-82c7-3ebd5633bee1)

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
![image](https://github.com/user-attachments/assets/8f2eca5f-682c-42cd-bae5-b8bef51dfdb4)

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
![image](https://github.com/user-attachments/assets/e944ec20-f4d7-47df-a71b-9f5b69784b13)

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
![image](https://github.com/user-attachments/assets/c1e21c04-c88e-4989-86d5-635b2be6deef)

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
![image](https://github.com/user-attachments/assets/cd8918fe-35f7-49e0-beb8-5b54a2b9682d)

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
![image](https://github.com/user-attachments/assets/fa1001aa-71d9-4f42-b2c2-3c3c07094b0a)

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
![image](https://github.com/user-attachments/assets/783c7ff7-c516-4b2f-bcd6-1f6fa1679cca)
 
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
![image](https://github.com/user-attachments/assets/bf6125a8-7742-4fe5-99f6-ec98b7c75159)

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
 ![image](https://github.com/user-attachments/assets/55705e99-e14a-4115-9265-3ee37c3b1171)

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
![image](https://github.com/user-attachments/assets/845ac51b-7e90-4597-bd37-ac42fa97f1ff)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![image](https://github.com/user-attachments/assets/460cd5d1-8fae-445b-a792-f1825e06ded0)

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
![image](https://github.com/user-attachments/assets/a2c100be-3240-4f81-a102-a50b269f95d6)

 ./funcex.sh 1 2
![image](https://github.com/user-attachments/assets/be1ca228-9ad2-419c-9f81-ddabdda530d1)

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
 ![image](https://github.com/user-attachments/assets/7e9cc1cd-0a57-4764-9a35-1be41549d5ee)

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
 ![image](https://github.com/user-attachments/assets/03faac37-2742-48f2-9a95-e8af707ba948)

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
 ![image](https://github.com/user-attachments/assets/7bc797da-f3c8-4ca9-b4d6-4c3156d11f0e)

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
 ![image](https://github.com/user-attachments/assets/d7b4a7e9-17ee-40ad-841e-76fd7525e916)

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
![image](https://github.com/user-attachments/assets/fb4afc2b-262f-451f-a36e-7158fca52d2b)

# RESULT:
The Commands are executed successfully.
