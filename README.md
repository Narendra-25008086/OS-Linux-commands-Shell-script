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
<img width="615" height="156" alt="image" src="https://github.com/user-attachments/assets/a099ee98-f8f0-4a0d-861d-3385c96e8522" />


cat < file2
## OUTPUT

<img width="533" height="188" alt="image" src="https://github.com/user-attachments/assets/63559aeb-8d3d-401b-9bcc-f25a8520204f" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="563" height="78" alt="image" src="https://github.com/user-attachments/assets/bd23b328-e917-4a10-b8e4-1d845b0a89e1" />

comm file1 file2
 ## OUTPUT
<img width="698" height="303" alt="image" src="https://github.com/user-attachments/assets/3337b128-787a-4dfa-8dfa-2d7830ab2e8f" />

 
diff file1 file2
## OUTPUT
<img width="550" height="277" alt="image" src="https://github.com/user-attachments/assets/75976b5b-9a66-4b82-a462-2b92328474e0" />


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
<img width="595" height="105" alt="image" src="https://github.com/user-attachments/assets/4b628368-a178-4174-aafa-b9eb9776faea" />

cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```
<img width="598" height="132" alt="image" src="https://github.com/user-attachments/assets/968954a5-451e-4e55-a509-752ad0c8093d" />


cut -c1-3 file11
## OUTPUT
<img width="535" height="112" alt="image" src="https://github.com/user-attachments/assets/93bb891e-e83f-4e07-b2b7-5b476ed0a5d5" />

cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 <img width="588" height="110" alt="image" src="https://github.com/user-attachments/assets/9ad6d1dc-9841-410b-a13d-90af447f066f" />

grep Hello newfile 
## OUTPUT
<img width="573" height="90" alt="image" src="https://github.com/user-attachments/assets/f74f5e73-c1e7-4126-93f2-e739f85153ce" />



grep -v hello newfile 
## OUTPUT
<img width="643" height="90" alt="image" src="https://github.com/user-attachments/assets/bf12e057-2103-465d-9479-6a95cbd7cceb" />




cat newfile | grep -i "hello"
## OUTPUT
<img width="812" height="102" alt="image" src="https://github.com/user-attachments/assets/3a67d7f6-4671-46af-82bd-93961e02fd90" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="578" height="95" alt="image" src="https://github.com/user-attachments/assets/2168e4a8-611d-4f1d-8c14-de02ad974c8f" />




grep -R ubuntu /etc
## OUTPUT

<img width="801" height="188" alt="image" src="https://github.com/user-attachments/assets/3ae02563-280a-43ab-9359-4d235fec36ca" />


grep -w -n world newfile   
## OUTPUT

<img width="580" height="107" alt="image" src="https://github.com/user-attachments/assets/f04e3731-3bff-4c54-84b7-6868a87079f0" />

cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
<img width="465" height="180" alt="image" src="https://github.com/user-attachments/assets/db0c3649-3faa-4853-9c7b-e62d0f43e206" />

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
<img width="607" height="117" alt="image" src="https://github.com/user-attachments/assets/3ca7e41b-5f3f-4bce-9370-45a5175c5e14" />

egrep -w 'Hello|hello' newfile 
## OUTPUT

<img width="607" height="117" alt="image" src="https://github.com/user-attachments/assets/d8552309-c01f-4109-8ea2-4b162c434947" />


egrep -w '(H|h)ello' newfile 
## OUTPUT




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="573" height="107" alt="image" src="https://github.com/user-attachments/assets/926585d7-8aad-41bb-8551-ebb66aaeb166" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="518" height="81" alt="image" src="https://github.com/user-attachments/assets/201bccc4-e6dc-4ac1-9f05-d8cd01c4b976" />


egrep '(World$)' newfile 
## OUTPUT
<img width="665" height="102" alt="image" src="https://github.com/user-attachments/assets/0554b019-030d-4953-ad10-44ce53ed6056" />



egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="675" height="125" alt="image" src="https://github.com/user-attachments/assets/7fc0dc0b-2afa-4338-a278-e76a727ab55f" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="520" height="82" alt="image" src="https://github.com/user-attachments/assets/5e4b7790-a335-4c07-93aa-ab0e3b29d623" />



egrep 'Linux.*world' newfile 
## OUTPUT

<img width="577" height="92" alt="image" src="https://github.com/user-attachments/assets/b55996e8-7f54-48c9-ae74-3d6ec340e095" />

egrep 'Linux.*World' newfile 
## OUTPUT


egrep l{2} newfile
## OUTPUT

<img width="495" height="80" alt="image" src="https://github.com/user-attachments/assets/99d7daa3-f385-49c3-b852-33fe970ecfb2" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="535" height="117" alt="image" src="https://github.com/user-attachments/assets/935ac65d-fe97-4298-93de-d2fe87a7fec2" />


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

<img width="640" height="217" alt="image" src="https://github.com/user-attachments/assets/f28f26e8-1ef5-4967-817e-3a28c8909acd" />

sed -n -e '3p' file23
## OUTPUT
<img width="557" height="106" alt="image" src="https://github.com/user-attachments/assets/33bd89d3-1c17-4913-87e7-38f9bf15e672" />



sed -n -e '$p' file23
## OUTPUT
<img width="562" height="88" alt="image" src="https://github.com/user-attachments/assets/8718eb8c-8e39-4a08-94f8-de3e70e1aac8" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="675" height="287" alt="image" src="https://github.com/user-attachments/assets/0e81e155-b4b8-4798-bccf-80672da651b9" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="612" height="281" alt="image" src="https://github.com/user-attachments/assets/cc8c42f3-8a16-4f6f-bba2-8e205dd875c5" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="662" height="286" alt="image" src="https://github.com/user-attachments/assets/42af6a46-b894-4519-9e5c-eba8d38c314f" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="650" height="192" alt="image" src="https://github.com/user-attachments/assets/89e218d6-47d8-4830-a01b-9ffb170229f2" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="652" height="165" alt="image" src="https://github.com/user-attachments/assets/876f5de8-4857-401c-9643-468035fbce41" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="527" height="105" alt="image" src="https://github.com/user-attachments/assets/0b7bcf51-bf2c-423b-b244-640c75284073" />




seq 10 
## OUTPUT
<img width="632" height="313" alt="image" src="https://github.com/user-attachments/assets/36096fbd-82b1-45e3-a1ee-bcf9abb2644c" />



seq 10 | sed -n '4,6p'
## OUTPUT


<img width="520" height="150" alt="image" src="https://github.com/user-attachments/assets/323597fc-fdb1-44c9-9864-024db9ff217e" />

seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="545" height="130" alt="image" src="https://github.com/user-attachments/assets/d681d98e-26c5-42f3-a3f2-9fd9e61d9624" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="505" height="142" alt="image" src="https://github.com/user-attachments/assets/0afe3ddf-157f-4e0e-a4bb-f4b3d221305c" />



seq 10 | sed '2,9c hello'
## OUTPUT
<img width="530" height="132" alt="image" src="https://github.com/user-attachments/assets/765eea0f-a1f3-4c74-bd9b-cadee087d3ee" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


<img width="555" height="147" alt="image" src="https://github.com/user-attachments/assets/78d9545a-7b11-4bae-8869-f19a3b85a0b6" />

sed -n '2,4{s/$/*/;p}' file23
<img width="558" height="130" alt="image" src="https://github.com/user-attachments/assets/1da44cfe-4e0d-461a-ae8b-c3a95787dbf0" />


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
<img width="661" height="182" alt="image" src="https://github.com/user-attachments/assets/94757e1c-7189-48dc-9a12-2dab913a4f3f" />


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```
<img width="660" height="220" alt="image" src="https://github.com/user-attachments/assets/641d7d42-23a7-4d8f-bb8a-3547295c51d1" />

uniq file22
## OUTPUT

<img width="753" height="302" alt="image" src="https://github.com/user-attachments/assets/8a6d0b9c-7763-4655-94e4-9615994d44fe" />


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
<img width="538" height="126" alt="image" src="https://github.com/user-attachments/assets/831ae670-1915-4f4c-972a-d23ea546222a" />

cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


<img width="633" height="127" alt="image" src="https://github.com/user-attachments/assets/ca3ccda6-67bc-4a87-86aa-3af4784c2016" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="622" height="383" alt="image" src="https://github.com/user-attachments/assets/14d1ba81-fdbc-42c4-ab62-19dd288bd776" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="692" height="92" alt="image" src="https://github.com/user-attachments/assets/a65b9e14-d5b4-4c9b-81de-6766b76e5aa1" />

tar -xvf backup.tar
## OUTPUT
<img width="670" height="152" alt="image" src="https://github.com/user-attachments/assets/ccf0365b-299c-41fd-bf90-13fc70d414db" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="1016" height="482" alt="image" src="https://github.com/user-attachments/assets/baa35535-dce4-43b2-830a-f0bd2b90821e" />

 
gunzip backup.tar.gz
## OUTPUT
<img width="935" height="162" alt="image" src="https://github.com/user-attachments/assets/c419bd4c-7bbe-4226-b2cd-58847a990a88" />

 
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

<img width="790" height="487" alt="image" src="https://github.com/user-attachments/assets/b6f4f10c-5123-4f47-8fe7-8eab749e0b77" />

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
<img width="487" height="387" alt="image" src="https://github.com/user-attachments/assets/f54b6329-1655-4132-a222-3064ef5720a6" />

 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT

 <img width="945" height="442" alt="image" src="https://github.com/user-attachments/assets/f7d5adef-b1b8-4360-9ddc-8a7953c2ce25" />

ls file1
## OUTPUT
<img width="675" height="93" alt="image" src="https://github.com/user-attachments/assets/b687ba2b-e30e-47c0-ab51-099912e9ebbc" />

echo $?
## OUTPUT 
<img width="633" height="80" alt="image" src="https://github.com/user-attachments/assets/cb714db2-8349-4363-b369-a0cae5aa25b6" />

./one
bash: ./one: Permission denied
 
 
echo $?
 ## OUTPUT

<img width="782" height="171" alt="image" src="https://github.com/user-attachments/assets/2e7663d8-43ce-4094-9b5e-7d2994c2f034" />

 
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

<img width="828" height="461" alt="image" src="https://github.com/user-attachments/assets/973cdbcc-d436-46a7-8eda-cc6f4232f667" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="712" height="305" alt="image" src="https://github.com/user-attachments/assets/ab0a4963-0ffd-43b4-892a-c3e198296e5d" />



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
<img width="828" height="461" alt="image" src="https://github.com/user-attachments/assets/3a23cdd1-a493-4d22-abe4-8ea4e50a23c5" />


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
<img width="771" height="657" alt="image" src="https://github.com/user-attachments/assets/0ee87705-547c-4d06-8edd-eb00515895c2" />



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
<img width="912" height="690" alt="image" src="https://github.com/user-attachments/assets/aa2e732c-b475-4486-8942-4e2db2a6fbd0" />


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
<img width="597" height="267" alt="image" src="https://github.com/user-attachments/assets/e2032fca-16fd-4a28-9b5c-b9335d5267c5" />

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
<img width="585" height="365" alt="image" src="https://github.com/user-attachments/assets/cf65a2b1-3282-4c88-97d9-45dd27f50475" />


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
<img width="615" height="427" alt="image" src="https://github.com/user-attachments/assets/5566307d-67ad-4a47-acae-f44d1a438a93" />

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
 <img width="445" height="465" alt="image" src="https://github.com/user-attachments/assets/ffe60914-e781-454f-9950-911e19b8cdd2" />

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
 
 
<img width="585" height="365" alt="image" src="https://github.com/user-attachments/assets/da6ea08b-4f75-45e8-a108-06bd670d1d1f" />

 
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
 
 <img width="692" height="350" alt="image" src="https://github.com/user-attachments/assets/b7047da0-9941-4477-8e85-b023e1ebc732" />

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
 <img width="532" height="397" alt="image" src="https://github.com/user-attachments/assets/e8cc8913-4bed-4c75-80d8-56fc79ee737f" />

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
 <img width="550" height="338" alt="image" src="https://github.com/user-attachments/assets/33e58c21-34c2-4d5c-abb5-378b4fc86479" />

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
<img width="603" height="160" alt="image" src="https://github.com/user-attachments/assets/b6be3217-739a-43e5-b1d5-fa0063dde3ef" />

## OUTPUT

<img width="673" height="401" alt="image" src="https://github.com/user-attachments/assets/0f838add-0b72-4233-8248-f59a5359d7d6" />

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
<img width="535" height="325" alt="image" src="https://github.com/user-attachments/assets/3ca6b0fa-247a-4713-8b60-32879664ec6e" />

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

 <img width="635" height="532" alt="image" src="https://github.com/user-attachments/assets/ae12b75a-d087-4296-8230-2b1a055ac7ac" />

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

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
## OUTPUT
<img width="616" height="431" alt="image" src="https://github.com/user-attachments/assets/5a1fed76-e94d-4f63-bbae-dc63320349eb" />


cat forcontinue.sh 
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
 <img width="553" height="170" alt="image" src="https://github.com/user-attachments/assets/5627957c-dd97-40a1-a065-d770f3f755d7" />

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
<img width="616" height="232" alt="image" src="https://github.com/user-attachments/assets/29a4ea7e-3d40-4233-9dc5-acfa001d0ba4" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 
$ ./exread1.sh 
 
## OUTPUT
<img width="541" height="362" alt="image" src="https://github.com/user-attachments/assets/a6ff1859-17d0-441a-9799-7de4ae659da6" />




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
./funcex.sh 
## OUTPUT
 

 <img width="560" height="257" alt="image" src="https://github.com/user-attachments/assets/a1a2c3fa-0622-4d3f-9ea4-778234421889" />


 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3
## OUTPUT
<img width="560" height="257" alt="image" src="https://github.com/user-attachments/assets/f19a84b7-52ed-4145-a042-c218cef0df14" />


 
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
$ ./argshift.sh 1 2 3
## OUTPUT

 <img width="472" height="312" alt="image" src="https://github.com/user-attachments/assets/4e2f7f9d-7868-4f61-8c97-b36e94996995" />

cat argshift2.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
./argshift2.sh 1 2 3
## OUTPUT
 
 
<img width="577" height="582" alt="image" src="https://github.com/user-attachments/assets/527d1eca-74a8-442b-9e06-69a4484c38fc" />


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
<img width="727" height="285" alt="image" src="https://github.com/user-attachments/assets/b2718c99-c188-4908-9dd8-8e3a465aca24" />

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
<img width="620" height="208" alt="image" src="https://github.com/user-attachments/assets/e890f706-f771-4650-8fdc-98441e6b540c" />

awk -f nc.awk data.dat
## OUTPUT 
 <img width="598" height="262" alt="image" src="https://github.com/user-attachments/assets/e402b2f6-4d37-488e-a729-1f9281136f5d" />

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
