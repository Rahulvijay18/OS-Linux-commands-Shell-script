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
![image](https://github.com/user-attachments/assets/72ae28a5-a06b-4f38-9f3b-7b1f76a0ee95)

## OUTPUT



cat < file2
![image](https://github.com/user-attachments/assets/f5f42459-1eb8-4335-8ca2-3c3d011d2af6)

## OUTPUT


# Comparing Files
### cmp file1 file2
![image](https://github.com/user-attachments/assets/0eadf332-1327-45f4-8bef-e48a4f713c6c)

## OUTPUT
 
### comm file1 file2
![image](https://github.com/user-attachments/assets/3ec367ec-7b7d-4cbd-938e-8245b22b1ffb)


 ## OUTPUT

 
diff file1 file2
![image](https://github.com/user-attachments/assets/f5d1a544-7b90-42c1-bbac-7c0c23a89c2c)


## OUTPUT


### Filters

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
![image](https://github.com/user-attachments/assets/3d939e23-8c9e-4878-877f-f5d223bf17e1)

## OUTPUT




cut -d "|" -f 1 file22
![image](https://github.com/user-attachments/assets/b619f49b-0310-4192-9654-e0aa530af48a)

## OUTPUT



cut -d "|" -f 2 file22
![image](https://github.com/user-attachments/assets/9c0bf02a-bf27-4fc9-a220-24fc827e836f)



## OUTPUT


cat > newfile
```
Hello world
hello world
^d
````
 
cat < newfile 
![image](https://github.com/user-attachments/assets/7d55a35e-a293-42aa-b527-8ff5fc7bc9a5)

 
grep Hello newfile 
![image](https://github.com/user-attachments/assets/2ebb7f73-cb48-4921-aebd-0bc293f888dc)

## OUTPUT



grep hello newfile 
![image](https://github.com/user-attachments/assets/c1597c7b-30cf-484f-b69b-85d1ea85917f)

## OUTPUT




grep -v hello newfile 
![image](https://github.com/user-attachments/assets/ee6c4c90-59b3-4b5d-a076-7cb628b156a1)

## OUTPUT



cat newfile | grep -i "hello"
![image](https://github.com/user-attachments/assets/f67cfe13-b8fc-4a55-9d5f-b3ee58ef10cf)

## OUTPUT




cat newfile | grep -i -c "hello"
![image](https://github.com/user-attachments/assets/1c8fea74-f523-4949-986b-f1e5a9b67167)

## OUTPUT




grep -R ubuntu /etc
![image](https://github.com/user-attachments/assets/bf74b4c3-e73d-4296-b870-3cc83650831f)


## OUTPUT



grep -w -n world newfile   
![image](https://github.com/user-attachments/assets/344eeb70-f916-4047-929d-ca13a55b182b)

## OUTPUT




cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
 cat < newfile 
![image](https://github.com/user-attachments/assets/909aa81f-dd04-4cd4-819f-4ba767e3be81)


egrep -w 'Hello|hello' newfile 
![image](https://github.com/user-attachments/assets/3cf4be0f-0399-4265-9b09-c10a725510a7)

## OUTPUT



egrep -w '(H|h)ello' newfile 
![image](https://github.com/user-attachments/assets/7b0c813f-e384-49d0-9a5a-4fac28f51b23)

## OUTPUT



egrep -w '(H|h)ell[a-z]' newfile 
![image](https://github.com/user-attachments/assets/659d85b9-42ff-40a9-8a6c-8781c23295a7)


## OUTPUT




egrep '(^hello)' newfile 
![image](https://github.com/user-attachments/assets/59535622-8ec0-4aee-a661-199ecf7e3d1b)

## OUTPUT



egrep '(world$)' newfile 
![image](https://github.com/user-attachments/assets/50070604-026e-41c4-9fc8-92f4199136ca)

## OUTPUT



egrep '(World$)' newfile 
![image](https://github.com/user-attachments/assets/8761731f-3961-4658-99df-1512912add90)

## OUTPUT


egrep '((W|w)orld$)' newfile 
![image](https://github.com/user-attachments/assets/50c78d48-8c72-45bc-843b-e2532a081b0d)

## OUTPUT



egrep '[1-9]' newfile 
![image](https://github.com/user-attachments/assets/8f406516-7e91-49f2-968e-0b1da3754bf8)

## OUTPUT



egrep 'Linux.*world' newfile 
![image](https://github.com/user-attachments/assets/94852bfb-2688-4a6e-a7fc-17189ac750dc)

## OUTPUT


egrep 'Linux.*World' newfile 
![image](https://github.com/user-attachments/assets/e428cf56-fc1d-4eb2-bb05-469dabb2d3bb)

## OUTPUT


egrep l{2} newfile
![image](https://github.com/user-attachments/assets/96a549d7-2693-42d2-8e5b-617c8baeab46)

## OUTPUT



egrep 's{1,2}' newfile
![image](https://github.com/user-attachments/assets/a5a5ba72-215d-4f2d-977a-1d04531ca3f6)

## OUTPUT 


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
![image](https://github.com/user-attachments/assets/63a4f163-5b5e-460f-b231-242b01188548)

## OUTPUT



sed -n -e '$p' file23
![image](https://github.com/user-attachments/assets/b0ffd97d-6764-4487-b8b9-c3d6d1c53998)

## OUTPUT



sed  -e 's/Ram/Sita/' file23
![image](https://github.com/user-attachments/assets/c08d52c9-fad7-43e3-86fd-fb0e62625951)

## OUTPUT



sed  -e '2s/Ram/Sita/' file23
![image](https://github.com/user-attachments/assets/6b2ea900-ccc5-4b3c-a5da-fdea137cc4bc)

## OUTPUT



sed  '/tom/s/5000/6000/' file23
![image](https://github.com/user-attachments/assets/e8540dfb-09bd-4837-8901-6aec69e8e7b2)

## OUTPUT



sed -n -e '1,5p' file23
![image](https://github.com/user-attachments/assets/60910db0-37f1-40be-ac72-9077713bb822)

## OUTPUT



sed -n -e '2,/Joe/p' file23
![image](https://github.com/user-attachments/assets/c2928ee7-6dab-4c72-be9a-97493d74ad17)

## OUTPUT




sed -n -e '/tom/,/Joe/p' file23
![image](https://github.com/user-attachments/assets/e0c338ac-0880-4932-b8f5-d433c18887b5)

## OUTPUT



seq 10 
![image](https://github.com/user-attachments/assets/abd8cda6-c3bd-4934-8244-ff365e024da5)

## OUTPUT



seq 10 | sed -n '4,6p'
![image](https://github.com/user-attachments/assets/4dbbbb92-6ee3-4129-a5da-1ee5c792942e)

## OUTPUT



seq 10 | sed -n '2,~4p'
![image](https://github.com/user-attachments/assets/4acdf0d6-b924-4517-8b65-efff73062400)

## OUTPUT



seq 3 | sed '2a hello'
![image](https://github.com/user-attachments/assets/db84117b-f25e-4fe0-ae83-5eb28eb43e51)

## OUTPUT



seq 2 | sed '2i hello'
![image](https://github.com/user-attachments/assets/8e229639-1686-4261-b366-360dfc3410b0)

## OUTPUT


seq 10 | sed '2,9c hello'
![image](https://github.com/user-attachments/assets/c69039ce-a363-4c91-8c49-c132bb4a10cd)

## OUTPUT


sed -n '2,4{s/^/$/;p}' file23
![image](https://github.com/user-attachments/assets/22ef9ec8-b9f9-4729-aa2d-60bccb8dfc3c)

## OUTPUT



sed -n '2,4{s/$/*/;p}' file23
![image](https://github.com/user-attachments/assets/4e18de38-2be7-42e7-96db-82300a9123f9)



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
![image](https://github.com/user-attachments/assets/a71b31dd-c2a4-45ef-ba27-b1d71f60a6be)

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
![image](https://github.com/user-attachments/assets/68e4d9a9-054c-48cd-bf44-242499fb07fc)

## OUTPUT



#Using tr command

cat file23 | tr [:lower:] [:upper:]
![image](https://github.com/user-attachments/assets/59a18354-0718-426d-b737-193c4f3c1091)

 ## OUTPUT

cat < urllist.txt
![image](https://github.com/user-attachments/assets/372232ae-1a1c-4f4d-bbe1-0f144eb46a7e)

cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
![image](https://github.com/user-attachments/assets/54656e4c-9759-474d-a065-7c0e7a6ea56c)

 ## OUTPUT


 
cat urllist.txt | tr -d ' ' | tr -s '.'
![image](https://github.com/user-attachments/assets/a4d1c1c7-6edf-4f4b-a7b4-a6f37833b06d)

## OUTPUT



#Backup commands
tar -cvf backup.tar *
![image](https://github.com/user-attachments/assets/45c8826b-2163-4ab7-ab97-97bd37f787de)

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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


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
