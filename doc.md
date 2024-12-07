# Linux

# whoami

# ls
ls -l (check file owners)

# change permission
chown root file.txt (change file owner to other (root))


# Make Directory
mkdir folder_name

# make dir inside dir
mkdir -p folder/inside_folder/inside_folder

# Create file
touch file.extension
touch dir_name/file_name.extension


# It will print the string
echo "ashish"

# It'll print the string inside file
echo "ashish.kushwaha" > file_name.txt

# create file
cat > file_name.extenstion

# print what inside it
cat file_name.extension

# merget the content inside the file
cat file_name.extension file_name2.extension > file_name.txt

# open file for edit
vi file_name.extension

# present working directory
pwd

# To know about the command
man commond

# pipe ( | )
output from the first command act as the input for the second command
( > ) redirect output
cat file.txt | tr a-z A-Z > upper.txt

# copy
cp file_name.txt copy_file.txt

# copy dir
cp -R dir_1 dir_2

# move
mv file/folder folder

mv file_name new_file_name // will rename the file

# remove file
rm file_name

rm -R dir_name

# Disk space uses
for hard drive
df
df -m ( show file in mb )
df -h( show file in human readable)

for current dir
du -h

# head / tail
head file.txt
head -n number file.txt

tail file.txt (see 10 above line)
tail -n number file.txt (see number of line)
tail -f file.txt (see full file)


# compare file line by line
diff file.txt file_2.txt

# find file
locate "*.txt" // give all the file ends with .txt

locat "file.txt" // full path of the file

# find all the dir and file
find dir (find .)

- find only dir
find . -type d

- find only files
find . -type f

- find only files in all the directories nested also
find . -type f -name "specific_file_name.extension"
find . -type f -name "*.txt"
find . -type f -iname "*.txt" (case senstive)
find . -type f -name "file*" (files which starts with the "file")


after 20 min ago
find . -type f -mmin -20

before 20 min ago
find . -type f -mmin +20

find . -type f -mmin +2 -mmin -10

find . -type f -mtime -10 (10 days ago)

find . -type f -maxdepth 1 (just show the file in current dir, 2 for another level depth)

find . -size +1k (files more then 1kb)

find . -empty (find all the file which are empty)

find . -perm 777 (find all the file who has permission 777)

find . -type f -name "*.txt" -exec rm -rf {} + (find all the file who has .txt and delete it)




# See the permission
ls -l file.txt (see the which has file permission)

chmod u=rwx,g=rx,o=r file.txt
where u = user, g = group, o = other
read = 4
write = 2
execute = 1

chmod 777 file.txt

# Searching inside file
case sensitive
grep "word" file.txt
grep -w "word" file.txt (search for the complete word)

grep -i "word" file.txt (not case sensitive)

grep -n "word" file.txt (show the line number)

grep -B 3 "word" file.txt (will previous 3 lines comes before word)

grep -in "word" ./*.txt (search the word in current dir and all the .txt files)

grep -rwin "word" . (in current dir search recursively)

grep -winl "word" . (all the files which contains "word" will be available here)

grep -winc "word" . (see the count)

grep -p "regex" file.txt



# history
history

history | grep "ls" (history of the ls command)

# edit .bashrc file for customization

# 
ctrl + A to move cursor at the start
ctrl + E to move cursor at the end

TAB is use for auto completion

#
!command (It's gonna run the previouos command)

sort -r programming.txt (sort the all in reverse)

jobs (all the running process started by the shell)

# Download file from internet
wget url
wget -o filename.txt url 

# see process
top (all running process)

kill port_id (gonna stop the process)

uname (kernel name)
uname -o
uname -m (architecture)
uname -r (kernel version)

lscpu (cpu details)

free (free memory)
free -h
vmstat (virtual memory)

check if user exists
getent group user_name

lsof (all the open file)

hostname
hostname -i

nslookup google.com (check ip address of the domain)
nslookup address


# Zip the file
zip zip_file_name.zip file_one.txt file_two.txt
uzip file.zip


# Add new user
sudo useradd user_name
sudo passwd user_name
sudo userdel user_name

# Working with operators
&&
||
|
>> (add it to file)
> (over write)

command1 && {command2; command3}



