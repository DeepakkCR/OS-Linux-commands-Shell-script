-------------# OS-Linux-commands-Shell-scripting
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
![image](https://github.com/user-attachments/assets/254e2afa-96bc-4718-bde1-80e5326ede62)



cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/968b8301-3338-4bcb-9a89-647165d690e9)



# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/user-attachments/assets/d68422b4-3b14-412a-8bd2-2ee6613fa10b)

comm file1 file2
 ## OUTPUT
![image](https://github.com/user-attachments/assets/2d16a4f6-83e6-42e6-8302-799eb940e1eb)

 
diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/d2401c96-e81c-43be-9f49-7a2207821107)


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
![image](https://github.com/user-attachments/assets/cbc81388-735a-4c12-aeea-260bac580fc8)





cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/a50f8a6b-e0f5-4828-9acf-6b7b052cf09a)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/51746f48-6f97-44bb-8f19-4d86f96b9f70)


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
![image](https://github.com/user-attachments/assets/f14becc2-93a3-4d8e-848e-39193d62386b)



grep hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/3b9ae169-addf-4de4-b3e5-d103ad9eb648)




grep -v hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/c3ccf95d-bdc8-49f6-b3fc-a75543703855)



cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/eeaa250f-8ee7-4dca-b4ff-cc4e0462eeb6)




cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/c2f82cc8-0e37-4710-9920-87c3e6ab00cf)




grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/ad96ae2c-f1ec-463a-8535-20b724634e8d)


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
![image](https://github.com/user-attachments/assets/4ed7026d-47d7-4526-941f-3aa2c9901461)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/2fff13b7-d061-47b7-9d64-5a2ca512b5d5)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/720d9f74-ad10-4bd1-930f-4889b5e3b6ba)




egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/5c36a53d-43f5-43dc-b6e1-d0a16a40562d)



egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/ecd4a49e-f80b-48bc-8660-b96500bd47af)



egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/9b9b8482-1ec1-4a72-b1ff-58cde0321c3b)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/05496e80-096e-4b4e-8184-e85d1e91d46b)



egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/d3355f27-81c4-41e2-b1cb-6076214b3528)



egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/125bfd29-944c-4278-abca-f966c6f505e9)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/9af3f822-dcc4-4843-a06f-c3d2c356c088)


egrep l{2} newfile
## OUTPUT
![image](https://github.com/user-attachments/assets/efea0d84-7dc3-4d07-8753-786c9be45b23)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/e0c45d44-b12b-4e3e-a5f4-9095162eddb6)


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
![image](https://github.com/user-attachments/assets/9d936f90-bc10-4d87-afe5-8db985ed0ca4)



sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/08dce932-4592-4cb6-8d1e-ab72f7e4f1d4)



sed  -e 's/Ram/Sita/' file23
## OUTPUT



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/4578b9be-90d8-4eeb-bc45-71351e0003a3)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/a9f80edd-6fe7-4737-9d2b-25fd7c8065bc)



sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/1ec1364c-2125-4c3a-9daf-0e3a4e7f7fc2)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/b2181e8f-a9e7-4000-b828-8f17ed188a5b)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/08fc25df-fc1c-41cc-8285-ac34e5e29b64)



seq 10 
## OUTPUT
![image](https://github.com/user-attachments/assets/ebdc2a9a-c7c9-4721-b030-589d2014b61e)



seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/user-attachments/assets/bd7ed776-8039-4ccb-9e25-973dfc7470c8)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/user-attachments/assets/b596461e-3c0a-48fc-8c4d-b71cd9561f62)



seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/d2060a7c-92ed-4aa5-9054-7103b83cf80f)



seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/1ba62217-6a93-4a9a-9d1d-e422b83210af)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/bd0b4baa-2855-40e0-8ca8-08500bc972f3)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/d754f646-e82d-4a6c-ad66-2bfe71397e01)



sed -n '2,4{s/$/*/;p}' file23
![image](https://github.com/user-attachments/assets/07d61ed9-5b47-42b0-9654-72b5ab3a181b)


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
![image](https://github.com/user-attachments/assets/ecf025f3-d389-4e3c-ba0c-2e1e6a0295dc)


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
![image](https://github.com/user-attachments/assets/5b1f5c69-0435-43ea-b584-bbdfb1f91ffc)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/user-attachments/assets/d118b1f2-6f10-40c1-9fc1-93e077555e63)

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
![image](https://github.com/user-attachments/assets/766d0700-6dbc-4029-b769-707ebc899143)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/user-attachments/assets/a376e44b-7c57-4105-acd8-def5d9d9b90f)



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/efee4341-936a-47cb-a236-7a07b23e7f54)


tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/5df40a50-beff-4640-8e20-02ce85599867)

gzip backup.tar

ls .gz
## OUTPUT
 ![image](https://github.com/user-attachments/assets/1889bf5f-e798-46d7-951c-fe45defbf24c)

gunzip backup.tar.gz
## OUTPUT
![image](https://github.com/user-attachments/assets/829da5ed-7c29-4a98-9de5-af8827a27ae7)

 
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
![image](https://github.com/user-attachments/assets/360c4e3e-71f0-4f62-80aa-cb283001eb00)


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
![image](https://github.com/user-attachments/assets/305fbf9d-80a1-411f-ba2a-7a1fb7611ad8)

 
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
