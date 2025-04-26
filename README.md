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
// git add-h // git commit // git origin
### Display the content of the files
cat < file1
## OUTPUT

![image](https://github.com/user-attachments/assets/a6eb9c57-fe0f-4646-b957-fa8b9b2ff39f)


cat < file2
## OUTPUT
![Screenshot 2025-04-26 131701](https://github.com/user-attachments/assets/52862181-0ce9-465b-802a-14403aebb7d8)


# Comparing Files
cmp file1 file2
## OUTPUT
![Screenshot 2025-04-26 133107](https://github.com/user-attachments/assets/7bc898bc-e238-4eff-b8b3-36b5ac229c6b)
 
comm file1 file2
 ## OUTPUT
![Screenshot 2025-04-26 133152](https://github.com/user-attachments/assets/0ca45abc-34ba-43ae-89f8-79e52e6fb35d)
 
diff file1 file2
## OUTPUT
![Screenshot 2025-04-26 133424](https://github.com/user-attachments/assets/751af00b-9d92-47a1-91e7-4a06116ebebd)

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

![Screenshot 2025-04-26 133547](https://github.com/user-attachments/assets/42ae70d5-8995-47d5-bfae-7fece2c8b15d)



cut -d "|" -f 1 file22
## OUTPUT

![Screenshot 2025-04-26 133611](https://github.com/user-attachments/assets/11f01138-c2ea-4521-8f55-aac9f0c4472f)


cut -d "|" -f 2 file22
## OUTPUT
![Screenshot 2025-04-26 133635](https://github.com/user-attachments/assets/d86c1747-e667-4d64-807f-266365ba1163)



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
![Screenshot 2025-04-26 133757](https://github.com/user-attachments/assets/a5c9e232-da99-4380-8643-644ed87562b4)


grep hello newfile 
## OUTPUT

![Screenshot 2025-04-26 133846](https://github.com/user-attachments/assets/2064b47a-0e5a-43b5-bc9e-72ea603ba70a)


grep -v hello newfile 
## OUTPUT

![Screenshot 2025-04-26 133948](https://github.com/user-attachments/assets/6fb2cf5b-9434-46e8-9e2c-de9530763382)


cat newfile | grep -i "hello"
## OUTPUT

![Screenshot 2025-04-26 134040](https://github.com/user-attachments/assets/73bd5d72-95e4-4ae1-92b9-16fdeb2796f0)

cat newfile | grep -i -c "hello"
## OUTPUT

![Screenshot 2025-04-26 134107](https://github.com/user-attachments/assets/f823978f-ca84-4820-b29f-4d4ccb8f505a)


grep -R ubuntu /etc
## OUTPUT

![Screenshot 2025-04-26 134132](https://github.com/user-attachments/assets/76cfc122-c0c1-4bd6-9642-9a5fec171bd5)

grep -w -n world newfile   
## OUTPUT

![Screenshot 2025-04-26 134216](https://github.com/user-attachments/assets/0286da79-da1a-47b7-9f0e-713119246e70)

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

![Screenshot 2025-04-26 134248](https://github.com/user-attachments/assets/3942d80c-cc44-445c-adec-17868c2f2c8d)

egrep -w '(H|h)ello' newfile 
## OUTPUT

![Screenshot 2025-04-26 134322](https://github.com/user-attachments/assets/a3bea560-feed-4b0c-9a7d-aad88207929c)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![Screenshot 2025-04-26 134343](https://github.com/user-attachments/assets/018849e5-c99e-4c4a-bf82-b81a161096db)


egrep '(^hello)' newfile 
## OUTPUT

![Screenshot 2025-04-26 134410](https://github.com/user-attachments/assets/468ea48d-ee5b-46c8-aa4c-ffa1912502dd)


egrep '(world$)' newfile 
## OUTPUT

![Screenshot 2025-04-26 134436](https://github.com/user-attachments/assets/bfb62a82-1dbb-401b-966e-9871fb832a2c)


egrep '(World$)' newfile 
## OUTPUT

![Screenshot 2025-04-26 134457](https://github.com/user-attachments/assets/8baa63b9-c1fb-4f7b-a57a-17a96cdefbb1)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![Screenshot 2025-04-26 134532](https://github.com/user-attachments/assets/431dd26e-14ce-4c6c-a4e0-275dad9d734e)


egrep '[1-9]' newfile 
## OUTPUT

![Screenshot 2025-04-26 134602](https://github.com/user-attachments/assets/70ec5242-50bd-46a4-9a77-824e63e28d98)


egrep 'Linux.*world' newfile 
## OUTPUT

![Screenshot 2025-04-26 134636](https://github.com/user-attachments/assets/c4527d1c-34d7-47ab-be33-9a4d5cfeb3a8)


egrep 'Linux.*World' newfile 
## OUTPUT

![Screenshot 2025-04-26 134703](https://github.com/user-attachments/assets/81ee3ab2-8f14-4387-ad7a-1c0ecd28abb3)

egrep l{2} newfile
## OUTPUT

![Screenshot 2025-04-26 134730](https://github.com/user-attachments/assets/c16f0652-fad8-4447-bc2c-92bb2127307a)


egrep 's{1,2}' newfile
## OUTPUT 

![Screenshot 2025-04-26 134850](https://github.com/user-attachments/assets/8ad177c9-0135-4450-97f3-69eb301a1bb8)


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

![Screenshot 2025-04-26 134850](https://github.com/user-attachments/assets/e39a31a5-97d1-4fdd-99d6-7e44bd952009)


sed -n -e '$p' file23
## OUTPUT
![Screenshot 2025-04-26 134927](https://github.com/user-attachments/assets/71ddedf8-ee4b-4618-a0ef-9c2397863b7e)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![Screenshot 2025-04-26 134949](https://github.com/user-attachments/assets/7b7732ca-5167-4588-bc45-451a2865d458)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![Screenshot 2025-04-26 135033](https://github.com/user-attachments/assets/30e2a5f9-5d8d-4518-a0bc-3e9a58b5046a)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![Screenshot 2025-04-26 135033](https://github.com/user-attachments/assets/f6e033a9-6b56-4366-81e9-cb3f1f279dc2)


sed -n -e '1,5p' file23
## OUTPUT

![Screenshot 2025-04-26 135107](https://github.com/user-attachments/assets/a6b72e76-77a3-42e9-9288-e9afab6b591d)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![Screenshot 2025-04-26 135133](https://github.com/user-attachments/assets/89a561d3-5f3d-4df5-9c26-1912ee893190)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![Screenshot 2025-04-26 135216](https://github.com/user-attachments/assets/11486057-c3f6-4bd3-8cea-74304ae46476)


seq 10 
## OUTPUT

![Screenshot 2025-04-26 135238](https://github.com/user-attachments/assets/367fa13e-f2ce-484b-bed8-bdbc984c1c67)


seq 10 | sed -n '4,6p'
## OUTPUT

![Screenshot 2025-04-26 135302](https://github.com/user-attachments/assets/e4745a2f-6e19-4b49-ad9c-f8673b4ce25d)


seq 10 | sed -n '2,~4p'
## OUTPUT

![Screenshot 2025-04-26 135349](https://github.com/user-attachments/assets/37609b96-4464-4ba5-8f5b-8e4c8e24faac)



seq 3 | sed '2a hello'
## OUTPUT

![Screenshot 2025-04-26 135419](https://github.com/user-attachments/assets/cfaab6e5-bb9e-4dd1-b8bf-0a8fe12a7699)


seq 2 | sed '2i hello'
## OUTPUT

![Screenshot 2025-04-26 135441](https://github.com/user-attachments/assets/e04d7355-f4cd-46b1-b561-dcfd13ef14c5)

seq 10 | sed '2,9c hello'
## OUTPUT

![Screenshot 2025-04-26 135533](https://github.com/user-attachments/assets/9514860d-c455-4c1e-904a-f82e0fd337ec)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![Screenshot 2025-04-26 135736](https://github.com/user-attachments/assets/fa50a666-69da-4b32-9e0f-c9bae335d9a7)


sed -n '2,4{s/$/*/;p}' file23
![Screenshot 2025-04-26 135807](https://github.com/user-attachments/assets/a64dbc59-2505-4e0e-a4f2-12b5e0555f65)


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

![Screenshot 2025-04-26 135834](https://github.com/user-attachments/assets/bd9f6484-998c-400f-84af-0fd14e18d9a6)

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

![Screenshot 2025-04-26 135905](https://github.com/user-attachments/assets/35290cd9-f165-4a8a-87cf-28a6e16dfdb3)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![Screenshot 2025-04-26 135937](https://github.com/user-attachments/assets/e3ee3113-98b2-4bd9-b533-5f9216da5658)

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

![Screenshot 2025-04-26 140000](https://github.com/user-attachments/assets/5ea3d39d-78a6-4c03-a72c-5fe595164c64)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![Screenshot 2025-04-26 140030](https://github.com/user-attachments/assets/8f822477-f3bc-4221-adb8-55b2cc23c7b4)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot 2025-04-26 140110](https://github.com/user-attachments/assets/11b6a13e-72d8-49a0-847e-85140f42f387)

mkdir backupdir
 
mv backup.tar backupdir

## OUTPUT

![Screenshot 2025-04-26 140148](https://github.com/user-attachments/assets/81305ce3-a5a4-4f81-9bc6-cd21d3e87d19)
![Screenshot 2025-04-26 140220](https://github.com/user-attachments/assets/0f331d9c-3a96-4d96-bf68-4128763e64f7)


tar -xvf backup.tar
## OUTPUT

![Screenshot 2025-04-26 140913](https://github.com/user-attachments/assets/aa2e04fc-b1a8-46f2-af35-e9ef1be80af2)
![Screenshot 2025-04-26 140944](https://github.com/user-attachments/assets/5b975203-0880-4de0-b759-fd23dc45858c)


gzip backup.tar

ls .gz
## OUTPUT

 ![Screenshot 2025-04-26 141006](https://github.com/user-attachments/assets/8568f424-71ec-4cde-9cf4-10f8e4b770c6)

gunzip backup.tar.gz
## OUTPUT

![Screenshot 2025-04-26 141027](https://github.com/user-attachments/assets/c93f9bfd-b917-4b6c-bab0-58fdc1fff70a)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

![Screenshot 2025-04-26 141109](https://github.com/user-attachments/assets/80b19c1b-f178-45c6-9a8c-ee003d7b4837)
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![Screenshot 2025-04-26 141332](https://github.com/user-attachments/assets/748ec295-c846-422b-a3a6-a47bc853fc5e)


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

![Screenshot 2025-04-26 141402](https://github.com/user-attachments/assets/79f4e162-2a6d-4fc4-a087-5739741f89af)

 
ls file1
## OUTPUT
![Screenshot 2025-04-26 141435](https://github.com/user-attachments/assets/80b4b65c-cba4-4cf5-bab4-26bb27059927)


## OUTPUT 
![Screenshot 2025-04-26 141531](https://github.com/user-attachments/assets/57b30a64-04fd-4538-8d07-84aeb79de0cc)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

 ![Screenshot 2025-04-26 141558](https://github.com/user-attachments/assets/0f7b3321-c13e-42d7-9c8c-b5804b0e8542)

abcd
 
echo $?
 ## OUTPUT

![Screenshot 2025-04-26 141621](https://github.com/user-attachments/assets/e66fd17e-c6a7-4862-8b71-a3c772490cd7)

 
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

![Screenshot 2025-04-26 141644](https://github.com/user-attachments/assets/4dddbf46-5351-4782-b9cb-c94adf1f50b2)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![Screenshot 2025-04-26 141707](https://github.com/user-attachments/assets/7959fa99-6cec-4f2a-be56-1750eb972d98)

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

![Screenshot 2025-04-26 141729](https://github.com/user-attachments/assets/a36c8c79-4d14-485d-895a-f7ac0f10e210)

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

![Screenshot 2025-04-26 141801](https://github.com/user-attachments/assets/98891aee-4291-4ac4-a48e-9385919d768d)


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

![Screenshot 2025-04-26 141838](https://github.com/user-attachments/assets/3fbdfdb9-1e66-41ee-9208-1a86a26e8186)


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

![Screenshot 2025-04-26 141917](https://github.com/user-attachments/assets/a0d360a1-bfe4-402e-8cb0-1068f36d872d)

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

![Screenshot 2025-04-26 141946](https://github.com/user-attachments/assets/e4b342fb-8aa6-484f-a838-966ba297244a)


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

![Screenshot 2025-04-26 142021](https://github.com/user-attachments/assets/282aad9c-ba8e-42b8-a13d-75c2698051bf)

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

![Screenshot 2025-04-26 142109](https://github.com/user-attachments/assets/3f5adaac-2219-4311-a449-bc182004798c)

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
## OUTPUT

![Screenshot 2025-04-26 142150](https://github.com/user-attachments/assets/a215e80c-f9f7-4781-b9a2-b5eba325843c)

 
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

## OUTPUT
![Screenshot 2025-04-26 142226](https://github.com/user-attachments/assets/8393253f-17f1-4659-8c01-550e8f0f3d0b)

 
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

## OUTPUT

![Screenshot 2025-04-26 142317](https://github.com/user-attachments/assets/c0e35b4d-2808-415b-b260-1585d97c9f58)

 
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

## OUTPUT

![Screenshot 2025-04-26 142523](https://github.com/user-attachments/assets/1fb78448-15c6-410f-8bb8-9f23418ee481)

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

![Screenshot 2025-04-26 142604](https://github.com/user-attachments/assets/7c5154da-9da8-466e-b18f-526c8e06019a)

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

![Screenshot 2025-04-26 142628](https://github.com/user-attachments/assets/001faf45-3dbd-44ba-9337-69b12ec36f2d)


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

![Screenshot 2025-04-26 142648](https://github.com/user-attachments/assets/4d013db1-b391-4a32-ad1e-1fcbe0326181)

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

![Screenshot 2025-04-26 142713](https://github.com/user-attachments/assets/5990513d-4897-46e4-ab0b-231cead28c59)

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
 
![Screenshot 2025-04-26 142735](https://github.com/user-attachments/assets/5b82a56b-adce-4976-a12b-d3e4fbf85db0)

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

![Screenshot 2025-04-26 142932](https://github.com/user-attachments/assets/d8ccc608-54c1-4370-b721-2d271b38867a)

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

 ![Screenshot 2025-04-26 143140](https://github.com/user-attachments/assets/00520676-bc18-4452-8488-02f3b09d0c34)

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

![Screenshot 2025-04-26 143239](https://github.com/user-attachments/assets/bafe9abb-fc92-4f04-85ce-3e64e3e51aaa)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 
$ ./exread.sh 
## OUTPUT

![Screenshot 2025-04-26 143329](https://github.com/user-attachments/assets/bd4934ff-affc-4629-85fd-06f364bbfde3)

 
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

![Screenshot 2025-04-26 143608](https://github.com/user-attachments/assets/2216195b-4674-4b07-a6c1-e81d0ee96990)

 ./funcex.sh 1 2
 ![Screenshot 2025-04-26 143623](https://github.com/user-attachments/assets/4d6a9681-e184-4773-ac5d-e461123956b0)

 
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

 ![Screenshot 2025-04-26 143650](https://github.com/user-attachments/assets/0568103c-f4e5-43bb-a709-c3b164befc61)

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

 ![Screenshot 2025-04-26 143710](https://github.com/user-attachments/assets/d111999b-291b-4a2d-9a42-55ba1d21d726)

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
 
![Screenshot 2025-04-26 143730](https://github.com/user-attachments/assets/9078907a-119c-411d-a0f5-7f3cb4e795a0)
 
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

 ![Screenshot 2025-04-26 143757](https://github.com/user-attachments/assets/d273e487-9a17-4df4-9a9e-29ad3b06cc00)

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
![Screenshot 2025-04-26 143818](https://github.com/user-attachments/assets/aea0748b-ed2a-494d-9fe9-ac274392e218)


# RESULT:
The Commands are executed successfully.
