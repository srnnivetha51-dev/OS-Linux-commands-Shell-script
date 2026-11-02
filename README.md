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

<img width="481" height="123" alt="image" src="https://github.com/user-attachments/assets/d2cb4494-4ee8-4cbd-9801-4cf4582089b7" />


cat < file2
## OUTPUT

<img width="590" height="168" alt="image" src="https://github.com/user-attachments/assets/cd306a05-7c8e-4a26-b9c4-93042739a4bd" />

# Comparing Files
cmp file1 file2
## OUTPUT
<img width="372" height="43" alt="image" src="https://github.com/user-attachments/assets/885737c3-b11d-4d0a-a418-a4ab1be2f285" />
 
comm file1 file2
 ## OUTPUT
<img width="447" height="317" alt="image" src="https://github.com/user-attachments/assets/3c457c10-6786-4efe-9088-b1645ffffbc5" />

 
diff file1 file2
## OUTPUT
<img width="430" height="280" alt="image" src="https://github.com/user-attachments/assets/10abea83-b1de-43fe-8447-498144274766" />


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

<img width="547" height="442" alt="image" src="https://github.com/user-attachments/assets/dff277a7-cd3b-4a7d-960b-e6abc8c72dcf" />



cut -d "|" -f 1 file22
## OUTPUT



cut -d "|" -f 2 file22
## OUTPUT


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

<img width="453" height="36" alt="image" src="https://github.com/user-attachments/assets/7aefec96-4686-4179-b3a9-e9cf1131c703" />


grep hello newfile 
## OUTPUT

<img width="432" height="37" alt="image" src="https://github.com/user-attachments/assets/15dff7fd-5cca-4ff5-8976-6f933bb8b175" />



grep -v hello newfile 
## OUTPUT

<img width="470" height="40" alt="image" src="https://github.com/user-attachments/assets/b2298df1-aedb-4bae-b56b-84085feb53c4" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="577" height="92" alt="image" src="https://github.com/user-attachments/assets/d0ebfca1-b4bf-4d9f-8542-4600ad3e43a1" />



cat newfile | grep -i -c "hello"
## OUTPUT



<img width="576" height="33" alt="image" src="https://github.com/user-attachments/assets/fe5c55ee-320c-40fb-9265-a51272837918" />

grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
<img width="940" height="36" alt="image" src="https://github.com/user-attachments/assets/f7fe1ad0-13a2-4641-91e8-b4c6e79f0f95" />


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

<img width="518" height="56" alt="image" src="https://github.com/user-attachments/assets/5ef63a9c-6ae0-44dc-bade-aea97bd264e4" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="513" height="52" alt="image" src="https://github.com/user-attachments/assets/7a64a6fb-8953-4ca7-92b0-a077b9ae08fc" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="557" height="52" alt="image" src="https://github.com/user-attachments/assets/fb5aa239-9e73-4cfe-bf8d-4fa0a2ad0843" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="480" height="40" alt="image" src="https://github.com/user-attachments/assets/0bea3233-9d31-4f1d-b2d7-207119971853" />


egrep '(world$)' newfile 
## OUTPUT



egrep '(World$)' newfile 
## OUTPUT
<img width="542" height="48" alt="image" src="https://github.com/user-attachments/assets/c34d8b1f-39e6-4d99-bad0-77d94a7b4d85" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="357" height="57" alt="image" src="https://github.com/user-attachments/assets/77d9ba6a-d17f-42ab-9d8f-323796052782" />



egrep '[1-9]' newfile 
## OUTPUT


<img width="452" height="40" alt="image" src="https://github.com/user-attachments/assets/2f3dcaae-52bd-4055-b6f0-0f3fa94ff4d7" />

egrep 'Linux.*world' newfile 
## OUTPUT

<img width="532" height="52" alt="image" src="https://github.com/user-attachments/assets/aae2aaee-2238-4a4e-9704-d188e4a8b88c" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="496" height="45" alt="image" src="https://github.com/user-attachments/assets/62a76b3e-dead-4513-b101-db4035058239" />


egrep l{2} newfile
## OUTPUT

<img width="940" height="35" alt="image" src="https://github.com/user-attachments/assets/4b40e596-0afa-4386-89cd-027ecdceb919" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="940" height="46" alt="image" src="https://github.com/user-attachments/assets/83c8d19d-ad79-4520-be56-ece541ff7b5e" />

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

<img width="481" height="42" alt="image" src="https://github.com/user-attachments/assets/24f8936a-625a-4004-87ec-95d71ca71672" />


sed -n -e '$p' file23
## OUTPUT



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="507" height="187" alt="image" src="https://github.com/user-attachments/assets/45379320-8d00-4f9f-a7e5-6c471df6de20" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="515" height="187" alt="image" src="https://github.com/user-attachments/assets/9ae866d6-024e-456d-80e8-8c13438931a3" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="595" height="187" alt="image" src="https://github.com/user-attachments/assets/66720c76-0e0e-4b86-8abe-eb9b9ac90e95" />


sed -n -e '1,5p' file23
## OUTPUT
<img width="505" height="127" alt="image" src="https://github.com/user-attachments/assets/962f3234-f293-453c-a0a8-f59b53c05d48" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="577" height="76" alt="image" src="https://github.com/user-attachments/assets/171cae30-7918-40c4-935a-cbe39661bf69" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="431" height="217" alt="image" src="https://github.com/user-attachments/assets/3fda7cee-503b-4d1d-91fb-be2e7341bd68" />


seq 10 
## OUTPUT

<img width="482" height="70" alt="image" src="https://github.com/user-attachments/assets/084d2e8b-5ed1-4fff-ba33-46e5dc87a46f" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="512" height="76" alt="image" src="https://github.com/user-attachments/assets/48f0ff7e-9784-4ed3-8501-8ae9caa4a963" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="512" height="76" alt="image" src="https://github.com/user-attachments/assets/cd6c962e-d026-409c-bfcc-2d6fb37a188f" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="526" height="102" alt="image" src="https://github.com/user-attachments/assets/db908386-20ee-496f-bc4a-42b136d391ed" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="485" height="78" alt="image" src="https://github.com/user-attachments/assets/ea5344f0-0bd3-4a29-adef-850a8dfe80f4" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="487" height="78" alt="image" src="https://github.com/user-attachments/assets/fcb62c6a-6ed6-4a1d-844d-937d68cc91e1" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT



sed -n '2,4{s/$/*/;p}' file23
<img width="551" height="86" alt="image" src="https://github.com/user-attachments/assets/013d6175-d6ae-434a-bdea-4c9aaf6060a0" />


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
<img width="645" height="173" alt="image" src="https://github.com/user-attachments/assets/84ef24d5-46fc-40bf-a30c-77e595578b37" />

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

<img width="542" height="77" alt="image" src="https://github.com/user-attachments/assets/c183f8a4-1043-4ebf-a989-eb4de4758b2e" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="655" height="73" alt="image" src="https://github.com/user-attachments/assets/a77b0107-e1fb-416e-ada3-1b7c92892e99" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
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

 <img width="713" height="42" alt="image" src="https://github.com/user-attachments/assets/4de37bad-83ab-4a1e-af21-2571d41b4b9e" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="482" height="176" alt="image" src="https://github.com/user-attachments/assets/53d8cf6c-cd31-46ef-93a8-0976b9f0640a" />

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

 <img width="940" height="25" alt="image" src="https://github.com/user-attachments/assets/cf4359a7-dbdb-436b-ac57-5b89ac467c11" />

ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 <img width="940" height="25" alt="image" src="https://github.com/user-attachments/assets/332430ed-e2b2-4da0-a9ec-a62d5a658383" />

echo $?
## OUTPUT 
 
abcd
 <img width="940" height="25" alt="image" src="https://github.com/user-attachments/assets/9fde0596-0eb4-49f9-bb83-17e18d22a51c" />

echo $?
 ## OUTPUT
<img width="940" height="112" alt="image" src="https://github.com/user-attachments/assets/46d3e53e-d8e6-4e7f-95d7-d0855a43343b" />


 
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

<img width="940" height="117" alt="image" src="https://github.com/user-attachments/assets/d5e7fb12-3cb4-4cda-b670-1487e0264b73" />

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
<img width="496" height="245" alt="image" src="https://github.com/user-attachments/assets/f9067cae-1751-45b3-8fd1-e036dff98bb0" />


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
<img width="492" height="310" alt="image" src="https://github.com/user-attachments/assets/5882b1a2-ad21-41d3-ac15-3a96c57127a2" />

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
<img width="542" height="223" alt="image" src="https://github.com/user-attachments/assets/87e5a4dd-5bd3-4e79-8133-7714eb5c0e04" />

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
<img width="761" height="276" alt="image" src="https://github.com/user-attachments/assets/0f16cbaa-f514-45a0-b1c6-6b0a641585f4" />

 
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

<img width="877" height="172" alt="image" src="https://github.com/user-attachments/assets/31b2f56d-dbe2-4ba8-99c2-9e5d74feda25" />

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
<img width="613" height="391" alt="image" src="https://github.com/user-attachments/assets/119a41fb-4694-4dd1-b6c8-0be74f2997d2" />

 
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
 <img width="940" height="148" alt="image" src="https://github.com/user-attachments/assets/e7cf7ff2-41b2-46f7-9cfe-3a5d47cc5ad9" />

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
 
 <img width="940" height="148" alt="image" src="https://github.com/user-attachments/assets/1fc9af78-c162-46bb-bec0-b0dd085aec42" />

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
 <img width="531" height="267" alt="image" src="https://github.com/user-attachments/assets/7ae21491-bc8b-4bc3-9b63-e0f1ddd604a8" />

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
<img width="738" height="501" alt="image" src="https://github.com/user-attachments/assets/e0aa4304-8900-4dae-a1c1-c0a0f77cb5c2" />


# RESULT:
The Commands are executed successfully.
