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

<img width="1430" height="1100" alt="1t" src="https://github.com/user-attachments/assets/3506278b-6df0-454f-b2c2-aa9c6e16b935" />


cat < file2
## OUTPUT


<img width="1933" height="814" alt="2t" src="https://github.com/user-attachments/assets/8c06f21f-b316-4bd0-9d38-155928f69fbd" />



# Comparing Files
cmp file1 file2
## OUTPUT


<img width="2173" height="724" alt="3t" src="https://github.com/user-attachments/assets/e5a791ff-bbfb-4da8-8728-23bd8594ee1f" />

 
comm file1 file2
 ## OUTPUT


 <img width="1748" height="900" alt="4t" src="https://github.com/user-attachments/assets/075dba14-da40-4bb0-b8ac-e407be9d1ee6" />


 
diff file1 file2
## OUTPUT


<img width="1498" height="1050" alt="5t" src="https://github.com/user-attachments/assets/f8096c48-8540-48ee-87af-57362452ddb3" />


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


<img width="1971" height="798" alt="6t" src="https://github.com/user-attachments/assets/28f19e2e-383e-401f-ac2e-e0cff926ed18" />



cut -d "|" -f 1 file22
## OUTPUT


<img width="1776" height="886" alt="7t" src="https://github.com/user-attachments/assets/8b59a95b-94d5-44c5-8cb1-bcea0e37b184" />


cut -d "|" -f 2 file22
## OUTPUT


<img width="1725" height="912" alt="8t" src="https://github.com/user-attachments/assets/7c794146-fe75-4442-b5be-bc3e5ea94061" />


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


<img width="1969" height="799" alt="9t" src="https://github.com/user-attachments/assets/197d71b5-ed46-4ed4-aaf2-4bf088e969d1" />


grep hello newfile 
## OUTPUT



<img width="1942" height="809" alt="10t" src="https://github.com/user-attachments/assets/4c24f23b-95f0-4d41-b8f3-33da50f72c23" />


grep -v hello newfile 
## OUTPUT


<img width="1883" height="835" alt="11t" src="https://github.com/user-attachments/assets/c61a215a-6e95-4a4b-b9b2-b91796cf6720" />


cat newfile | grep -i "hello"
## OUTPUT


<img width="2166" height="726" alt="12t" src="https://github.com/user-attachments/assets/4d108e06-9432-46c6-b999-147da47e33ab" />



cat newfile | grep -i -c "hello"
## OUTPUT


<img width="2170" height="725" alt="13t" src="https://github.com/user-attachments/assets/69fe22cf-4f3e-4ae3-bd3f-04e1b3f0494f" />



grep -R ubuntu /etc
## OUTPUT


<img width="1609" height="977" alt="14t" src="https://github.com/user-attachments/assets/807e1e5e-9fe6-4ac9-a636-414fa09d41a7" />


<img width="1067" height="701" alt="15t" src="https://github.com/user-attachments/assets/58cfea6b-f65e-47d5-89ea-4d0dc848e4bc" />



<img width="1152" height="701" alt="16t" src="https://github.com/user-attachments/assets/f5df5762-e1c5-4239-b24a-0d940361fe9e" />



<img width="1142" height="589" alt="17t" src="https://github.com/user-attachments/assets/666adea8-c5e9-4c5a-916b-e1126b3ea8be" />


grep -w -n world newfile   
## OUTPUT


<img width="2159" height="728" alt="18t" src="https://github.com/user-attachments/assets/44f08daf-ef90-49ca-aa34-b23c3c5ce3c5" />


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


<img width="1774" height="886" alt="19t" src="https://github.com/user-attachments/assets/b3b88916-2cdf-4ac0-8964-27cc1b3313d4" />


egrep -w '(H|h)ello' newfile 
## OUTPUT


<img width="2163" height="727" alt="20t" src="https://github.com/user-attachments/assets/d3552f2e-aeda-4a23-bbb2-6accd727a821" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="1824" height="862" alt="21t" src="https://github.com/user-attachments/assets/6d9bc6e0-6632-4315-b1ca-247519b0b4eb" />



egrep '(^hello)' newfile 
## OUTPUT


<img width="1944" height="809" alt="22t" src="https://github.com/user-attachments/assets/019dde7a-2fb0-4e1f-a039-35b11a776999" />


egrep '(world$)' newfile 
## OUTPUT


<img width="2112" height="744" alt="23" src="https://github.com/user-attachments/assets/1010ab6a-3146-472b-92e5-608a319f30be" />


egrep '(World$)' newfile 
## OUTPUT


<img width="2041" height="771" alt="24" src="https://github.com/user-attachments/assets/a7c35423-b3f1-4da1-876b-03ba855f72f3" />


egrep '((W|w)orld$)' newfile 
## OUTPUT


<img width="2172" height="724" alt="25" src="https://github.com/user-attachments/assets/3131c365-549b-43e3-a302-0b774fe8bef4" />


egrep '[1-9]' newfile 
## OUTPUT


<img width="2169" height="725" alt="26" src="https://github.com/user-attachments/assets/05bb00d7-104c-46d1-baae-e0fb9d9aaa73" />


egrep 'Linux.*world' newfile 
## OUTPUT


<img width="1875" height="839" alt="27" src="https://github.com/user-attachments/assets/7a87f633-d307-43e6-83f4-37e62b869ab0" />


egrep 'Linux.*World' newfile 
## OUTPUT


<img width="2175" height="723" alt="28" src="https://github.com/user-attachments/assets/09494e28-916e-48a3-a866-0c900e5f9215" />


egrep l{2} newfile
## OUTPUT


<img width="2172" height="724" alt="29" src="https://github.com/user-attachments/assets/289260d2-2bb6-4be2-a7df-676c007433d6" />


egrep 's{1,2}' newfile
## OUTPUT 


<img width="2172" height="724" alt="30" src="https://github.com/user-attachments/assets/242c3400-529a-4c34-8ad6-bb7dd64baf04" />


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


<img width="2173" height="724" alt="31" src="https://github.com/user-attachments/assets/9ebbf27f-92ca-49d2-9f24-81038c45fb3c" />


sed -n -e '$p' file23
## OUTPUT


<img width="1949" height="807" alt="32" src="https://github.com/user-attachments/assets/b4081299-04fc-4d6b-b720-d0822679015a" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT



sed  -e '2s/Ram/Sita/' file23
## OUTPUT


<img width="2109" height="745" alt="33" src="https://github.com/user-attachments/assets/ce9eae12-f9ad-4ec0-966f-2bf227e3008e" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT


<img width="1915" height="821" alt="36" src="https://github.com/user-attachments/assets/bfe57004-813c-49ca-9262-ffa0cb572b85" />



sed -n -e '1,5p' file23
## OUTPUT


<img width="2173" height="724" alt="37" src="https://github.com/user-attachments/assets/2df93644-e00f-4533-b948-4690d59e47a1" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="1925" height="817" alt="38" src="https://github.com/user-attachments/assets/5498922d-b9b1-44e9-bc7b-7a4de1c0bcfd" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


<img width="2172" height="724" alt="39" src="https://github.com/user-attachments/assets/74de8eda-4aa1-4975-9942-231575086e3f" />


seq 10 
## OUTPUT


<img width="1893" height="831" alt="40" src="https://github.com/user-attachments/assets/1abc6378-df3a-4b98-9de1-6e307a5bfeba" />


seq 10 | sed -n '4,6p'
## OUTPUT



seq 10 | sed -n '2,~4p'
## OUTPUT


<img width="1945" height="808" alt="41" src="https://github.com/user-attachments/assets/e5a26f28-196b-4acb-9ba7-86851e2e0ae1" />


seq 3 | sed '2a hello'
## OUTPUT


<img width="2172" height="724" alt="43" src="https://github.com/user-attachments/assets/55e3c78c-1fa6-4a38-a959-e5b3dd4fba0e" />


seq 2 | sed '2i hello'
## OUTPUT


<img width="2166" height="726" alt="44" src="https://github.com/user-attachments/assets/d9ad279f-ff5c-4761-ab28-2f99c8bf44db" />


seq 10 | sed '2,9c hello'
## OUTPUT


<img width="2172" height="724" alt="42" src="https://github.com/user-attachments/assets/ed10d2b9-fd56-4284-b520-313c61e1c7b0" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


<img width="2172" height="724" alt="46" src="https://github.com/user-attachments/assets/28f8ff54-79a1-4601-9e92-d7eab0c31380" />


sed -n '2,4{s/$/*/;p}' file23


<img width="2172" height="724" alt="47" src="https://github.com/user-attachments/assets/eb87d501-e9b2-4b53-a87b-df5810342dc4" />


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


<img width="2172" height="724" alt="48" src="https://github.com/user-attachments/assets/534dbe4c-b633-4bf2-b66d-fe442705316c" />


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


<img width="2172" height="724" alt="49" src="https://github.com/user-attachments/assets/70024175-15d9-4847-827a-b5308f6779eb" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT


 <img width="1214" height="1295" alt="50" src="https://github.com/user-attachments/assets/2a00ddb8-a9fd-4480-a981-3b4e74a409b6" />


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


<img width="2172" height="724" alt="51" src="https://github.com/user-attachments/assets/4ef60e96-ad04-432c-968c-e55aee9e8f12" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


<img width="2172" height="724" alt="51" src="https://github.com/user-attachments/assets/0077a78a-86f3-42de-9451-b55d5d665f0d" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT


<img width="1254" height="1254" alt="52" src="https://github.com/user-attachments/assets/fd4bcc93-b946-474e-98b4-6f13572f01e9" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


<img width="1582" height="994" alt="53" src="https://github.com/user-attachments/assets/0d04f42c-c208-4026-933e-db14ae0ed4fa" />


<img width="1557" height="1010" alt="54" src="https://github.com/user-attachments/assets/47513e98-adf4-4106-9509-335f0d859803" />



tar -xvf backup.tar
## OUTPUT



<img width="1638" height="960" alt="55" src="https://github.com/user-attachments/assets/9e136180-ce03-4676-93ba-22bc9fd0d14e" />


gzip backup.tar

ls .gz
## OUTPUT


<img width="2172" height="724" alt="56" src="https://github.com/user-attachments/assets/e5bb9e0a-73cd-45e8-9475-655859369730" />

 
gunzip backup.tar.gz
## OUTPUT


<img width="2172" height="724" alt="57" src="https://github.com/user-attachments/assets/d0ed052e-5c2b-4f2e-a617-7c0b85921225" />


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT


<img width="1708" height="921" alt="58" src="https://github.com/user-attachments/assets/4efa7caa-dce6-4150-aaab-4b6ea6dd7e4d" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


<img width="1822" height="863" alt="59" src="https://github.com/user-attachments/assets/230afd29-551d-470e-b571-f22e28a755b9" />



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



<img width="1369" height="1149" alt="60" src="https://github.com/user-attachments/assets/3fc436aa-56e5-4318-86ec-58d7b69c1f9d" />



 
ls file1
## OUTPUT


<img width="1959" height="803" alt="61" src="https://github.com/user-attachments/assets/5ec5474c-1355-4583-9318-4018500c9324" />


echo $?
## OUTPUT 


<img width="1850" height="850" alt="62" src="https://github.com/user-attachments/assets/ff322814-787c-4778-acc1-2e4635568a74" />


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 


<img width="1880" height="836" alt="63" src="https://github.com/user-attachments/assets/606d3b61-fb94-4226-a04f-5c89a4901c36" />

 
abcd
 
echo $?
 ## OUTPUT


 <img width="1850" height="850" alt="62" src="https://github.com/user-attachments/assets/3083f426-e9bf-43d6-934b-952d3d85c8e6" />



 
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


<img width="1667" height="944" alt="64" src="https://github.com/user-attachments/assets/304bdcdb-3872-43a5-a12a-9d799624d134" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


<img width="1667" height="944" alt="64" src="https://github.com/user-attachments/assets/d28445c8-cc61-453c-8fe8-688672d1aef1" />


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


<img width="1677" height="938" alt="65" src="https://github.com/user-attachments/assets/6257f106-625e-4f53-8c03-667d82286514" />


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


<img width="2172" height="724" alt="66" src="https://github.com/user-attachments/assets/8c0bf68c-1ddf-4a5e-b8c0-7859101dc637" />


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


<img width="1707" height="921" alt="67" src="https://github.com/user-attachments/assets/5f25f498-3d9c-4dfb-93fd-38729676438d" />


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


<img width="2169" height="725" alt="68" src="https://github.com/user-attachments/assets/4af47331-9abc-4a21-b4e8-ebbc9db25f9f" />


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


<img width="1692" height="930" alt="69" src="https://github.com/user-attachments/assets/fb4797b8-d19e-4144-a49f-75c9ee76b3c8" />


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


<img width="1672" height="941" alt="70" src="https://github.com/user-attachments/assets/43f2a754-73c4-4dd8-a7ef-c7e364d1b6fc" />


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


<img width="1683" height="934" alt="71" src="https://github.com/user-attachments/assets/a2f678b0-aa23-444e-afa2-2a721575d150" />

 
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


<img width="1446" height="1088" alt="72" src="https://github.com/user-attachments/assets/75961944-09f3-4860-a3b7-a596b10d6937" />

 
 
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
 

 <img width="1717" height="916" alt="73" src="https://github.com/user-attachments/assets/69651612-223b-481a-8f05-fd247c8c26c9" />

 
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


 <img width="1774" height="886" alt="74" src="https://github.com/user-attachments/assets/ee642549-e09d-48ec-a107-29d29247405b" />

 
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


<img width="1563" height="1006" alt="75" src="https://github.com/user-attachments/assets/1644ab54-0ceb-4aec-ad3f-397278dab862" />

 
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


<img width="1563" height="1006" alt="75" src="https://github.com/user-attachments/assets/2bd9f267-978a-4bf8-9ebe-0d38bc8009a2" />

 
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


<img width="1555" height="1011" alt="76" src="https://github.com/user-attachments/assets/3bef860a-4d0a-4d54-93b0-cda478fb3c99" />

 
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

<img width="1555" height="1011" alt="76" src="https://github.com/user-attachments/assets/aa3b60bf-c7a5-4b99-9705-64c7ba772401" />


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


<img width="1774" height="886" alt="74" src="https://github.com/user-attachments/assets/c0dd13df-e158-4aa7-94ac-4a617e79754a" />


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


<img width="1677" height="938" alt="77" src="https://github.com/user-attachments/assets/c65d2635-73f8-4280-a800-5577956a1fe7" />


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


<img width="1739" height="904" alt="78" src="https://github.com/user-attachments/assets/c26594a2-aa64-4c8b-85cd-94c70fe3b8fe" />


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


<img width="1493" height="1054" alt="79" src="https://github.com/user-attachments/assets/663fda0c-06f4-4531-9c48-62d1d3f11a81" />

 
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


<img width="2007" height="783" alt="80" src="https://github.com/user-attachments/assets/8de33106-34d1-4ba4-9765-bddaca95ef1a" />


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


<img width="1939" height="811" alt="81" src="https://github.com/user-attachments/assets/2888e1c4-a448-4109-975a-1d4ac231133b" />

 
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


<img width="1905" height="825" alt="82" src="https://github.com/user-attachments/assets/0937f9ee-a82c-4e9e-a3bd-31966bde259a" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT


<img width="1905" height="825" alt="82" src="https://github.com/user-attachments/assets/079ffa6e-377a-4b30-b785-d4e56962633e" />


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


<img width="1935" height="812" alt="83" src="https://github.com/user-attachments/assets/c7e396ef-16a1-4b08-b4a5-4219d2f09499" />

 
 ./funcex.sh 1 2

 

<img width="1935" height="812" alt="83" src="https://github.com/user-attachments/assets/6b825990-35b0-4a30-bf39-3292fedf4e3f" />


 
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


<img width="1834" height="858" alt="85" src="https://github.com/user-attachments/assets/608b757a-cdf9-4db0-9655-d6904378f1fd" />

 
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


<img width="1153" height="1364" alt="86" src="https://github.com/user-attachments/assets/b46158e0-cdf7-4bad-a4f5-8ba34d5ddf78" />

 
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


 <img width="1153" height="1364" alt="86" src="https://github.com/user-attachments/assets/b8669a9e-6c29-4703-a494-bea9ef2dfa57" />

 
 
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


<img width="1560" height="1008" alt="87" src="https://github.com/user-attachments/assets/db05210b-ff45-4d1b-a4e4-ef71d34bf380" />

 
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



<img width="1600" height="983" alt="88" src="https://github.com/user-attachments/assets/8d041633-5408-487e-bf3e-c5bf7a6c958f" />


# RESULT:
The Commands are executed successfully.
