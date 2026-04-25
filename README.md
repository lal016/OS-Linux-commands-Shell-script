# OS-Linux-commands-Shell-scripting
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

<img width="641" height="189" alt="Screenshot 2026-04-25 131424" src="https://github.com/user-attachments/assets/afa58056-7177-4177-a924-7f9495048af5" />



cat < file2

## OUTPUT

<img width="630" height="199" alt="Screenshot 2026-04-25 131432" src="https://github.com/user-attachments/assets/63634747-e32e-42fa-97dc-13fdc367881e" />

# Comparing Files
cmp file1 file2
## OUTPUT

<img width="638" height="76" alt="image" src="https://github.com/user-attachments/assets/a2b3371a-0f43-4ede-ba54-30c53b274d93" />
 
comm file1 file2
 ## OUTPUT

 <img width="647" height="357" alt="image" src="https://github.com/user-attachments/assets/ebdfca93-d653-4f2c-9630-c05d01808975" />


 
diff file1 file2
## OUTPUT

<img width="620" height="275" alt="image" src="https://github.com/user-attachments/assets/bf6275ef-6c57-4516-80d5-31369d0ce30d" />


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

<img width="657" height="124" alt="image" src="https://github.com/user-attachments/assets/94da0855-a703-43f9-b8bb-6a3c5880baba" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="604" height="147" alt="image" src="https://github.com/user-attachments/assets/a2ad89ed-95d2-4633-9334-eff57f361e28" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="695" height="146" alt="image" src="https://github.com/user-attachments/assets/b7f7a4d9-f7e5-4cb9-8cf4-68ddf3ce0700" />


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

<img width="642" height="77" alt="image" src="https://github.com/user-attachments/assets/d390b8cb-83a7-4d19-9ba0-a1aa9e3e277f" />


grep hello newfile 
## OUTPUT

<img width="632" height="89" alt="image" src="https://github.com/user-attachments/assets/91d3fea7-408a-4794-9c1c-bcec1193a7f8" />



grep -v hello newfile 
## OUTPUT

<img width="613" height="80" alt="image" src="https://github.com/user-attachments/assets/06415244-f30c-4336-878c-f1d19b2fb3d5" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="632" height="110" alt="image" src="https://github.com/user-attachments/assets/70580999-c7be-482b-aecc-bf7cdb70eb38" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="606" height="84" alt="image" src="https://github.com/user-attachments/assets/2d8ab7c7-6924-46bd-b74b-3ee6cffa0521" />



grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT

<img width="632" height="111" alt="image" src="https://github.com/user-attachments/assets/f3526646-a11f-4399-aa89-f2b4d9a4b781" />


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

<img width="703" height="106" alt="image" src="https://github.com/user-attachments/assets/5029c0fe-c2a6-4732-ac09-bb86f138e649" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="591" height="97" alt="image" src="https://github.com/user-attachments/assets/b4dca0a6-1c61-4e33-b3c3-3ccf13fb5f1e" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="676" height="106" alt="image" src="https://github.com/user-attachments/assets/8397aaa1-8257-4956-b8c4-bb074d4a0ff7" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="727" height="86" alt="image" src="https://github.com/user-attachments/assets/8e960454-c7d2-4278-bc08-d459e5d5e127" />


egrep '(world$)' newfile 
## OUTPUT

<img width="685" height="99" alt="image" src="https://github.com/user-attachments/assets/208f753a-d10b-4b9e-a901-49bbd700bc7b" />


egrep '(World$)' newfile 
## OUTPUT


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="569" height="79" alt="image" src="https://github.com/user-attachments/assets/445637aa-243d-48f0-8e77-923078481694" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="661" height="81" alt="image" src="https://github.com/user-attachments/assets/eac1f92e-cd04-4eef-9514-381b996e92da" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="581" height="83" alt="image" src="https://github.com/user-attachments/assets/48afac62-b030-43b8-9f7e-0a097861595a" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="635" height="84" alt="image" src="https://github.com/user-attachments/assets/1021e633-c1c9-4857-a376-792085398575" />


egrep l{2} newfile
## OUTPUT

<img width="721" height="105" alt="image" src="https://github.com/user-attachments/assets/e97ad958-17ba-4b54-9453-2a919e2cee66" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="690" height="125" alt="image" src="https://github.com/user-attachments/assets/bdc0d07e-185a-4225-97a7-4cf3ec8f93d6" />


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

<img width="582" height="78" alt="image" src="https://github.com/user-attachments/assets/f0b9e657-45d1-43d3-9cca-b0c3ab9f43ae" />


sed -n -e '$p' file23
## OUTPUT

<img width="707" height="70" alt="image" src="https://github.com/user-attachments/assets/af150c3c-8f6c-4972-9cb4-ab66f4d5e4fa" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="656" height="280" alt="image" src="https://github.com/user-attachments/assets/999b702d-b131-4cf0-ba3c-f2c4da596c31" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="589" height="279" alt="image" src="https://github.com/user-attachments/assets/c0140151-ebe7-4bc5-98a3-57bdcd379bbe" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="702" height="279" alt="image" src="https://github.com/user-attachments/assets/783bdc24-f5b5-4c19-b8eb-028466cd9b26" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="585" height="179" alt="image" src="https://github.com/user-attachments/assets/aedafdfd-2548-427f-aef7-1fa0ef2245a0" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="609" height="130" alt="image" src="https://github.com/user-attachments/assets/dd67f2ea-cc47-4c40-96bd-6e84772cc287" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="607" height="105" alt="image" src="https://github.com/user-attachments/assets/1ea1b43e-ee26-403b-9d21-a0d14e7ea28d" />


seq 10 
## OUTPUT

<img width="732" height="299" alt="image" src="https://github.com/user-attachments/assets/337d0bef-b532-4777-8e5f-3b5d8f1045a0" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="681" height="129" alt="image" src="https://github.com/user-attachments/assets/7b6ca166-3a92-4e34-948b-813c332a2511" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="590" height="134" alt="image" src="https://github.com/user-attachments/assets/bba5d60c-142a-4c70-ab1b-5fadeadda85b" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="632" height="163" alt="image" src="https://github.com/user-attachments/assets/c05ac408-006c-40a9-acef-9c31a8d568c0" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="723" height="129" alt="image" src="https://github.com/user-attachments/assets/f4b45d03-043f-4301-a26d-50f8211b3fb8" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="704" height="137" alt="image" src="https://github.com/user-attachments/assets/e9b5b4f9-ea59-40d3-8226-faedc0fe2cee" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="623" height="136" alt="image" src="https://github.com/user-attachments/assets/de6536b9-5c61-46d6-aaa8-e39b93e6c02a" />


sed -n '2,4{s/$/*/;p}' file23

<img width="676" height="124" alt="image" src="https://github.com/user-attachments/assets/2e4b388b-4099-4a40-af8a-3d3ace3f9c25" />


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

<img width="677" height="172" alt="image" src="https://github.com/user-attachments/assets/fc03221d-b79c-460a-8b93-b64b105c5eed" />


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

<img width="679" height="185" alt="image" src="https://github.com/user-attachments/assets/4018cd69-1e97-4ddd-9c93-cacd2ed8c2f8" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="704" height="273" alt="image" src="https://github.com/user-attachments/assets/8a79d378-4362-4501-b2de-74d75a655668" />

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

<img width="605" height="129" alt="image" src="https://github.com/user-attachments/assets/7e34a819-8f7a-4aa8-8bf1-94622bad39b7" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="652" height="126" alt="image" src="https://github.com/user-attachments/assets/5797870e-b786-4f99-ad04-ae9cd63b5f4f" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="668" height="302" alt="image" src="https://github.com/user-attachments/assets/eff02123-0839-44dd-a934-1302a3d4c4a4" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="701" height="303" alt="image" src="https://github.com/user-attachments/assets/895d5b2a-f9bf-4831-a055-f52a367e7ebb" />


tar -xvf backup.tar
## OUTPUT

<img width="719" height="302" alt="image" src="https://github.com/user-attachments/assets/cc24ff98-0eef-45bc-9429-1e75c195836b" />


gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World'; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="756" height="259" alt="image" src="https://github.com/user-attachments/assets/6c74df8d-da6f-40a9-8a79-d82d56f602aa" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="774" height="459" alt="image" src="https://github.com/user-attachments/assets/8a7ea1b6-3e7f-4093-9735-f72c35b616a6" />


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

<img width="681" height="90" alt="image" src="https://github.com/user-attachments/assets/72bbcd9b-b732-4be3-a3de-b0f2282cc156" />

 
ls file1
## OUTPUT

<img width="668" height="279" alt="image" src="https://github.com/user-attachments/assets/bdedff98-2947-4d03-8568-b0b80a50e3df" />


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

<img width="763" height="158" alt="image" src="https://github.com/user-attachments/assets/475f1d5e-341b-4887-b116-e61cbf8a7cf9" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="743" height="109" alt="image" src="https://github.com/user-attachments/assets/0816f50d-2f76-4d97-9a0c-f8e502de6a2b" />


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

<img width="729" height="158" alt="image" src="https://github.com/user-attachments/assets/f159f99a-697d-43a2-a565-d42d2d1505fc" />


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

<img width="716" height="160" alt="image" src="https://github.com/user-attachments/assets/fd1967c2-779a-4f8f-84f1-12ec3ca4b48b" />


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

<img width="704" height="184" alt="image" src="https://github.com/user-attachments/assets/7f304b49-fd6c-40c6-af91-652147838e03" />


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

<img width="781" height="121" alt="image" src="https://github.com/user-attachments/assets/37a74e2e-9ebf-407c-9a2a-2f3c0bb66b1b" />


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

<img width="735" height="125" alt="image" src="https://github.com/user-attachments/assets/1ce2e36b-7fe8-47dc-8a69-bde9279e35cb" />


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

<img width="704" height="174" alt="image" src="https://github.com/user-attachments/assets/53075a4b-83a1-48eb-87ff-402c43e34476" />

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
 ##output
 
 <img width="676" height="360" alt="image" src="https://github.com/user-attachments/assets/6821cd64-c1e0-431a-99c1-7eb86639592e" />

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
##output

<img width="630" height="156" alt="image" src="https://github.com/user-attachments/assets/269a01d7-2267-4c42-8938-07d117837c63" />

 
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
 ##output

 <img width="725" height="255" alt="image" src="https://github.com/user-attachments/assets/eb73046d-ed2c-4f12-b51d-0647c781983a" />

 
 
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
 ##output

 <img width="692" height="357" alt="image" src="https://github.com/user-attachments/assets/0797b913-1583-4af2-b73b-5eb72f85690b" />

 
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
 ##uotput
 
<img width="628" height="359" alt="image" src="https://github.com/user-attachments/assets/c82bc394-eb25-4364-a706-bebc682488bd" />

 
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
##output

<img width="616" height="437" alt="image" src="https://github.com/user-attachments/assets/3a3d2b14-5194-4b34-ad4f-61d28edc6b00" />

 
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
##output

<img width="694" height="426" alt="image" src="https://github.com/user-attachments/assets/8a84906b-b2a8-4288-9519-dc75496add6e" />

 
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

<img width="657" height="230" alt="image" src="https://github.com/user-attachments/assets/adf356cc-3230-4fd4-b0aa-a90d17ed7f7d" />


cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file"
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

<img width="555" height="183" alt="image" src="https://github.com/user-attachments/assets/4b9dfa62-f896-4905-a2bd-14595768a953" />


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

![Uploading image.png…]()


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


# RESULT:
The Commands are executed successfully.
