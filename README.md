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
<img width="623" height="209" alt="image" src="https://github.com/user-attachments/assets/553e3b9a-c76c-4d09-8f8f-c7772e12aa32" />


cat < file2
## OUTPUT
<img width="624" height="245" alt="image" src="https://github.com/user-attachments/assets/049306ca-4254-4c71-9fab-29b122f33f1b" />

# Comparing Files
cmp file1 file2
## OUTPUT
<img width="606" height="97" alt="image" src="https://github.com/user-attachments/assets/7b85bd4f-6f2a-4c8c-a245-30bff3925a78" />

comm file1 file2
 ## OUTPUT
<img width="637" height="198" alt="image" src="https://github.com/user-attachments/assets/0d7efb34-fd67-47aa-872c-e91eea77b3ee" />
 
diff file1 file2
## OUTPUT
<img width="669" height="261" alt="image" src="https://github.com/user-attachments/assets/3e4c8d15-cf43-43b0-842f-60b58ee053ac" />

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

<img width="670" height="368" alt="image" src="https://github.com/user-attachments/assets/f59b703d-a3a1-4f67-90e1-83c5c5ed878f" />

cut -c1-3 file11
## OUTPUT

<img width="612" height="149" alt="image" src="https://github.com/user-attachments/assets/1fc2e88a-732a-463c-a8a4-8ec4e7d07b97" />


cut -d "|" -f 1 file22
## OUTPUT
<img width="586" height="133" alt="image" src="https://github.com/user-attachments/assets/a4a1b99e-8003-4783-8df3-44e791e59305" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="638" height="92" alt="image" src="https://github.com/user-attachments/assets/1d10e82b-7484-4407-8a37-9dc471f4f6b7" /># OS-Linux-commands-Shell-scripting

cat < newfile 
```
Hello world
hello world
^d
```
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
<img width="716" height="449" alt="image" src="https://github.com/user-attachments/assets/eed85629-ad39-4806-b96a-56f76cee9084" />

## OUTPUT
<img width="619" height="94" alt="image" src="https://github.com/user-attachments/assets/edbd0e1c-e733-4904-891e-0837d0f88708" />


grep hello newfile 
## OUTPUT
<img width="605" height="83" alt="image" src="https://github.com/user-attachments/assets/7caaef14-4e85-4c93-8a17-94c95e752dd5" />

grep -v hello newfile 
## OUTPUT
<img width="614" height="121" alt="image" src="https://github.com/user-attachments/assets/f5f8dd3d-3308-4c25-8fc1-db92039c2574" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="611" height="102" alt="image" src="https://github.com/user-attachments/assets/4c1cbddb-c481-4eff-9f9f-557d6b597ee9" />


cat newfile | grep -i -c "hello"
## OUTPUT

<img width="945" height="651" alt="image" src="https://github.com/user-attachments/assets/f35ac140-9000-403d-9878-1d2dc987daa6" />


grep -R ubuntu /etc
## OUTPUT

<img width="640" height="116" alt="image" src="https://github.com/user-attachments/assets/8dbdaff0-5ad0-4cc3-8f1d-aede85d25538" />

grep -w -n world newfile   
## OUTPUT
<img width="656" height="507" alt="image" src="https://github.com/user-attachments/assets/9ca10067-61a6-41cf-8181-e0d0d0bfd5f4" />

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
<img width="607" height="110" alt="image" src="https://github.com/user-attachments/assets/f6144717-5e68-49e0-b3c6-5c5d035bb7db" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="610" height="117" alt="image" src="https://github.com/user-attachments/assets/e957c0b5-e926-42a8-9c70-14b1bfde44f5" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="615" height="89" alt="image" src="https://github.com/user-attachments/assets/d7965cdb-72ac-4121-8d4d-21c820a82f8e" />

egrep '(^hello)' newfile 
## OUTPUT
<img width="610" height="109" alt="image" src="https://github.com/user-attachments/assets/15fca49e-3579-4778-a734-e49abc26162c" />


egrep '(world$)' newfile 
## OUTPUT
<img width="640" height="85" alt="image" src="https://github.com/user-attachments/assets/b0c38574-2e64-4081-a64f-97ab3272fb1f" />


egrep '(World$)' newfile 
## OUTPUT
<img width="650" height="110" alt="image" src="https://github.com/user-attachments/assets/0a240a48-c3af-4605-890c-8e5af3316faa" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="649" height="93" alt="image" src="https://github.com/user-attachments/assets/55662d95-6165-4e58-af81-fb30e66b45f8" />

egrep '[1-9]' newfile 
## OUTPUT
<img width="646" height="85" alt="image" src="https://github.com/user-attachments/assets/70c29606-0402-490a-91e6-a54988be21bd" />

egrep 'Linux.*world' newfile 
## OUTPUT
<img width="650" height="96" alt="image" src="https://github.com/user-attachments/assets/57887857-c7ce-41ce-b548-b20b116f0321" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="641" height="109" alt="image" src="https://github.com/user-attachments/assets/dbf8eb01-b8be-4320-9da0-3adca8b4b89a" />

egrep l{2} newfile
## OUTPUT
<img width="638" height="92" alt="image" src="https://github.com/user-attachments/assets/fec37405-524c-4df2-801e-9f3c4714ed64" />

egrep 's{1,2}' newfile
## OUTPUT 
<img width="646" height="257" alt="image" src="https://github.com/user-attachments/assets/569f77e6-c1e5-4503-ae6a-5363e4b5a1a9" />

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
<img width="653" height="97" alt="image" src="https://github.com/user-attachments/assets/602c7b67-fe67-444b-9c72-9e9fd55b6b46" />

sed -n -e '3p' file23
## OUTPUT

<img width="647" height="97" alt="image" src="https://github.com/user-attachments/assets/cbfc0deb-9502-475f-aca2-d39bb436b4a7" />

sed -n -e '$p' file23
## OUTPUT

<img width="642" height="234" alt="image" src="https://github.com/user-attachments/assets/5d137feb-bd48-48cc-9f69-e02a65176d45" />

sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="653" height="261" alt="image" src="https://github.com/user-attachments/assets/0f34f882-94ad-4454-80b2-528424b18e20" />

sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="650" height="248" alt="image" src="https://github.com/user-attachments/assets/42541810-327e-47ae-aa8f-ef88ed700e83" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="647" height="177" alt="image" src="https://github.com/user-attachments/assets/42d6304a-8086-4cf8-ae63-ba0f6270e92b" />

sed -n -e '1,5p' file23
## OUTPUT
<img width="647" height="158" alt="image" src="https://github.com/user-attachments/assets/8a45e0f9-62d7-448b-af8a-00323bcb15e9" />

sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="643" height="114" alt="image" src="https://github.com/user-attachments/assets/e8d4ba3a-2651-493b-9239-9f4710d5187a" />

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="641" height="318" alt="image" src="https://github.com/user-attachments/assets/06a71163-d2b9-4517-b6a3-1ef16965798b" />

seq 10 
## OUTPUT
<img width="608" height="137" alt="image" src="https://github.com/user-attachments/assets/3c31730a-fd20-410d-a563-3e1e09562871" />

seq 10 | sed -n '4,6p'
## OUTPUT
<img width="600" height="137" alt="image" src="https://github.com/user-attachments/assets/d6389e21-f84b-4601-a967-5f37e13b9c37" />

seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="602" height="162" alt="image" src="https://github.com/user-attachments/assets/ab645de7-4b63-4790-9da7-d49de191972a" />

seq 3 | sed '2a hello'
## OUTPUT
<img width="604" height="141" alt="image" src="https://github.com/user-attachments/assets/96a66083-823f-40f1-8e47-bb6b91ad6de4" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="610" height="145" alt="image" src="https://github.com/user-attachments/assets/18e056f2-c4cd-43a7-873c-d956aac2c933" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="647" height="137" alt="image" src="https://github.com/user-attachments/assets/3dc7ad81-adca-4df7-a7c8-191cdf733ab5" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="639" height="360" alt="image" src="https://github.com/user-attachments/assets/c5cfa557-28f8-4bc7-88cf-4979803e9ad3" />


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
<img width="609" height="371" alt="image" src="https://github.com/user-attachments/assets/c105041d-bee7-40be-9e6d-c4baf533c78a" />

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
<img width="650" height="413" alt="image" src="https://github.com/user-attachments/assets/864dba87-ed8b-468b-9d9e-5b4db042bf11" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Alt text](img/image48.png)
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
<img width="605" height="136" alt="image" src="https://github.com/user-attachments/assets/512fe1d5-9179-4d32-a020-fa9babe6a971" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="614" height="342" alt="image" src="https://github.com/user-attachments/assets/f4fbe4e6-1c76-4456-9c2c-c569da335996" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="621" height="334" alt="image" src="https://github.com/user-attachments/assets/43878e33-352e-48ff-a2d0-8162b4864879" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="614" height="340" alt="image" src="https://github.com/user-attachments/assets/23a4c669-e9fe-48b4-9fc2-b616d5a6b074" />

tar -xvf backup.tar
## OUTPUT
gzip backup.tar
<img width="605" height="99" alt="image" src="https://github.com/user-attachments/assets/3a0f11c2-60c0-43a1-835d-b48f6734434c" />

ls .gz
## OUTPUT
<img width="646" height="63" alt="image" src="https://github.com/user-attachments/assets/814b277e-e65f-4cc9-8ef0-e715bb1c2cc4" />

gunzip backup.tar.gz
## OUTPUT
<img width="610" height="169" alt="image" src="https://github.com/user-attachments/assets/1b5984bc-2d02-4bf3-a947-43ce0a8d8048" />
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="613" height="273" alt="image" src="https://github.com/user-attachments/assets/1f38bf03-e134-435e-b844-9d950795a468" />
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="605" height="687" alt="image" src="https://github.com/user-attachments/assets/9e055061-75bd-460d-9399-324189477f2f" />

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
<img width="645" height="108" alt="image" src="https://github.com/user-attachments/assets/f47a52ba-d0b3-41fa-a1a4-cec6696f41cf" />
 
ls file1
## OUTPUT
<img width="642" height="118" alt="image" src="https://github.com/user-attachments/assets/b5435cbd-e6d5-4b4e-a237-16462764a335" />

echo $?
## OUTPUT 
<img width="645" height="246" alt="image" src="https://github.com/user-attachments/assets/51a38919-a0ce-4f5c-8138-4686418133e6" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
abcd
 <img width="646" height="172" alt="image" src="https://github.com/user-attachments/assets/518d5a8e-1c45-471f-8405-80708d17130e" />

echo $?
 ## OUTPUT
<img width="648" height="285" alt="image" src="https://github.com/user-attachments/assets/98d5f0d7-e3bc-4e87-a2ee-da56f8e6852c" />

 
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
<img width="646" height="170" alt="image" src="https://github.com/user-attachments/assets/7b3d4f42-93a3-4120-a8e9-acf26fb16d2a" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="639" height="82" alt="image" src="https://github.com/user-attachments/assets/136699e1-890f-4bd9-a82b-5fff0444a888" />

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
<img width="649" height="101" alt="image" src="https://github.com/user-attachments/assets/448da455-254c-4f92-bcb8-95080a4019e4" />

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

<img width="615" height="76" alt="image" src="https://github.com/user-attachments/assets/77205100-1f77-4ecc-84d2-01e0e165c8f5" />

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
<img width="648" height="84" alt="image" src="https://github.com/user-attachments/assets/36d9ba08-519c-4148-b972-da7d8f411d96" />

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
<img width="642" height="97" alt="image" src="https://github.com/user-attachments/assets/b363b7b2-2de5-40a1-91fb-b961eaef80ae" />

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
<img width="640" height="372" alt="image" src="https://github.com/user-attachments/assets/8d037413-e56c-4856-87b8-0cef4d3b86b0" />

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
<img width="616" height="459" alt="image" src="https://github.com/user-attachments/assets/fbeb12ce-9925-4458-9225-ca60749d3b7a" />

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
 <img width="607" height="503" alt="image" src="https://github.com/user-attachments/assets/e598c156-b384-451b-87b1-bb6e493f5f0c" />

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
 
 <img width="617" height="374" alt="image" src="https://github.com/user-attachments/assets/0f1e18d7-d190-4594-a936-0b3df4869fae" />

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
 
<img width="646" height="441" alt="image" src="https://github.com/user-attachments/assets/8c057a2d-9d6e-4317-ac2f-2e48485442c1" />
 
 
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
 
<img width="607" height="358" alt="image" src="https://github.com/user-attachments/assets/ba118759-3fdf-4acc-b18c-7324bf304a59" />
 
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
 <img width="613" height="435" alt="image" src="https://github.com/user-attachments/assets/42f307a1-6981-49b0-9bef-c30a0ccc1595" />

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
 <img width="638" height="387" alt="image" src="https://github.com/user-attachments/assets/33ea656f-ca54-40f3-86eb-5d5873d4cf5f" />

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
<img width="606" height="253" alt="image" src="https://github.com/user-attachments/assets/942873f6-a538-4aea-b307-7d4f62e46b38" />
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
<img width="649" height="358" alt="image" src="https://github.com/user-attachments/assets/455b9491-5f1f-47d1-b0ee-67ffdbbac2e2" />

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
<img width="654" height="83" alt="image" src="https://github.com/user-attachments/assets/4a852c8d-011f-4ffc-a7c0-475a460c257e" />

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
<img width="656" height="83" alt="image" src="https://github.com/user-attachments/assets/6852965e-b87f-4912-88c7-f0502257af44" />

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
 <img width="709" height="406" alt="image" src="https://github.com/user-attachments/assets/65345420-7f21-4a09-b189-858e570a46f3" />

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
<img width="652" height="457" alt="image" src="https://github.com/user-attachments/assets/d4eb8bc7-cb31-4cf8-8efd-f5b6e01dae52" />

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
<img width="663" height="260" alt="image" src="https://github.com/user-attachments/assets/2ab61739-817c-4899-98b4-74852830a985" />

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
<img width="611" height="209" alt="image" src="https://github.com/user-attachments/assets/2fb85d89-acd9-435e-ab51-11158197c53d" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="648" height="413" alt="image" src="https://github.com/user-attachments/assets/9e3312c6-cf40-4f07-851c-68a75527fb33" />

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
 <img width="642" height="98" alt="image" src="https://github.com/user-attachments/assets/a61470e8-410b-458a-9f20-3e8f104f2bcf" />

 
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
<img width="655" height="93" alt="image" src="https://github.com/user-attachments/assets/379c5cc9-369b-4f1c-9b61-c87feaeb8e88" />

$ ./argshift.sh 1 2 3
 
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
<img width="659" height="108" alt="image" src="https://github.com/user-attachments/assets/7c6c8e3c-4623-479e-a032-9b1402f3417f" />

$ ./argshift.sh 1 2 3
 
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
 <img width="659" height="108" alt="image" src="https://github.com/user-attachments/assets/7c6c8e3c-4623-479e-a032-9b1402f3417f" />


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
 <img width="664" height="533" alt="image" src="https://github.com/user-attachments/assets/4ed516de-89a6-4d09-942f-ccc02ccb5350" />

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
<img width="627" height="198" alt="image" src="https://github.com/user-attachments/assets/799aed30-09c6-48a1-b46d-948a522f876a" />

# RESULT:
The Commands are executed successfully.
