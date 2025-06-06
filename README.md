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

![419305196-65f6e7ec-7970-4a4f-ad9f-ce205b989706](https://github.com/user-attachments/assets/405d29b0-5e57-43de-b9dd-8e99ade3bd01)


cat < file2
## OUTPUT
![419305311-9c345b4f-261e-4c9a-926d-fa0bc70b49f7](https://github.com/user-attachments/assets/96830f21-5b97-4380-8faa-a3cf3276845b)


# Comparing Files
cmp file1 file2
## OUTPUT

 ![419305481-511bf3cd-3f4d-40a4-a03b-beae4fca2874](https://github.com/user-attachments/assets/9fdf2652-8495-4594-a0fb-c2ea0f1e53b0)

comm file1 file2
 ## OUTPUT

 ![419305588-12f7bf46-3647-43f5-93e9-5b5eb1a37f73](https://github.com/user-attachments/assets/519b3c8a-2b7e-4102-a36f-88553234060a)

diff file1 file2
## OUTPUT

![419305588-12f7bf46-3647-43f5-93e9-5b5eb1a37f73](https://github.com/user-attachments/assets/28a8543f-0c1d-4fbc-b034-1a7a7b8ee6a7)

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


![419305711-a83b5968-b67b-4858-9abc-a07dbd73690a](https://github.com/user-attachments/assets/8d2c77ed-9e43-4a60-9ffe-6731fb176160)


cut -d "|" -f 1 file22
## OUTPUT



cut -d "|" -f 2 file22
## OUTPUT

![419306289-8ec43151-7aba-49a7-95dc-a1d00b6705f0](https://github.com/user-attachments/assets/cfa0051f-a3ff-48f6-a331-b64750735e57)


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

![419306583-56f3293d-2f49-4f81-ac02-5a798b7a7e34](https://github.com/user-attachments/assets/d9439ded-03fc-41f2-a91b-c9465bc7f57a)


grep hello newfile 
## OUTPUT

![419306665-8eaef493-0be2-4550-9287-f3d5eadb7ce8](https://github.com/user-attachments/assets/536eee11-333a-4274-8818-9b400c411ce5)



grep -v hello newfile 
## OUTPUT

![419306763-03958186-a91f-4eaf-9d6c-cf21ec1a2715](https://github.com/user-attachments/assets/127048ee-8355-4bce-872a-9ca257316376)


cat newfile | grep -i "hello"
## OUTPUT


![419306825-60c796f3-520a-4eb4-9d38-31538cb41bac](https://github.com/user-attachments/assets/cbc27b27-2c6a-4107-9333-ffd1a9e4541b)


cat newfile | grep -i -c "hello"
## OUTPUT

![419306825-60c796f3-520a-4eb4-9d38-31538cb41bac](https://github.com/user-attachments/assets/ff6c7fd1-aac7-424e-a08b-1652a415a760)



grep -R ubuntu /etc
## OUTPUT

![419307008-c1a03299-9a44-4719-a72b-75102b75dea9](https://github.com/user-attachments/assets/fb33ca2d-52dc-49d7-bc73-05b8594fed5b)



grep -w -n world newfile   
## OUTPUT

![419307096-5436db2f-27d6-4562-95d9-e4fa4bf9d002](https://github.com/user-attachments/assets/695d7755-c4e8-4c61-8d16-0c2681ced11d)

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

![306325633-2f7618eb-26c9-4a06-b037-6e2a05e035a8](https://github.com/user-attachments/assets/4b0c79ac-862f-4f33-8ca9-f124b07f72f8)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![306325688-1586acca-2c82-4c42-98bc-4ae798eef1a8](https://github.com/user-attachments/assets/2c814c01-48eb-470e-90bc-6f6dcacc5536)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


![306325797-8688c525-73fb-44c1-aedc-42c6bf61741e](https://github.com/user-attachments/assets/4d53caa2-37fb-43fc-9ac7-271fdb89701e)


egrep '(^hello)' newfile 
## OUTPUT

![306326121-4980783d-eee0-4468-a932-ed98b32fb05f](https://github.com/user-attachments/assets/0bf67c17-348d-443c-b3c9-9b6f590078ae)


egrep '(world$)' newfile 
## OUTPUT

![306326236-0c3b9da2-1ec3-4ed6-afdf-d97b3ec65697](https://github.com/user-attachments/assets/e6a41d74-eaf8-4d9a-882a-faf0bcb56894)


egrep '(World$)' newfile 
## OUTPUT
![306326325-69094a6a-7169-4233-8e34-b63fd3b50f86](https://github.com/user-attachments/assets/861bc1e9-4332-41dc-9520-c7aa65514c16)

egrep '((W|w)orld$)' newfile 
## OUTPUT


![306326400-228361e3-4c51-408b-acae-b547654c8d92](https://github.com/user-attachments/assets/429116a4-d0d1-4093-9e5a-5e1b945e8e6b)

egrep '[1-9]' newfile 
## OUTPUT

![306326507-78841f5b-a1d6-42da-a170-f873f2db1c02](https://github.com/user-attachments/assets/3fa7cbef-abcf-4c07-ba8d-66dce9bf204b)


egrep 'Linux.*world' newfile 
## OUTPUT

![306326696-218b2ba3-76f4-4fe8-8822-3d64fc006de9](https://github.com/user-attachments/assets/0076c39f-ee2a-4285-a8b4-626753d8b1bc)


egrep 'Linux.*World' newfile 
## OUTPUT

![306327153-e0fb9fd4-0e34-4bb0-b447-480e7353e23c](https://github.com/user-attachments/assets/bead975d-a0fc-4900-90e7-2ab1cb79a109)

egrep l{2} newfile
## OUTPUT

![306327065-455cefd1-c3cf-4a56-9626-22f5acc9d758](https://github.com/user-attachments/assets/dda29579-cd3e-4491-a5e1-8e1663e92357)

egrep 's{1,2}' newfile
## OUTPUT 

![306327376-8b7b973d-2ecb-4adf-b3b0-b4a6090238f4](https://github.com/user-attachments/assets/b5387125-1bb6-477c-ae21-84c522841257)

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

![306327645-6ed8eeb2-98aa-489d-b7b5-502fad1fa948](https://github.com/user-attachments/assets/9cc00d1c-8413-41ab-a285-f127750060ed)


sed -n -e '$p' file23
## OUTPUT

![306327739-a525b7f6-5451-4607-bf43-47e41df195cc](https://github.com/user-attachments/assets/a0a09d9c-3e3f-46e1-928f-991de9ad693e)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![306327903-2dec5d41-9a09-4e5e-8b9e-124614c5ba56](https://github.com/user-attachments/assets/22b25459-e828-4b2f-99ad-7f3f3d9145fb)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![306328067-18fb9a8e-d5ce-4f68-8d04-799b2e781cd6](https://github.com/user-attachments/assets/e9153dcd-6e90-4dc7-b964-5f2ae855c46d)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![306328125-5209fed2-c815-4dd9-bbfc-885f9104d28a](https://github.com/user-attachments/assets/300719b3-e4b3-4114-bd8f-33e25da50f61)



sed -n -e '1,5p' file23
## OUTPUT

![306328252-59481f62-1000-4099-be96-30a15f0f9f9f](https://github.com/user-attachments/assets/9f7d9ec4-0c6d-4e29-8b9c-c9142be0ac85)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![306328320-c1935ffc-35e7-488e-a332-e3dd4c0b4220](https://github.com/user-attachments/assets/86755818-e2b6-4bed-97eb-2b5a6fef49ad)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![306328404-3156abad-90b0-40bc-82f2-7e288e6776c9](https://github.com/user-attachments/assets/d25af9eb-556e-4239-88fc-be478732b379)


seq 10 
## OUTPUT

![306328511-ea0f93d4-b7fe-4b56-83f8-5df261f74fcb](https://github.com/user-attachments/assets/99924430-987b-45a3-8519-434ffa56af62)


seq 10 | sed -n '4,6p'
## OUTPUT

![306328612-bc5e24b5-5130-4756-b972-bd061802099e](https://github.com/user-attachments/assets/a6443907-405c-4f24-b796-5f2f55814402)



seq 10 | sed -n '2,~4p'
## OUTPUT

![306328704-af99d8d5-a0fb-4a3f-8391-4ce396c27f9f](https://github.com/user-attachments/assets/9385699c-286a-4d8b-b157-91f15111a8b0)


seq 3 | sed '2a hello'
## OUTPUT

![306328812-ebff4972-2af6-4823-8af3-5a2218ed0f9e](https://github.com/user-attachments/assets/79442aa0-5003-40b0-8724-2f333e500c3d)

seq 2 | sed '2i hello'
## OUTPUT

![306329113-6a7d5a34-213f-4d78-a264-72be126d9325](https://github.com/user-attachments/assets/e6481375-ae6b-4c63-84b6-2dd9d52e9d85)


seq 10 | sed '2,9c hello'
## OUTPUT
=

sed -n '2,4{s/^/$/;p}' file23![306329230-56f96442-9167-4513-812b-07e8b22b9252](https://github.com/user-attachments/assets/e3198016-cd4e-40f1-9192-82a945fef4eb)

## OUTPUT

![306329333-cbadd6df-119c-4a6a-b7ac-8888a033311e](https://github.com/user-attachments/assets/77e5e64f-6413-4c4d-a0be-3f5e930a10d0)


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

![306329585-36d38ad5-fd86-4e5d-86f3-734e1c0390bc](https://github.com/user-attachments/assets/963d9569-ddc3-4893-a8ca-3b4b071f4daf)

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

![306329910-b947d6ba-4de8-436b-a7b7-fd88455c4fa3](https://github.com/user-attachments/assets/1604b82a-2478-4765-956c-92ef4efcea26)

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

![306329989-df15d132-7d04-43d4-ae87-87bb88a3e002](https://github.com/user-attachments/assets/d2bba9f7-1c22-4a75-9e83-6ec16e97bc3f)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 
![306330077-2fe37e25-e5ba-4bbb-9209-9980e7b79ff5](https://github.com/user-attachments/assets/6bf99be4-8a14-4554-9cfc-5508aa8ae281)

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

![306330127-3d90c98b-a7b3-43f6-8674-b310a5ab193b](https://github.com/user-attachments/assets/86adb758-6281-46db-aa26-8859a1876c1e)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![306330188-ca555058-30ad-4a25-899a-81179c28d117](https://github.com/user-attachments/assets/1475d7e6-b29f-4493-9c25-138ab7f621c4)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![307496539-d813cb49-6684-4e3c-8570-ea7d6368b688](https://github.com/user-attachments/assets/1cbfa51c-5fc1-4e09-a1c4-a1919540cb95)


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


![307496550-70216941-d36d-4b4a-88a5-8243e9fd3ebf](https://github.com/user-attachments/assets/b5415ad2-eaa8-4797-ab48-fbd6fc6f53bf)

tar -xvf backup.tar
## OUTPUT

![image-43](https://github.com/user-attachments/assets/26bb2e82-db15-47fa-8f19-2570d171fcac)

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 ![image-44](https://github.com/user-attachments/assets/4b0f7544-3332-4af8-85b2-301418acd036)

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 ![image-49](https://github.com/user-attachments/assets/83b13172-0f96-4827-8640-3a20212215ce)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![image-50](https://github.com/user-attachments/assets/a55eb5f6-f323-4d90-a8f9-0c452eb35ab9)

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

 ![image-51](https://github.com/user-attachments/assets/56717133-5f69-4384-bba8-1a06b3c69388)

ls file1
## OUTPUT

![image-52](https://github.com/user-attachments/assets/974b9706-38e8-438e-80a3-45cc85953a68)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

 ![image-53](https://github.com/user-attachments/assets/f1fbb650-b038-4b7b-a534-5797a7b3fe0c)

abcd
 
echo $?
 ## OUTPUT

![image-54](https://github.com/user-attachments/assets/ed91a594-02f4-483e-8eb2-5aa551e2a3b0)

 
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

![image-55](https://github.com/user-attachments/assets/55d8539b-dde3-4329-8aa5-620409a825d3)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![image-56](https://github.com/user-attachments/assets/a20d8088-1cc9-4451-a14c-b4d13856e6e9)

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

![image-57](https://github.com/user-attachments/assets/699b4cf4-f2d9-4c39-ac1f-a8662000dcd4)

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

![image-58](https://github.com/user-attachments/assets/9910aa55-1412-431c-8c9d-e32e0bc26571)


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

![image-59](https://github.com/user-attachments/assets/12731c50-120d-4170-8b0c-fb962fe9de7c)

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

![image-60](https://github.com/user-attachments/assets/43352d16-cee9-4484-bd55-b2b3e19a1508)

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

![image-61](https://github.com/user-attachments/assets/d164b671-cb0e-4592-806d-6dc5759ec667)

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

![image-62](https://github.com/user-attachments/assets/178c5016-70bc-40b9-b138-3332161202b3)

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
 
 ![image-65](https://github.com/user-attachments/assets/73f22e5f-1c6b-478d-8703-c5c0f85b3f70)

 
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
 
 ![image-66](https://github.com/user-attachments/assets/dbd027c0-7334-4071-8116-8b718e3f535f)

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

![image-67](https://github.com/user-attachments/assets/283016ae-7a65-4113-8cbd-c05fac34b692)

```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 ![image-67](https://github.com/user-attachments/assets/4654acc3-bbbd-4d05-84a1-a0309adf8dbb)

$ ./forin2.sh 

 ![image-68](https://github.com/user-attachments/assets/25a5862c-8c23-4310-ada6-11c469f3a1b2)

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

![image-69](https://github.com/user-attachments/assets/45ce32c3-0625-4c6c-9174-6f1dd5765d1d)

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
![image-70](https://github.com/user-attachments/assets/a7ffb6c7-7b35-46ba-a625-c14d0389ac6b)

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
![image-71](https://github.com/user-attachments/assets/b47198cc-4a04-4263-8dc1-ca633385a89e)

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

 ![image-72](https://github.com/user-attachments/assets/cd3eb656-ec37-45f0-acc6-11a5ded0a068)

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
![image-73](https://github.com/user-attachments/assets/72eedeed-72c4-436a-a138-b572137b6a07)

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 ![image-74](https://github.com/user-attachments/assets/26a73d0a-0a85-4a63-8c79-8b6e18c692ed)

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
 ![image-75](https://github.com/user-attachments/assets/f4dde8a2-ba74-47f0-b5b0-825d34e85c27)

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

![image-76](https://github.com/user-attachments/assets/91cb01b0-3692-4ed1-8506-a87cd20c47f1)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![image-77](https://github.com/user-attachments/assets/3c9f7665-651f-45ff-b5a6-81268740d339)


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

 ![image-78](https://github.com/user-attachments/assets/3d533f7d-57de-4042-a043-ad2482f06118)

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
 ![image-79](https://github.com/user-attachments/assets/966b1802-a2e0-4bb9-a672-5348f8627d4a)

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

 ![image-80](https://github.com/user-attachments/assets/ea3ab9f4-8ff4-4f6a-a821-6d2fc93df237)

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
 

![image-83](https://github.com/user-attachments/assets/008fef8a-195d-402c-a983-07f13d1c194f)

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

 ![image-82](https://github.com/user-attachments/assets/d0c95306-1c81-4d2c-b04f-1d781b9b35c9)

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

![image-84](https://github.com/user-attachments/assets/c949702f-67fb-4f51-b35a-c37f43da72dd)

# RESULT:
The Commands are executed successfully.
