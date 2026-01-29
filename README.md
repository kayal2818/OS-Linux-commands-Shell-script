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
<img width="369" height="104" alt="image" src="https://github.com/user-attachments/assets/157c075b-88fd-4b48-b649-341a0a4ef86c" />



cat < file2
## OUTPUT
<img width="398" height="165" alt="image" src="https://github.com/user-attachments/assets/82650e34-b033-4b47-898a-88acd7be3941" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="450" height="51" alt="image" src="https://github.com/user-attachments/assets/623bf892-1179-4bf5-9257-b053058818e3" />

comm file1 file2
 ## OUTPUT
<img width="463" height="243" alt="image" src="https://github.com/user-attachments/assets/aac9a6d7-3870-4f9f-ac9f-f25865c6e726" />

 
diff file1 file2
## OUTPUT
<img width="500" height="311" alt="image" src="https://github.com/user-attachments/assets/af9107df-859b-4572-a79b-564edd9b430e" />


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
<img width="403" height="94" alt="image" src="https://github.com/user-attachments/assets/ad7dc1c2-ee64-44d8-b4bb-9d9501950096" />




cut -d "|" -f 1 file22
## OUTPUT

<img width="453" height="114" alt="image" src="https://github.com/user-attachments/assets/62d46ebc-3098-4f12-8914-f7983020afff" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="471" height="117" alt="image" src="https://github.com/user-attachments/assets/bbe5c1fa-524b-4ae6-98bb-fcd83234e010" />

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

<img width="448" height="56" alt="image" src="https://github.com/user-attachments/assets/0375809d-f9ca-4ed1-a63f-80352d2ff43b" />


grep hello newfile 
## OUTPUT

<img width="454" height="57" alt="image" src="https://github.com/user-attachments/assets/f7a6a857-9576-4ec7-8c62-3ee8741b0757" />



grep -v hello newfile 
## OUTPUT
<img width="461" height="65" alt="image" src="https://github.com/user-attachments/assets/a924eb7d-b52b-47b9-a4a9-41f7d91eca32" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="579" height="87" alt="image" src="https://github.com/user-attachments/assets/3bfb8db9-9385-4eb9-946b-a001c2c533f9" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="602" height="63" alt="image" src="https://github.com/user-attachments/assets/56cc9944-592e-4edc-9815-786ed09d667b" />



grep -R ubuntu /etc
## OUTPUT

<img width="702" height="217" alt="image" src="https://github.com/user-attachments/assets/11a492ad-c760-472e-8cfb-0d9d5f2bc961" />


grep -w -n world newfile   
## OUTPUT

<img width="705" height="85" alt="image" src="https://github.com/user-attachments/assets/66d4c04e-e1ac-4d81-b66c-fad92b1722c0" />

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

<img width="662" height="96" alt="image" src="https://github.com/user-attachments/assets/57281263-bfb3-4e5a-a536-1c1d208a3e72" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="668" height="82" alt="image" src="https://github.com/user-attachments/assets/19b1859c-6996-44c7-ae17-8b24be51d86e" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="668" height="86" alt="image" src="https://github.com/user-attachments/assets/d639295c-f179-41d8-8df6-d5c787d8062a" />



egrep '(^hello)' newfile 
## OUTPUT


<img width="663" height="67" alt="image" src="https://github.com/user-attachments/assets/4960dd79-0c1c-4fa3-aa89-65577320fc24" />

egrep '(world$)' newfile 
## OUTPUT
<img width="667" height="59" alt="image" src="https://github.com/user-attachments/assets/e9b9ab62-d0d8-472e-ab45-9a93061a18ef" />



egrep '(World$)' newfile 
## OUTPUT
<img width="668" height="59" alt="image" src="https://github.com/user-attachments/assets/783598d2-6f6f-42b6-810c-42a1c0e410ff" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="674" height="85" alt="image" src="https://github.com/user-attachments/assets/80a888fb-b6b7-4c91-ab65-708df207de40" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="673" height="58" alt="image" src="https://github.com/user-attachments/assets/6e854b33-0103-44b0-aff9-9f1efeed3963" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="672" height="62" alt="image" src="https://github.com/user-attachments/assets/678b574b-27e6-49d6-b710-e1f2523462fa" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="671" height="60" alt="image" src="https://github.com/user-attachments/assets/202053a2-56a5-4a94-b3a0-9d456fb3323d" />

egrep l{2} newfile
## OUTPUT

<img width="686" height="94" alt="image" src="https://github.com/user-attachments/assets/68895bc8-23ee-4c36-b1b8-678f91803fbb" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="677" height="116" alt="image" src="https://github.com/user-attachments/assets/9df2a868-2d0d-4631-8d74-72540eea9a56" />


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

<img width="472" height="57" alt="image" src="https://github.com/user-attachments/assets/fa86a8cc-039c-481b-bc47-c25832cb1744" />


sed -n -e '$p' file23
## OUTPUT

<img width="530" height="59" alt="image" src="https://github.com/user-attachments/assets/be5bb8a1-1098-4b0b-8bb9-7af41ca08553" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="528" height="246" alt="image" src="https://github.com/user-attachments/assets/10dcf5c8-556a-4386-934e-7b76aa272169" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="574" height="72" alt="image" src="https://github.com/user-attachments/assets/00188930-fcec-44eb-83c0-d6dd07a39728" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="580" height="248" alt="image" src="https://github.com/user-attachments/assets/4f027d15-b79f-41e2-8922-0c401b784da0" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="585" height="107" alt="image" src="https://github.com/user-attachments/assets/cbc86937-16f4-4ee1-8aa6-1210a30d084d" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="583" height="165" alt="image" src="https://github.com/user-attachments/assets/59d43419-7cc9-4b8e-947a-376ab7e1ce76" />


seq 10 
## OUTPUT

<img width="582" height="297" alt="image" src="https://github.com/user-attachments/assets/9a3ae900-2aeb-411d-9959-65b94585290f" />


seq 10 | sed -n '4,6p'
## OUTPUT


<img width="572" height="108" alt="image" src="https://github.com/user-attachments/assets/37bd620a-a063-4229-9b8a-97378a90ce09" />

seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="587" height="109" alt="image" src="https://github.com/user-attachments/assets/1a8879a9-4996-4d0f-ae8d-9ce24973469b" />


seq 3 | sed '2a hello'
## OUTPUT


<img width="596" height="134" alt="image" src="https://github.com/user-attachments/assets/8ecd82c1-ca31-4395-972d-0c5a7e9e0e05" />

seq 2 | sed '2i hello'
## OUTPUT
<img width="592" height="112" alt="image" src="https://github.com/user-attachments/assets/74bff7fe-ce6c-4bb9-b42f-d62f4715ab07" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="594" height="111" alt="image" src="https://github.com/user-attachments/assets/72e8d7f6-1eee-489b-bc41-9a3e7840c25c" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="594" height="110" alt="image" src="https://github.com/user-attachments/assets/305448cd-c1da-4f9b-97a7-07f53ab1c0c0" />


sed -n '2,4{s/$/*/;p}' file23
<img width="600" height="111" alt="image" src="https://github.com/user-attachments/assets/e39386eb-8bc0-4f84-b553-4394b41349b8" />


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
<img width="383" height="164" alt="image" src="https://github.com/user-attachments/assets/44879756-b6fc-434e-91d0-c11f413051dc" />


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

<img width="400" height="159" alt="image" src="https://github.com/user-attachments/assets/34c3e108-487f-4bc6-9ee4-6bf60e5ed09b" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="704" height="244" alt="image" src="https://github.com/user-attachments/assets/76c7121f-1c63-48b2-a797-e37870aada3e" />

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

<img width="713" height="112" alt="image" src="https://github.com/user-attachments/assets/c798b205-2678-44da-a978-d81cb9e40cbd" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


<img width="702" height="113" alt="image" src="https://github.com/user-attachments/assets/9b6620d4-1147-480e-b4c1-2bc1295f936c" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT


<img width="348" height="139" alt="image" src="https://github.com/user-attachments/assets/7937703e-3c68-473c-9ec2-d2224a5ba0b6" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


<img width="348" height="139" alt="image" src="https://github.com/user-attachments/assets/07414efa-a253-42d0-a1e5-dcb5286e6529" />

tar -xvf backup.tar
## OUTPUT

<img width="489" height="166" alt="image" src="https://github.com/user-attachments/assets/d120a2f1-fa73-4644-bb2f-2d2ebd839f4a" />

gzip backup.tar

ls .gz
## OUTPUT

 <img width="795" height="161" alt="image" src="https://github.com/user-attachments/assets/9e472bd4-9095-4b1f-a22f-50b5a360a0ff" />

gunzip backup.tar.gz
## OUTPUT

<img width="1034" height="83" alt="image" src="https://github.com/user-attachments/assets/8a691b2a-e25a-4e01-a818-e057a254b8bf" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT


 <img width="1037" height="124" alt="image" src="https://github.com/user-attachments/assets/a4f5f7f4-0424-4eb1-ab63-ac8af44ba377" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="1034" height="96" alt="image" src="https://github.com/user-attachments/assets/cb5684ea-6344-4e8d-88f9-a80170feece1" />


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

<img width="1038" height="671" alt="image" src="https://github.com/user-attachments/assets/96136d56-e200-4b84-9ed0-f54ca717c062" />

 
ls file1
## OUTPUT

<img width="1055" height="55" alt="image" src="https://github.com/user-attachments/assets/2e9491b7-e338-44c3-a9da-2bbb7647ffb1" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied

 <img width="1029" height="46" alt="image" src="https://github.com/user-attachments/assets/0e69bf50-b358-4026-b0c0-a41d2c0e2d57" />

echo $?
## OUTPUT 

<img width="1028" height="48" alt="image" src="https://github.com/user-attachments/assets/113bc3b3-0f2b-45d9-ab9b-4d38e0847ba2" />
 
abcd
 
echo $?
 ## OUTPUT


<img width="1041" height="235" alt="image" src="https://github.com/user-attachments/assets/3597c19a-4d53-4229-b4f7-9716907ffc64" />

 
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


<img width="1035" height="239" alt="image" src="https://github.com/user-attachments/assets/ef067441-b102-465e-9994-d44ac4b8e3cd" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


<img width="1035" height="94" alt="image" src="https://github.com/user-attachments/assets/f811d09d-9db2-40ac-a59c-255b551e4247" />

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

<img width="1031" height="89" alt="image" src="https://github.com/user-attachments/assets/2125a708-7e16-4d0a-a935-b22763e17c06" />

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

<img width="1050" height="133" alt="image" src="https://github.com/user-attachments/assets/92ea0b48-af55-48a0-8585-4bcacaf69be6" />



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

<img width="1037" height="105" alt="image" src="https://github.com/user-attachments/assets/c5d2a7aa-51fa-4efb-ade4-96b7642043d8" />

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

<img width="1032" height="121" alt="image" src="https://github.com/user-attachments/assets/79b49eb0-f98e-4549-b9c5-5d512851a428" />

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

<img width="1035" height="78" alt="image" src="https://github.com/user-attachments/assets/2db45021-ccf9-4197-b449-dec7cfe95dd4" />


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

<img width="1032" height="76" alt="image" src="https://github.com/user-attachments/assets/69af2be0-e704-42e5-84f0-9960a4f7f8b7" />

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

<img width="1028" height="74" alt="image" src="https://github.com/user-attachments/assets/17a05f21-4b10-43d8-bbfd-b6c774dc533a" />
 
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
 

 <img width="1039" height="290" alt="image" src="https://github.com/user-attachments/assets/10ab4f59-f66e-46bb-8355-a39d2b72d0bc" />

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
 

 <img width="1025" height="164" alt="image" src="https://github.com/user-attachments/assets/fdda8236-e226-4901-97b7-805ae88d8991" />

 
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
 

<img width="1018" height="210" alt="image" src="https://github.com/user-attachments/assets/3c40b8f6-7d2b-42da-8442-ccc58f17e372" />
 
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

 <img width="1031" height="144" alt="image" src="https://github.com/user-attachments/assets/cff9c5d0-8fcf-4c3f-93a0-4759b9258185" />

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

<img width="1029" height="189" alt="image" src="https://github.com/user-attachments/assets/ee108e65-b16e-4aa2-9edc-acac1dfd01af" />

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


<img width="1029" height="333" alt="image" src="https://github.com/user-attachments/assets/19ec0e43-5a00-4c00-b459-db2db18bf578" />

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

<img width="1037" height="166" alt="image" src="https://github.com/user-attachments/assets/475e2bad-d92c-4c05-9aa5-3468bb924352" />

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

<img width="1036" height="170" alt="image" src="https://github.com/user-attachments/assets/0d1294b6-4fdd-4d6a-a5a8-b3e6dbad7210" />

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

<img width="1034" height="337" alt="image" src="https://github.com/user-attachments/assets/8f10a0c5-d265-45dc-a069-b3105a6127e9" />

 
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

<img width="1034" height="121" alt="image" src="https://github.com/user-attachments/assets/e7be04b1-eb5d-455c-b94d-4065ee7bc78c" />

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

<img width="1032" height="153" alt="image" src="https://github.com/user-attachments/assets/96a0180b-faa6-4386-9917-a625f44153e3" />
 
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


<img width="1041" height="98" alt="image" src="https://github.com/user-attachments/assets/f35cd0c1-776a-4905-a60a-e42c584aa8da" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="1039" height="102" alt="image" src="https://github.com/user-attachments/assets/c382a9e6-b0b4-4537-9585-6620c935dd62" />



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

<img width="1034" height="69" alt="image" src="https://github.com/user-attachments/assets/23672fc3-39ed-4fc2-923d-06e4cd8c5352" />

 
 ./funcex.sh 1 2


 <img width="1037" height="50" alt="image" src="https://github.com/user-attachments/assets/70b2404d-e919-48d5-a0f9-49ade8e8121a" />

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

 <img width="1034" height="127" alt="image" src="https://github.com/user-attachments/assets/ac30ceb7-538c-40d9-9f0f-260b32099abc" />

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

 <img width="1037" height="124" alt="image" src="https://github.com/user-attachments/assets/5dbb309a-6c5a-4608-afa3-48b92f35289f" />

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

 <img width="1031" height="384" alt="image" src="https://github.com/user-attachments/assets/a29f96bc-d201-4bac-b346-d8a8f8188521" />

 
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

 <img width="1034" height="343" alt="image" src="https://github.com/user-attachments/assets/573adab9-e92c-428a-b031-dee3177143f1" />

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


<img width="1032" height="357" alt="image" src="https://github.com/user-attachments/assets/a6c9cf46-f521-4108-ad7b-4a2a1c3800fb" />

# RESULT:
The Commands are executed successfully.
